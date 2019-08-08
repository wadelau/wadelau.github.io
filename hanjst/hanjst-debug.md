# [Hanjst](/hanjst/index)
## Hanjst Debugging
### IsDebug Directive
Hanjst has a debug mode.
To enable the debug mode, just set "IsDebug=true" before invoking the main template parsing engine.

```javascript
<script type="text/javascript" async>
    window.Hanjst = {'JsonDataId':'Hanjstjsondata', 
	    'IsDebug': true}; // for develop and debug only
</script>
```

The template parse engine will output verbose message in current browser's console log or via window.alert.
Be careful，debug mode will consume extra computing resources and it should be set to false in production environment.
 
### Debugging Output
There are a few of type of log messages. Basically, information, warnings and errors.

1. Information
>Hanjst aft parse copyright_year:2019

>Hanjst sorted tpl sentence:[span {if $user['feedback'] lt 3 } class="cls2" {else} {/if}] in Chrome-likes.

>Hanjst includeScript:	if(1==1){.....


2. Warnings
> additional original scripts before jsondata will be invoked twice.....Thu Aug 08 2019 12:37:00 GMT+0800 (China Standard Time)

>Hanjst found embedded tpl sentence:[span {if="" $user['feedback']="" gt="" 4}="" class="cls2" {else}="" {="" if}=""] but compatible partially.

>Hanjst illegal tpl sentence:[if $newslist[$k]['title'].length > 25 ] but compatible.

3. Errors


---
#### Related works
1. [Hanjst in -GitHub]([https://github.com/wadelau/Hanjst](https://github.com/wadelau/Hanjst))


----
[Back to Top](/hanjst/hanjst-debug)

[Previous](./hanjst-config) ... [Next](./)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2NDU3NzQxNjBdfQ==
-->