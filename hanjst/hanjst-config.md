# [Hanjst](/hanjst/index)
## Hanjst Configurations
### Runtime Settings

Except from what we have introduced in previous section, there are some other variables which can be set as custom values.

```javascript
window.HanjstDefault = {
	//- variables from response starting with this, e.g. $pageTitle
	"TplVarTag": "$", 
	
	//- an html element id which holds server response json data
	"JsonDataId": "Hanjstjsondata", 
	
	//- inner usage
	"LogTag": "Hanjst", 
	
	//- inner usage
	"ParseTag": "__JSTPL__", 
	
	//- verbose output in console 
	"IsDebug": false, 
};
```
Keys listed in above can be set in window.Hanjst before the main source file, i.e., Hanjst.js .

However it is highly-recommended to keep them untouched due to unexpected or unknown warnings or errors.


### Available Variables

Hanjst provides a few environmental values via this keys:

`$copyright_year` : current year's value in four digits, e.g. 2020

`$time_stamp` : current time stamp since 1970, in millisecond.


---
#### Related works
1. [Hanjst in -GitHub]([https://github.com/wadelau/Hanjst](https://github.com/wadelau/Hanjst))


----
[Back to Top](/hanjst/hanjst-config)

[Previous](./hanjst-install) ... [Next](./hanjst-debug)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM4MjM5MTY0MywtMTc4OTkzMzI1MSwyMT
I1MTM2MDQxXX0=
-->
