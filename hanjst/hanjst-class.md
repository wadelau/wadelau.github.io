# [Hanjst](/hanjst/index)
## Hanjst Class
### Backend Overview
---
We have switched our default template engine from Smarty to Hanjst for all versions of GWA2.

Regarding to backend or server-side for Hanjst, it is only one task to do. The task in server-side is to output a group of key-value pairs in JSON format to client-side.

This preparation work of JSON can be split into two parts: one is to read all server-side data for business, and the other is to read other embedded template files and output them as common key-value pairs.

Here we have an example of this kind of JSON from server-side. (eg08111102)

```javascript
{
"innerTpl":"<header class=\"navi\"><a href=\"/\">Homepage</a></header>",
"serverTime":"2019-08-11 01:53:29",
"newsList":[
	{
		"title":"News-Title-1019",
		"id":1019
	},
	{
		"title":"News-Title-2019",
		"id":2019
	}
],
"mod":"news",
"act":"list"
}
```

A template file looks like this. (eg08111103)

```html
...
<!-- header -->
{$innerTpl}
<!-- header,end -->
<!-- news list -->
<ul>
{foreach $newsList as $n}
	<li>
	{foreach $newsList[$n] as $p}
		<span>{$p}: {$newsList[$n][$p]}</span>
	{/foreach}
	</li>
{foreachelse}
	<li>No data.</li>
{/foreach}
</ul>
<!-- news list, end -->
<div>
	<p>Server Time: {$serverTime}</p>
</div>
....

```

If all of these work well, we finally generate a pure HTML like this. (eg08111104)

```html
...
<!-- header -->
<header class="navi"><a href="/">Homepage</a></header>
<!-- header,end -->
<!-- news list -->
<ul>
	<li>
		<span>id: 1019</span>
		<span>title: News-Title-1019</span>
	</li>
	<li>
		<span>id: 2019</span>
		<span>title: News-Title-2019</span>
	</li>
</ul>
<!-- news list, end -->
<div>
	<p>Server Time: 2019-08-11 01:53:29</p>
</div>
....
```

### Hanjst Class for Server-side
---
So for each back-end language, it is mandatory to create a class of methods for Hanjst to cope with JSON data in server-side.

Generally the class has a container, e.g., HashMap, Associative Array, to hold all variables which need to be output at the end of this request.

For instance, in GWA2 Java, a news reader may look like this. (eg08111105)

```java

HashMap output = new HashMap();

//- suppose news is initilized
HashMap newList = news.getList();
output.put("newsList", newsList);
output.put("serverTime", Wht.dateFormat((new Date())));

//- suppose hanjst is initilized
String jsonData = hanjst.map2Json(output);
String currentTemplateFile = "index.html";
String jsonDataArea = "HANJST_JSON_DATA";
String templateContent = hanjst.readTemplate(currentTemplateFile);

//- replacements and display
templateContent = templateContent.replace(jsonDataArea, jsonData);
out.println(templateContent);

```

All of these codes can be found in [GWA2 in Java in GitHub](https://github.com/wadelau/GWA2/blob/master/java/comm/footer.inc.jsp).

A simple flow chat shows the process here.

**Hanjst server-side** (eg08111105)  
	--> Raw HTML (eg08111102 + eg08111103)
	--> **Hanjst client-side**
	--> Final HTML (eg08111104)



---

#### Related works

1. [Hanjst with GWA2 in Java](https://github.com/wadelau/GWA2/tree/master/java)
2. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)
3. [GWA2 switch from Smarty to Hanjst](https://ufqi.com/blog/gwa2-8-years-with-smarty-to-hanjst/)

---

[Back to Top](/hanjst/hanjst-function-class)

[Previous](./hanjst-function-2) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTExOTI1ODI0MSw3MjU4NDA1OCwxNzA5MT
MyMTk0LC0xMjU4NzQ5NzI3LDE3MjA1NDY0OTZdfQ==
-->