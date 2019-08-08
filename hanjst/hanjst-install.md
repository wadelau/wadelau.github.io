# [Hanjst](/hanst/index)
## Hanjst Installation
### Simple and Basic

Hanjst source codes are written in pure JavaScript and has no dependency on any of third-party libraries. and all of codes are wrapped into a single JavaScript source file, Hanjst.js.

So the simplest way to install Hanjst is to [download a copy of Hanjst.js](https://github.com/wadelau/Hanjst) and put it in an HTML as below.

```html
<html>
....
<body>
....
<div id="Hanjstjsondata">
	{"copyright_year": 2018}
</div>
<script type="text/javascript" src="Hanjst.js"></script>
</body>
</html>
```
There are two HTML blocks needed to run the Hanjst. 
1. The first is a div which has an ID of "Hanjstjsondata" and holds all the data (format in JSON) needed to be merged into the final page presentations.
2. The 2rd one is a script element which introduces the source file of Hanjst and its trigger. The source file will check all the pages to find Hanjst template sentences and parse them into final HTML codes and print out all of them with resources if needed.

Please pay attention to BODY element, Hanjst need it to be its parent node.

#### Extended Setup

### Environments

### Run-time


----
[Back to top](/hanjst/hanjst-install)

[Previous](./what-is-hanjst) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTU2MDIyMzU4MywxODI4Mjg4ODk3XX0=
-->