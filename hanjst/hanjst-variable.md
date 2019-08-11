# [Hanjst](/hanjst/index)
## Variables and Modifiers
### Variables

#### Variables from Server-side
Hanjst variables come from JSON data which being generated from its server response via HTTP request.

Variable names are actually the key names in JSON data. Therefore, the main source to define a variable in Hanjst is server-side, that is to say, declaring in server-side what will be output to clients and named as variables.

Another way to define a variable in Hanjst is client-side, e.g. define a global or local variable just like a common variable in JavaScript. Furthermore, this is the way to define a function, a class or an object.

Define JSON keys in server-side, for instance in Java as below. (eg08101128)

```java
//- define a map
HashMap map = new HashMap();
map.put("userName", "Alice");

//- call Hanjst server-side object
Hanjst hanjst = new Hanjst();
String jsonData = hanjst.map2Json(map);
jsonData = "<div id=\"Hanjstjsondata\">"+jsonData+"</div>";

//- append data to output
out.println(jsonData);
```

Hopefully, this codes will output an HTML as below.

```html
<div id="Hanjstjsondata">
	{"userName": "Alice"}
</div>
```
After Hanjst engine has been triggered by **window.onload**,  the key,  "userName", will be parsed as a variable in Hanjst or JavaScript as below.

```javascript
$userName = 'Alice';
```

Therefore, suppose we have the following Hanjst template file with a line:

```html
<p>Hello, {$userName}! You are welcome.</p>
```
The template content will be finally translated into pure HTML sentence.

```html
<p>Hello, Alice! You are welcome.</p>
```

This is the travelling of a variable in Hanjst.
A simple variable goes through server-side and client, back-end and front-end like this way. And any of other variables, like array, object, will also travel in this routing. 

#### Variables from client-side

It is obvious that a variable  from server-side has a long way to walk through. But a variable from client-side is lucky and has no such a long walk.

Depends on whether a variable is global or local, it can be declared in any place in Hanjst whenever or wherever. (eg08101129)

```html
<!-- globally -->
{$i=0}
{$myTime=(new Date()).getTime()}

<!-- locally -->
{foreach $newsList as $news}
	{$news['title']}
{/foreach}
```
#### Conflicts with Third Parties

As shown above, Hanjst will parse all keys in JSON data into variable names in current JavaScript run-time. There is possible that too many global variables will make conflicts with third parties.

For example, the $dollar sign, the single sign is set to a global variable designated into jQuery. If a page loaded both jQuery and Hanjst, potential conflicts may exist.

Bearing this in mind, we have added validation in process of the parsing works. When any conflict raised, an exception is being thrown and developers need to fix them before continuing next.

---
### Modifiers

#### Modifiers with JavaScript built-in functions

There are so many functions which can be used directly in Hanjst.
See [Standard built-in objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects) for detailed list.

Examples are demonstrated below.

```html
{$str='Hello World!'}
{$str.substring(0,5)}
<!-- output: Hello -->

{$num=123.4}
{$parseInt($num)}
<!-- output: 123 -->

```
 
#### Modifiers with Custom functions

Define a custom function in JavaScript：
```javascript
function myFunc(x, y){
	return x = x * y;
}
```
Call it in HTML written in Hanjst template language:
```html
<!-- define variables -->
{$a=3}
{$b=5}
<!-- display a custom function result -->
{$myFunc($a, $b)}
<!-- output: 15 -->
```

---
### Modifiers Chain

JavaScript allow function chain, so it is easy to use for Hanjst modifiers.
Here is an example to show the chain.

```html
{$a=3}
{$b=5}
{$myFunc($myFunc($a, $b), $myFunc($a, $b))}
<!-- output: 3*5 * 3*5 = 225 -->

{$str = "Hello World!"}
{$str.substring(0,5).toLowerCase()}
<!-- output: hello -->
```

---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/) .
2. [MDN JavaScript Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects) .

----
[Back to Top](/hanjst/hanjst-variable)

[Previous](./hanjst-syntax) ... [Next](./hanjst-function)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbNzE0ODkwMTU3LDE2MjQ3Njk0MywxNjU1Nz
Y0MjcxLDEzMzg0Njk1MjYsLTcyNjg0NjE1NCwxMzE0MTM1NDY0
LDg1MTA0ODYxM119
-->