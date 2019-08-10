# [Hanjst](/hanjst/index)
## Functions, Part-2
### Custom Functions

(Continued...)

1. `{include}`

`{include}` allows Hanjst to embed one template file or part of another template into the other template.  That is to say, `{include}` are used for including other template(s) in the current template. All variables available in the current template are also available within the included template(s).

The `{include}` tag must have the _`file`_ attribute which contains the template contents, not an actual resource  file path.

The usage of `{include}` looks like as below.

```html
{include file="$innerTemplate"}
```
This is an emulator for including templates in the current template. The parameter "file" is pointing to a variable of Hanjst or JavaScript.

A simple example shows this process.

```html
{$innerTpl='<header class="navi"><a href="/">Homepage</a></header>'}

<div id="top">
{include file="$innerTpl"}
<div class="main">
	This is main content.
</div>
</div>
```

These template lines will be parsed into pure HTML contents as below.

```html

<div id="top">
<header class="navi"><a href="/">Homepage</a></header>
<div class="main">
	This is main content.
</div>
</div>

```
In real and production environments, it is quite sophisticated that there are lots of key points to be considered. As stated above, it is straightforward to include pure template contents into current template. However, it is not easy to include some contents with extra resources, images, css and JavaScript.

Thes
 


---

2. literal




#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


----
[Back to Top](/hanjst/hanjst-function)

[Previous](./hanjst-variable) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1NjM0NTUxMDEsLTI0NjIwNjY4N119
-->