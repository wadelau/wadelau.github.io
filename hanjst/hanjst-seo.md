# [Hanjst](/hanjst/index)
## Hanjst Search Engine Optimization
### Title, Description and Keyword
---
It is an unexpected and unwelcome drawback for JavaScript-based template engines that they are not friendly to search engines. In other words, search engines are unable to extract plain contents from JavaScript as well as from pure HTML.

Though search engines grows powerful as fast as the speed of Moore's Law, we still put search engine optimization (SEO) under consideration when making design and development of Hanjst language and engine.

The goal will soon be reached as we start towards from the two ends that search engines are getting smarter and smarter so they are read and extract correct data from JavaScript and Hanjst is getting better and better to act like it is a purl HTML.

Usually, a page's title, description and keyword (TDK) are variables generated from server-side and passed into client-side by being wrapped into a JSON data. 
Unfortunately, search engines are unable to read correct title, description and keyword from the JSON data.
Hanjst has some placeholders to meet this requirements. That is to say, Hanjst leave pre-defined placeholders for a page's title, description and keyword.

These TDK will be replaces in server-side just like what happened to `HANJST_JSON_DATA` described in last section [Hanjst Ready to go](./hanjst-ready-to-go).

Here is an example to show the TDK in a template file. (eg08131528)

```html
<html>
<head>
	<title>Serv_Page_Title</title>
	<meta name="description" content="Serv_Page_Desc"/>
    <meta name="keywords" content="Serv_Page_Keyword"/>
</head>
<body>
....
</body>
</html>
```

When the template is read in server-side the placeholders for TDK will be replaces with actual values.

```php

//- resp data container
$respData = array();
$tdkArr = array(
	"Hanjst is so powerful.",
	"Hanjst is a JavaScript-based template language and engine. It is very powerful and has a few of exciting features as back-end tempalte engines.",
	"Hanjst, 汉吉斯特, template engine, JavaScript"
); // keys are optional
$respData['tdkArr'] = $tdkArr;

//- template contents processing
$tplFile = "news.html";
$jsonDataPlaceHolder = "HANJST_JSON_DATA";
$tplContent = file_get_contents($tplFile);
$tplContent = str_replace($jsonDataPlaceHolder , $jsonDataStr, $tplContent);

//- tdk replacements
$tdkPlaceHolders = array("Serv_Page_Title", "Serv_Page_Desc", 
	"Serv_Page_Keyword");
$tplContent = str_replace($tdkPlaceHolders, $respData['tdkArr'], 
	$tplContent);

```

So that template contents have been merged with actual values in server-side and its contents looks exactly like a pure HTML which is welcome to search engines.

The template file (eg08131528) looks like as below from the view of a search engine.

```html
<html>
<head>
	<title>Hanjst is so powerful.</title>
	<meta name="description" content="Hanjst is a JavaScript-based template language and engine. It is very powerful and has a few of exciting features as back-end tempalte engines."/>
    <meta name="keywords" content="Hanjst, 汉吉斯特, template engine, JavaScript"/>
</head>
<body>
....
</body>
</html>
```




### Links
---
dddsd

### Plain Contents
---
dddsd


---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)
2. [GWA2 in Java](https://github.com/wadelau/GWA2/)

---

[Back to Top](/hanjst/hanjst-seo)

[Previous](./hanst-ready-to-go) ... [Next](./)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTgzNDg2OTI2LC0xNjExNjczODcxLC0zMT
g3Nzk4MjNdfQ==
-->