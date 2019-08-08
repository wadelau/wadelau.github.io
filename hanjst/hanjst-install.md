# [Hanjst](/hanst/index)
## Hanjst Installation
### Simple and Basic

Hanjst source codes are written in pure JavaScript and has no dependency on any third-party libraries. and all of codes are wrapped into a single JavaScript source file, Hanjst.js.

So the simplest way to install Hanjst is to download a copy of Hanjst and put it in an HTML as below.

```html
<div id="Hanjstjsondata">
{
	"newslist":[
		{"title":"Runtime in client-side, reduce computing render in server-side;", "href":"#f1"},
		{"title":"Language-independent, not-bound with backend scripts/languages;", "href":"#f2"},
		{"title":"Totally-isolated between MVC, data transfer with JSON;", "href":"#f3"}
	],
	"copyright_year": 2018
}
</div>

<!-- Hanjst codes begin -->
<script type="text/javascript" async>
    window.Hanjst = {'JsonDataId':'Hanjstjsondata', 'IsDebug': true}; // optional
</script>
<script type="text/javascript" src="Hanjst.js" async></script>
<noscript>JavaScript Required for Hanjst.</noscript>
<!-- Hanjst codes end -->

</body>
```

#### Extended Setup

### Environments

### Run-time


----
[Back to top](/hanjst/hanjst-install)

[Previous](./what-is-hanjst) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyNzIzNTc4OTYsMTgyODI4ODg5N119
-->