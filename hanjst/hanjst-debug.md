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

**1. Information**
>Hanjst aft parse copyright_year:2019

This marks Hanjst has successfully read JSON data and generated all global variables including one of the default tags, **copyright_year**. 
The copyright_year will be set dynamically to the current year.

>Hanjst sorted tpl sentence:[span {if \$user['feedback'] lt 3 } class="cls2" {else} {/if}] in Chrome-likes.

Hanjst allows embedded template sentences which can be mixed with a normal HTML element.
However it is error-prone that the confusions raised by the chars of < (less than) and > (greater than).
To figure it out, we designate "lt" (less than) to represent <, so as "gt" for >. 

>Hanjst includeScript:	if(1==1){.....

dd
>Hanjst tpl2code:try{ var tpl2js = []; ...

dd
>tplParse:&lt;style>...."

dd
>Hanjst parse time                 cost: 0.017s

dd


**2. Warnings**
> additional original scripts before jsondata will be invoked twice.....Thu Aug 08 2019 12:37:00 GMT+0800 (China Standard Time)

>Hanjst found embedded tpl sentence:[span {if="" $user['feedback']="" gt="" 4}="" class="cls2" {else}="" {="" if}=""] but compatible partially.

>Hanjst illegal tpl sentence:[if \$newslist[$k]['title'].length > 25 ] but compatible.

>Hanjst illegal tpl sentence:[foreach $newscontentlist as $page] but compatible.



**3. Errors**
>Hanjst template code exec failed.
>{“stack”:”ReferenceError: \$myAds2 is not defined\n at eval (eval at renderTemplate (http://example.com/view/default/js/Hanjst.js?v=201906171103:468:15), :405:1)\n at renderTemplate (http://example.com//view/default/js/Hanjst.js?v=201906171103:468:39)\n at _callRender (http://example.com//view/default/js/Hanjst.js?v=201906171103:679:9)\n at http://example.com//view/default/js/Hanjst.js?v=201906171103:698:9\n at http://example.com//view/default/js/Hanjst.js?v=201906171103:701:3″,”message”:”\$myAds2 is not defined”}
>Line 404:
>Line 405: if( $myAds2[‘sadplace’]==’homepage_up_right’){
>Line 406: tpl2js.push(” <a href=\””);

...

---
#### Related works
1. [Hanjst update blog: +readable error-reporting]([https://ufqi.com/blog/hanjst-error-reporting-innerloop-and-loadinglayer/](https://ufqi.com/blog/hanjst-error-reporting-innerloop-and-loadinglayer/))
2. [Hanjst in -GitHub]([https://github.com/wadelau/Hanjst](https://github.com/wadelau/Hanjst))


----
[Back to Top](/hanjst/hanjst-debug)

[Previous](./hanjst-config) ... [Next](./)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzc1ODE0OTBdfQ==
-->