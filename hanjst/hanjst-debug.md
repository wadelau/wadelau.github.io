# [Hanjst](/hanjst/index)
## Hanjst Debugging
### IsDebug Directive
Hanjst has a debug mode.
To enable the debug mode, just set "IsDebug=true" before invoking the main template parsing engine.

```javascript
<script type="text/javascript" async>
    window.Hanjst = {'JsonDataId':'Hanjstjsondata', 
	    'IsDebug': true}; // optional
</script>
```

The template parse engine will output verbose message in current browser's console log or via window.alert.
Be careful，debug mode will consume extra computing 
 

### Debugging Output


---
#### Related works
1. [Hanjst in -GitHub]([https://github.com/wadelau/Hanjst](https://github.com/wadelau/Hanjst))


----
[Back to Top](/hanjst/hanjst-debug)

[Previous](./hanjst-config) ... [Next](./)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMjgxNzA5OV19
-->