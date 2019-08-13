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

//- inside Hanjst.readTemplate to enable cache
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
eyJoaXN0b3J5IjpbLTQ3MDM2ODczOSwtNDU1NzI0MTMsLTEyMD
g1ODM1MDMsLTg5MjE5MzAyM119
-->