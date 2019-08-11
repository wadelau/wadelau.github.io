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

This will be done by a global variable in Hanjst. The variable is so-called `viewdir` and it can be see as the relative or absolute path for all resources that need to be loaded with current template.

Given that we have an embedded template lines looks like 



### Scripts
---
ddd

#### Third-party library
---
dsd


### Images
---
dsd



---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


---

[Back to Top](/hanjst/hanjst-resource)

[Previous](./data-in-json) ... [Next](./)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDcwMjM0MDksMTk5ODAxMTc0NywtMTc1Nz
Q4MTcxOV19
-->