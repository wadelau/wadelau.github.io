# [Hanjst](/hanjst/index)
## Hanjst Class
### Backend Overview
---
We have switched our default template engine from Smarty to Hanjst.

Smarty itself is good enough and strong enough to meet the requirements of the production environment, which is one of the reasons Smarty won in our candidates list before. Smarty's concise expression is very close to natural language, making it easy to learn and easy to use. Advanced applications of Smarty keep this simplicity, so the learning curve is not steep.

We have integrated Smarty in GWA2PHP and it works very well. When we have developed GWA2Java, we find that Smarty fans on the Internet had moved Smarty to the Java version, Smarty4J, so we also integrated Smarty4J consequently.

Unfortunately, Smarty4J is a version of about 7-8 years ago, and has not been updated since then, also it is only compatible with the syntax of Smarty 2, which heavily limits the further development of GWA2Java.

So we have committed to make this switch happen. Hanjst will be our default template engine in GWA2 ecosystem.

Regarding to backend or  server-side for Hanjst, it is only one task to do. The task in server-side is to output a group of key-value pairs in JSON format to client-side.

This preparation work of JSON can be split into two parts: one is to read all server-side data for business, and the other is to read other embedded template files and 

### Hanjst Class for Server-side
---
dddd



---

#### Related works

1. [Hanjst with GWA2 in Java](https://github.com/wadelau/GWA2/tree/master/java)
2. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)
3. [GWA2 switch from Smarty to Hanjst](https://ufqi.com/blog/gwa2-8-years-with-smarty-to-hanjst/)

---

[Back to Top](/hanjst/hanjst-function-class)

[Previous](./hanjst-function-2) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0NjI3NzQyNzEsMTcyMDU0NjQ5Nl19
-->