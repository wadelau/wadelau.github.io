# [Hanjst](/hanjst/index)
## Functions, Part-2
### Custom Functions

(Continued...)

1. `{include}`

`{include}` allows Hanjst to embed one template file or part of another template into the other template.  That is to say, `{include}` are used for including other template(s) in the current template. All global variables available in the current template are also available within the included template(s).

The `{include}` tag must have the _`file`_ attribute which contains the template contents, not an actual resource  file path.

`{include}` allows multiple layers in depth, which help designers organize template contents in a top-down mode. 

The usage of `{include}` looks like as below.

```html
{include file="$innerTemplate"}
```
This is an emulator for including templates in the current template. The parameter "file" is pointing to a variable of Hanjst or JavaScript. Usually, the contents will be organized in server-side and sent to client via HTTP requests.

A simple example shows this process.

```html
{$innerTpl='<header class="navi"><a href="/">Homepage</a></header>'}

<div id="top">
<!-- embedded content -->
{include file="$innerTpl"}
<!-- embedded content, end -->
<div class="main">
	This is main content.
</div>
</div>
```

These template lines will be parsed into pure HTML contents as below.

```html

<div id="top">
<!-- embedded content -->
<header class="navi"><a href="/">Homepage</a></header>
<!-- embedded content, end -->
<div class="main">
	This is main content.
</div>
</div>

```
It is quite sophisticated that there are lots of key points to be considered  in real and production environments. As stated above, it is straightforward to include pure template contents into current template. However, it is not easy to include some contents with extra resources, images, CSS and JavaScript.

These extra resources needs to be handled paths and load-order. That is to say, including here is not only to load pure contents but also to pull all extra resources it points to into the current template.

---

2. `{literal}`

`{literal}` allows a block of template lines to be taken literally. This is rare for designers except that we would like to explain Hanjst in detail with examples.

Anything within the block of `{literal}...{/literal}`  is not interpreted by Hanjst, but displayed as it is in plain text in the form of Hanjst syntax.

```html
<!-- try literal -->
<div class="literal">
{literal}
    {if $user['feedback'] == 2}
        {$user['age']}
    {/if}
{/literal}
</div>
```
These template lines will be shown as original form in final purl HTML elements.

```html
<!-- try literal -->
<div class="literal">
    {if $user['feedback'] == 2}
        {$user['age']}
    {/if}
</div>
```

In common and daily usage, `{literal}...{/literal}` tags are normally not necessary.


---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)
2. [Hanjst Improvements on JavaScript Run-time](https://ufqi.com/blog/hanjst-javascript-runtime/)

----
[Back to Top](/hanjst/hanjst-function-2)

[Previous](./hanjst-function) ... [Next](./hanjst-nodejs)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzNzQ3NzM5NTgsLTE2NDY1OTY3MzYsLT
g4NDU0ODIzLC0yNDYyMDY2ODddfQ==
-->