# [Hanjst](/hanjst/index)
## Basic Syntax
### Hello World

Let's make a start with "Hello World".

```html
<html>
<body>
Hello {$user}!

<div id="Hanjstjsondata">
	{"user":"World", "copyright_year": 2019}
</div>
<script type="text/javascript" src="Hanjst.js"></script>
</body>
</html>
```

Hanjst will parse this template and generate a final representation of the HTML page as below.

```html
<html>
<body>
Hello World!

</body>
</html>
```
Inside the box of Hanjst, it reads template data from the element identified by "**Hanjstjsondata**", and reads template sentence from the element of BODY.

If these steps work well, Hanjst tries to load template data into current JavaScript run-time by introducing each key of JSON data as a variable. And Hanjst find each pair of lines enclosed with {...}.

When all of these are ready, computing  and replacements are going on each block of codes step by step.   


### Variables

Hanjst template variables start with the **$dollar** sign as default. They can contain numbers, letters and underscores, just like a variable in [JavaScript](https://www.javascript.com). You can reference arrays by index numerically or non-numerically. Also reference object properties and methods.

Some other template languages also defined a variable in this way, e.g. [PHP](php.net) or [Smarty](smarty.net).

1. Displaying
---
{$foo}
>display a variable

{$foo[1]}
>display the 2nd element of a zero-indexed array

{$foo['bar']}
>display the "bar" key value of an array

{\$foo.bar}
{\$foo.$bar}
>same as $foo['bar']

{$foo['bar']['car']}
{\$foo.bar.car}
{\$foo.\$bar.\$car}
>display multiple dimension array

2. Declaring
---
{$i=0}
{$s='abc'}


### Functions

#### Built-in Functions

#### Custom Functions


----
[Back to Top](/hanjst/hanjst-syntax)

[Previous](./hanjst-debug) ... [Next](./)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI5MzU2MDA0NV19
-->