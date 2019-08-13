# [Hanjst](/hanjst/index)
## Hanjst Caching
### Server-side Caching
---
Hanjst server-side components are able to cache their raw contents of template files as so to accelerate the speed of generating outputs for HTTP requests.

Regarding to `GWA2 in Java`, caching service is provided with its core components of WebApp.class, here follows an example. (eg08131113)

```java
//- suppose Hanjst extends WebApp, and be ready
Hanjst hanjst = new Hanjst();
String rawTemplate = hanjst.readTemplate(templateFile);

//- inside Hanjst.readTemplate to enable cache
//- suppose Wht is ready
public String readTemplate(String mytpl){
	String tplcont = "";
	HashMap hmArgs = Wht.initHashMap("file,enablecache",
		mytpl+",1");
	HashMap hmtmp = this.getBy("file:", null, hmArgs);
	if((boolean)hmtmp.get(0)){
		tplcont = (String)hmtmp.get(1);
		tplcont = this.replacePath(tplcont, viewdir);
	}
	return tplcont;
}
```  

In the example above, the `enablecache` tells GWA2 core components to try its cache service firstly for the targeted object. This kind of services are also available for database service, session service, etc. 


### Client-side Caching
---
@todo

---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)
2. [GWA2 in Java](https://github.com/wadelau/GWA2/)

---

[Back to Top](/hanjst/hanjst-cache)

[Previous](./data-in-resource) ... [Next](./hanst-ready-to-go)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjkzMDU1OTc3LC00NTU3MjQxMywtMTIwOD
U4MzUwMywtODkyMTkzMDIzXX0=
-->