# [Hanjst](/hanjst/index)
## Variables and Modifiers
### Variables

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

Hopeful



### Modifiers
....


#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


----
[Back to Top](/hanjst/hanjst-variable)

[Previous](./hanjst-syntax) ... [Next](./hanjst-function)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2MDg2OTU0MTQsMTMxNDEzNTQ2NCw4NT
EwNDg2MTNdfQ==
-->