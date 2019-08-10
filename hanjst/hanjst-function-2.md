# [Hanjst](/hanjst/index)
## Functions, Part-2
### Custom Functions

(Continued...)

1. `{include}`

`{include}` allows Hanjst to embed one template file or part of another template into the other template.  That is to say, `{include}` are used for including other template(s) in the current template. All variables available in the current template are also available within the included template(s).

The usage of `{include}` looks like as below.

```html
{include file="$innerTemplate"}
```
This is an emulator for including templates in the current template. The parameter "file" is pointing to a variable of Hanjst or JavaScript.

A simple example shows this process.

```html
{$innerTpl='<header class="navi"><a href="#">Homepa</a></header>'}
```



---

2. literal




#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


----
[Back to Top](/hanjst/hanjst-function)

[Previous](./hanjst-variable) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExNjQ1NDIwMTMsLTI0NjIwNjY4N119
-->