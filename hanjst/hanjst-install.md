# [Hanjst](/hanjst/index)
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
1. The first is a DIV which has an ID of "Hanjstjsondata" and holds all the data (format in JSON) needed to be merged into the final page presentations.
2. The 2nd one is a SCRIPT element which introduces the source file of Hanjst and its trigger.

The source file will run automatically and check all the elements of the host page to find Hanjst template sentences and parse them into final HTML codes and print out all of them with resources if needed.

Please pay attention to BODY element, Hanjst need it to be its parent node.

That's all!
The powerful and unmatched template engine Hanjst has been implemented successfully and will be running automatically, seamlessly and efficiently. 

---
#### Extended Setup
With more we learned from Hanjst, there are some options to install and run the Hanjst template engine.

Here is an advanced and sophisticated example of extended setup with Hanjst.
```html
<html>
....
<body>

....
<div id="Hanjstjsondata">
	{"copyright_year": 2018}
</div>
<!-- Hanjst codes begin -->
<script type="text/javascript" async>
    window.Hanjst = {'JsonDataId':'Hanjstjsondata', 
	    'IsDebug': true}; // optional
</script>
<script type="text/javascript" src="Hanjst.js" async></script>
<noscript>JavaScript Required for Hanjst.</noscript>
<!-- Hanjst codes end -->
</body> 
</html>
```
We adds two more elements for Hanjst, trying to adjust the behaving of the template engine.  
1. a SCRIPT element for run-time settings where we set a global variable **window.Hanjst** as a container. There are two key-value pairs inside the global variable. 
2. a NOSCRIPT element for compatible with obsolete browsers. It displays a friendly warning when detecting that there is no JavaScript-enabled in current browser.

Alternatively, we also add the keyword  **async** for JavaScript scripts.  "async" allow scripts to be loaded wisely with non-blocking pipe when browsers downloading and pages rendering. 

All of these additions are optional, so they can be removed and omitted.

The key-value pairs inside window.Hanjst are "**JsonDataId**" and "**IsDebug**". 
The first one tells Hanjst where the JSON data resides in and the 2nd tells Hanjst whether to display more debugging messages in browsers' console log.

We will investigate deeply into [Hanjst configurations and settings](./hanjst-config) in late sections.

#### Waiting Layer
Sometimes it is necessary to hide JSON data from end-users. Usually there are two methods to make this done.

1. To add a waiting layer.
End-users will see a waiting layer if we choose this method by adding a top-index DIV layer as the very first element of BODY.
```html
<div id="Hanjstloading" 
	style="width:100%;height:100%;z-index:99;opacity:0.92;position:absolute;background-color:#ffffff;"> 
	Loading... 加载中... 
</div>
```

2. To set JSON data DIV hidden.
End-user will see a few parts of the loading page if we choose this method by set a CSS style as below.
```html
<div id="Hanjstjsondata" 
	style="display:hidden;">
	{"copyright_year": 2018}
</div>
```

Template designers and developers are encouraged to implement one of them to prevent the 


#### Related works
1. [Hanjst in -GitHub]([https://github.com/wadelau/Hanjst](https://github.com/wadelau/Hanjst))


----
[Back to Top](/hanjst/hanjst-install)

[Previous](./what-is-hanjst) ... [Next](./hanjst-config)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwMzY4OTcxNTIsMTU2MDIyMzU4MywxOD
I4Mjg4ODk3XX0=
-->