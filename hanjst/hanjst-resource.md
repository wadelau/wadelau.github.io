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
Functions....
Before or after,....

#### Third-party library
---
Conflicts....
Async....


### Images
---
Images are recommended in innerTpl, not in main template file as the template contents firstly will be rendered by current browser itself. This will cause `404` errors due to that the paths of images are not well-organized before Hanjst is being executed.



---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


---

[Back to Top](/hanjst/hanjst-resource)

[Previous](./data-in-json) ... [Next](./)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE5ODEyOTY3MSwxOTk4MDExNzQ3LC0xNz
U3NDgxNzE5XX0=
-->