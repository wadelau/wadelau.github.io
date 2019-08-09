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
--
>
>Hanjst aft parse copyright_year:2019
>

This marks Hanjst has successfully read JSON data and generated all global variables including one of the default tags, **copyright_year**. 
The **copyright_year** will be set dynamically to the current year.

>
>Hanjst sorted tpl sentence:[span {if \$user['feedback'] lt 3 } class="cls2" {else} {/if}] in Chrome-likes.
>

Hanjst allows embedded template sentences which can be mixed with a normal HTML element.
However it is error-prone that the confusions raised by the chars of < (less than) and > (greater than).
To figure it out, we designate "lt" (less than) to represent <, so as "gt" for >. 

>
>Hanjst includeScript:	if(1==1){.....
>

@todo

>
>Hanjst tpl2code:try{ var tpl2js = []; ...
>

@todo

>
>tplParse:&lt;style>...."
>

@todo

>Hanjst parse time                 cost: 0.017s

Hanjst records its cost time from the very beginning, then at the end of all work, the time elapsed will be figured out by the diff of these two points.

In the [demo page of Hanjst]([https://ufqi.com/dev/hanjst/](https://ufqi.com/dev/hanjst/)), the log shows that it has spent 0.017 second to parse all the template sentences, i.e., 17 milliseconds.

 It is clear and believable that the parse time should be less and less with the rapid growth of computing in client-side. Therefore, Hanjst follows adhere the trends of grid-computing or edge-computing.  


**2. Warnings**
--
> 
> additional original scripts before jsondata will be invoked twice.....Thu Aug 08 2019 12:37:00 GMT+0800 (China Standard Time)
> 

@todo

>
>Hanjst found embedded tpl sentence:[span {if="" $user['feedback']="" gt="" 4}="" class="cls2" {else}="" {="" if}=""] but compatible partially.
>

@todo

>
>Hanjst illegal tpl sentence:[if \$newslist[$k]['title'].length > 25 ] but compatible.
>

@todo

>
>Hanjst illegal tpl sentence:[foreach $newscontentlist as $page] but compatible.
>

Hanjst provides lots of compatible remedies for human misspelling or misused with the syntax or semantics.

Hanjst also strives to behave as Smarty and it can parse many template sentences which are being composed with Smarty syntax, such as the log shows in the above lines.

```html
{foreach $newsContentList as $news}
	{$news['title']}
{/foreach}
```
The lines will be translated into JavaScript codes as below.

```javascript
for(var $news in $newsContentList){
	$news['title'];
}
```
Similar compatible measures include **foreach**, **foreachelse**, **whileelse**. **forelse**. Because these keywords are not built-in keywords in pure JavaScript source codes.

These keywords and their usages will be discussed in detail in following sections. 


**3. Errors**
--
>
>Hanjst template code exec failed.
>
>{“stack”:”ReferenceError: \$myAds2 is not defined\n at eval (eval at renderTemplate (http://example.com/view/default/js/Hanjst.js?v=201906171103:468:15), :405:1)\n at renderTemplate (http://example.com//view/default/js/Hanjst.js?v=201906171103:468:39)\n at _callRender (http://example.com//view/default/js/Hanjst.js?v=201906171103:679:9)\n at http://example.com//view/default/js/Hanjst.js?v=201906171103:698:9\n at http://example.com//view/default/js/Hanjst.js?v=201906171103:701:3″,”message”:”\$myAds2 is not defined”}
>
>Line 404:
>
>Line 405: if( $myAds2[‘sadplace’]==’homepage_up_right’){
>
>Line 406: tpl2js.push(” <a href=\””);
>


When Hanjst encounters a syntax error, it throws a readable exception code description to form a traceable error report.

Based on these error message specific to the line number, the developers can find the error location and make corrections as fast as possible. As shown above, it is indicated that when the template engine performs parsing, it has been found that a variable such as $myAds2 which is undefined on line 405 is used without being initialized prior to being called, so an error is reported.

Attention! It is worthy to be noted! Hanjst turns on JavaScript's Strict mode, which doesn't allow undefined variables!

---
#### Related works
1. [Hanjst update blog: +readable error-reporting]([https://ufqi.com/blog/hanjst-error-reporting-innerloop-and-loadinglayer/](https://ufqi.com/blog/hanjst-error-reporting-innerloop-and-loadinglayer/))
2. [Hanjst in -GitHub]([https://github.com/wadelau/Hanjst](https://github.com/wadelau/Hanjst))


----
[Back to Top](/hanjst/hanjst-debug)

[Previous](./hanjst-config) ... [Next](./hanjst-syntax)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc4ODg1MzQwNiwtMTUyNjM5NzIyMCwtMT
A5ODUyNzkwOCwtNTY0MjgyNCwzOTk5NTg5MTAsLTEwMDQzNDQ2
MjYsMjE4NzAxOTU2LDc3NTgxNDkwXX0=
-->