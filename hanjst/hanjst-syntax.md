# [Hanjst](/hanjst/index)
## Basic Syntax
### Hello World

Let's make a start with "Hello World". (eg08092010)

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
---
Hanjst template variables start with the **$dollar** sign as default. They can contain numbers, letters and underscores, just like a variable in [JavaScript](https://www.javascript.com). We can reference arrays by index numerically or non-numerically, and also reference object properties and methods.

Some other template languages also defined a variable in this way, e.g. [PHP](php.net) or [Smarty](smarty.net).

#### Displaying
---

{$foo}

{=$a+1}
>display a variable

>display a variable after its addtion

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
>display a multiple dimension array


#### Declaring
---
{\$i=0}

{\$s='abc'}
>define a variable

{\$i++}

{\$i+=2}
>add 1, or 2 to variable i

{\$myArr=[]}

{\$myArr[0]=1}
>define an array
>and set an element

{$myList=new Object()}

{$myList['key']='value'}
>define an object
>and set a key


---
### Functions

Hanjst functions are all functions of JavaScript. Reversely, all JavaScript functions and objects are all accessible to the current Hanjst.

{$foo()}
>display the return of function "foo"

{\$foo($bar)}
>display the return of function "foo", with a parameter "bar"

---
#### Built-in Functions

As stated above, all built-in functions in JavaScript are accessible in Hanjst template run-time, so there too many to iterate the list.

See [MDN JavaScript Docs online](https://developer.mozilla.org/en-US/docs/Web/JavaScript) for detailed instructions and references.

#### Custom Functions
---

Besides of so many built-in JavaScript functions, developers are encouraged to make custom objects, classes or functions for specific usages.

An example is attached below.

Define the custom function in JavaScript：
```javascript
function foo(x, y){
	return x = x + y;
}
```
Call it in HTML written in Hanjst template language:
```html
<!-- define variables -->
{$a=3}
{$b=5}
<!-- display a custom function result -->
{$foo($a, $b)}
<!-- output: 8 -->
```
---
### Comments

Comments in Hanjst have two parts.
For JavaScript part, 

```javascript
//-- this is a line comment
/*
 * these are block comment
 */
```

For HTML part,

```html
<!-- this is a line comment in html -->
```

---
#### Related works

1. [Mozilla Developer Network, Web Docs, JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
2. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


----
[Back to Top](/hanjst/hanjst-syntax)

[Previous](./hanjst-debug) ... [Next](./hanjst-variable)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc2NjA3MDI2MSw4Mjk4NTIwNjIsMTAwNT
QyNTI0NSwtMjAwODI4NTAxMl19
-->
