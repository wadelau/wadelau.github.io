# [Hanjst](/hanjst/index)
## Hanjst Resources
### Paths
---
A few of paths in Hanjst will be replaced in server-side, which has been shown with examples in previous section, i.e. [Hanjst Replacements](./hanjst-replacement), (eg08112313).

```html
...
<link rel="stylesheet" href="/path-to/view/css/style.css" />
...
<img src='/path-to/view/images/myfav.png' alt=""/>

```

It is also necessary that replacements will be triggered in client-side when Hanjst attempts to load embedded templates which contains several lines of extra resources, e.g. images, CSS and JavaScript.

This will be done by a global variable in Hanjst. The variable is so-called `viewdir` and it can be seen as the relative or absolute path for all resources that need to be loaded with current template.

Given that we have an embedded template consist of lines as below.

```html
{$innerTpl='<img src="images/myfav.png" alt=""/>'}

...
{$innerTpl}
```

Hanjst will replace the static and relative path of the image with `viewdir` when parsing the $innerTpl. After that, the template lines looks like as below.

```html
<img src="/path-to/view/images/myfav.png" alt=""/>
```

### Scripts
---
#### JavaScript Paths
Scripts paths are same with other resources like images, CSS.
See the above section for details with paths.

What's needed to be mentioned are JavaScript functions places and the loading of third-party library.

#### Functions Positions
JavaScript functions in Hanjst are different with their places or positions.

A function defined in the current main template and called before the main function of Hanjst, will be triggered again during the process of Hanjst parsing work. So if the function has been restricted with run-only-once, it is better to place this function after Hanjst main function.

Here comes an example to make clear demo. (eg08122040)

```html
<html>
...
<body>
....
<script type="text/javascript">
function myTime(){
	return ((new Date()).getTime());
}
myTime();
</script>
....
<script type="text/javascript" src="Hanjst.js"></script>
...
</body>
</html>
```
In the example, the function `myTime` will be executed twice as the first time it is called when current browser is rendering this page, and the second time it is called by Hanjst.

However, if we relocate `myTime` from current place to a place after Hanjst, then myTime will be triggered  only once.  The revised example lists as below. (eg08122043)

```html
<html>
...
<body>
....
<script type="text/javascript" src="Hanjst.js"></script>
...
<script type="text/javascript">
function myTime(){
	return ((new Date()).getTime());
}
myTime();
</script>
</body>
</html>
```

#### Scripts from Inner Templates

It needs be careful to load scripts from inner or embedded templates. The scripts may include pure JavaScript or extra resource JavaScript file.

For the first kind of pure JavaScript, it is easy to import as a part of current page.

For the second kind of extra resource JavaScript file, paths remedy work is necessary to make corrections on those extra resource JavaScript files.
See the very first part of this page for details on paths.

#### Third-party library
---
Third-party library will work well together with Hanjst. 

There are some practical guides for including or import third-party libraries.

JavaScript codes which will be run only once after Hanjst's work, should be placed below and after Hanjst. And also please keep in mind:
> `use strict` mode, add comma for each sentence;
>src of Objects should be loaded in sync mode, e.g. jquery.min.js;
>invokes with Objects should be loaded in async mode, e.g. project.base.js;


### Images
---
Images are recommended in innerTpl, not in main template file as the template contents firstly will be rendered by current browser itself. This will cause `404` errors due to that the paths of images are not well-organized before Hanjst is being executed.

This example below shows the demo. (eg08122054)

```html
<html>
<body>
...
<div>
	<!-- acceptable -->
	<img src="images/defaultfav.png" alt=""/>
	<!-- acceptable, but not recommended -->
	<img src="images/{$userFav}" alt="userFav"/>
</div>
....
<script type="text/javascript" src="Hanjst.js"></script>
...
</body>
</html>
```


---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


---

[Back to Top](/hanjst/hanjst-resource)

[Previous](./data-in-json) ... [Next](./hanjst-cache)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTA1NDQwODg5LC0zNjI4NTY3MTUsMTE5OD
EyOTY3MSwxOTk4MDExNzQ3LC0xNzU3NDgxNzE5XX0=
-->