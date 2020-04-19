# [Hanjst](/hanjst/index)
## Functions, Part-3
### Custom Functions

(Continued...)

1. {\$showImageAsync($imgId)}

It is quite understood that a web browser will invoke a single HTTP request to a server for its referring resource file when parsing an HTML element as `<img src="/path/to/abc.png"`.

However, it is quite annoying if the image path is represented with variables from Hanjst. Here is a common but error-prone sentence written in Hanjst.

```html
...
<img src="{$imgPath}" alt=""/>
...
```
This sentence will trigger a real HTTP request to a server for asking for the resouce marked with the path,  "{$imgPath}", apparently, this will yiled a 404 page error.

In order to overcome this issue, Hanjst introduces a custom function named `showImageAsync`. The function will show an image with Hanjst variables in its image path. Here is the revised version of the example above.

```html
...
<img src=”data:image/png;base64,MA==” alt=”” id=”{$imgId}” data-src=”{$imgPath}”/>  
{$showImageAsync($imgId)}
...
```

Some other resources are also silimiar with the HTML image element, therefore Hanjst may add more custom functions to meet these kinds of requirements, such as,

`{$loadScriptAsync($scriptId)}`

(drafting...)

`{$loadCSSAsync($cssId)}`

(drafting...)



---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)
2. [Hanjst Improvements with showImageAsync](https://ufqi.com/blog/hanjst-showimage-dotpos/)

----
[Back to Top](/hanjst/hanjst-function-3)

[Previous](./hanjst-function-2) ... [Next](./hanjst-nodejs)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc1ODUxNjA5MF19
-->