# [Hanjst](/hanjst/index)
## Hanjst Server-side Replacements
### JSON Data Placeholder
---
We have seen lots of examples written in Hanjst template language till now. But most of them are codes snippets or fragments due to that they are written on a single proposal to illustrate one of the aspects of Hanjst.

In fact, the raw template file looks not so pretty as the examples presented above.

```java
String jsonDataArea = "HANJST_JSON_DATA";
```

The following example shows that we place an placeholder in the position where we will put all JSON data from server-side in. (eg09111146)

```html
<html>
....
<body>
...
<!-- Hanjst codes bgn-->
<div id="Hanjstjsondata" style="display:none;">
	HANJST_JSON_DATA
</div>
<script type="text/javascript">
    window.Hanjst = {
	    'JsonDataId':'Hanjstjsondata','IsDebug': false
    }; // optional
</script>
<script type="text/javascript" 
	src="js/Hanjst.js?v=201906171103"></script>
<noscript>JavaScript Required for Hanjst.</noscript>
<!-- Hanjst codes end -->
</body>
</html>
```

Here `HANJST_JSON_DATA` is the placeholder where Hanjst will replace it with actual JSON data in server-side. This can be seen in [(eg08111105)](./hanjst-class) in previous section.

This is the very first or raw form of Hanjst template file which has not yet handled by Hanjst server-side. It will present another look after the template file has been replaced several times in server-side.

For instance, the template contents (eg08111146) in server-side will be replaced as below and sent to the client-side, that is to say, what we see in client-side. (eg08111147)

```html
<html>
....
<body>
...
<!-- Hanjst codes bgn-->
<div id="Hanjstjsondata" style="display:none;">
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
</div>
<script type="text/javascript">
    window.Hanjst = {
	    'JsonDataId':'Hanjstjsondata','IsDebug': false
    }; // optional
</script>
<script type="text/javascript" 
	src="js/Hanjst.js?v=201906171103"></script>
<noscript>JavaScript Required for Hanjst.</noscript>
<!-- Hanjst codes end -->
</body>
</html>
```

Hanjst client-side will take the raw template contents (eg08111147) and try to parse them into pure and final HTML elements, which is what we have seen in [(eg08111104)](./hanjst-class) in previous section.
  

### Templates Directory
---
In a common implementation of Web application which deploys MVC-based architecture there will be a sub directory call `view`.

The `view` will hold all template raw files and files would connect to each other with relative paths. Therefore these relative paths will be fixed or replaced with actual run-time paths which may be same or not same with its original values.

It should not be the same if the application directory is not the root directory of a website. So it is inevitable to make replacements to all of this view paths.

Given we have the template lines as below. (eg08111220)

```html
...
<link rel="stylesheet" href="css/style.css" />
...
<img src='images/myfav.png' alt=""/>

```

The raw template lines will be replaced in server-side with actual paths of the web application.

```html
...
<link rel="stylesheet" href="/path-to/view/css/style.css" />
...
<img src='/path-to/view/images/myfav.png' alt=""/>

```

### Multiple Template Versions
---
Furthermore, we have multiple versions for the web application, e.g. desktop version, mobile phone version, mobile pad version, android app or iOS app, etc.

If so, we have to set every sub directory for each version of the web application. (eg08111227)

`view/desktop`
`view/mobile`
`view/pad`
`view/android`
`view/iphone`

Therefore, the template lines in (eg08111220) will be further replaced with actual view directory and its corresponding sub directory.

```html
...
<link rel="stylesheet" href="/path-to/view/descktop/css/style.css" />
...
<img src='/path-to/view/desktop/images/myfav.png' alt=""/>

```

### Other Replacements
---
Hanjst template files maybe needs to be replaced some other placeholders with specific keywords, e.g., for SEO considerations, a pages's title needs to be replaced with actual title for current page.

This will be investigated with great details in following sections, i.e., [Search Engine Optimization](./hanjst/hanjst-seo).

---

#### Related works

1. [Hanjst with GWA2 in Java](https://github.com/wadelau/GWA2/tree/master/java)
2. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)
3. [GWA2 switch from Smarty to Hanjst](https://ufqi.com/blog/gwa2-8-years-with-smarty-to-hanjst/)

---

[Back to Top](/hanjst/hanjst-function-replacement)

[Previous](./hanjst-class) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0NTA0MTA0LDc1MTQ3MjIxOCw0NjA1OD
IwNjMsMTU2NjgxMDcxNywtODI2NjE3MDc0XX0=
-->