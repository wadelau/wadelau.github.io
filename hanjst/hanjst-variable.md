# [Hanjst](/hanjst/index)
## Variables and Modifiers
### Variables

#### Variables from Server-side
Hanjst variables come from JSON data which being generated from its server response via HTTP request.

Variable names are actually the key names in JSON data. Therefore, the main source to define a variable in Hanjst is server-side, that is to say, declaring in server-side what will be output to clients and named as variables.

Another way to define a variable in Hanjst is client-side, e.g. define a global or local variable just like a common variable in JavaScript. Furthermore, this is the way to define a function, a class or an object.

Define JSON keys in server-side, for instance in Java:

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

It is obvious that a variable  



### Modifiers
....


#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


----
[Back to Top](/hanjst/hanjst-variable)

[Previous](./hanjst-syntax) ... [Next](./hanjst-function)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgxMjkxNzkwMiwxMzE0MTM1NDY0LDg1MT
A0ODYxM119
-->