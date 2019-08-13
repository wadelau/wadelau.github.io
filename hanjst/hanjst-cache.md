# [Hanjst](/hanjst/index)
## Hanjst Caching
### Server-side Caching
---
Hanjst server-side components are able to cache their raw contents of template files as so to accelerate the speed of generating outputs for HTTP requests.

Regarding to `GWA2 in Java`, caching service is provided with its core components of WebApp.class, here follows an example.

```java
//- suppose Hanjst is ready
Hanjst hanjst = new Hanjst();
String rawTemplate = hanjst.readTemplate(templateFile);
//- inside readTemplate to enable cache



```  


### Client-side Caching
---
@todo

---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


---

[Back to Top](/hanjst/hanjst-cache)

[Previous](./data-in-resource) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQ1NTcyNDEzLC0xMjA4NTgzNTAzLC04OT
IxOTMwMjNdfQ==
-->