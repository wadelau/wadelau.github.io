# [Hanjst](/hanjst/index)
## Hanjst Ready-to-go
### A Standalone Example
---
Let's rolls up sleeves and have a ready-to-go example to demonstrate what we have just discussed before and validate them from a practical perspective of engineering.

The example blow will show a news items list on a page.

1. Template File

```html
<html>
<head>News List</head>
<body>
<div id="Hanjstloading" 
	style="width:100%;height:100%;z-index:99;opacity:0.92;position:absolute;background-color:#ffffff;"> 
	Loading... 加载中... 
</div>
<div id="newsList">
<ul>
{foreach $newsList as $n}
	<li>
		{foreach $newsList[$n] as $np}
			<dt>{$np}: {$newsList[$n][$np]}</dt>
		{/foreach}
	</li>
{foreachelse}
	<li>No data.</li>
{/foreach}
</ul>
</div>
<div id="Hanjstjsondata" 
	style="display:hidden;">
	HANJST_JSON_DATA
</div>
<script type="text/javascript" src="Hanjst.js" async></script>
<noscript>JavaScript Required for Hanjst.</noscript>
</body>
</html>
```

Copy these lines and as a file: news.html .

2. Hanjst Server-side in PHP

```php
$respData = array();
//- data preparing
$newsList = array(
	array("id"=>12, "title"=>"Hanjst is releasing to pulic."),
	array("id"=>34, "title"=>"Hanjst Ready-to-go."),
	array("id"=>56, "title"=>"Hanjst has outpaced all other jst.")
);
array_push($respData, $newsList);
$jsonData = json_encode($);

//- template contents
$tplFile = "news.html";
$tplContent = file_get_contents($tplFile);

```

3. Raw Template File

dd

4. Final Parsed HTML

dd



### GWA2 in Java
---

@todo


---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)
2. [GWA2 in Java](https://github.com/wadelau/GWA2/)

---

[Back to Top](/hanjst/hanjst-ready-to-go)

[Previous](./hanst-cache) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbODgzNTI3NDI2XX0=
-->