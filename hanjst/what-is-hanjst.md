
# [Hanjst](/hanjst/index)
## What is Hanjst and Why

### What is Hanjst?

![Hanjst Logo](http://ufqi.com/blog/wp-content/uploads/2019/06/hanjst-logo.201901.jpg)

Han JavaScript Template Language and Engine.

Hanjst is a template language aiming at present a page of Web contents.

Hanjst is a template engine which parses the pages written in Hanjst template language.

Han is the surname of my wife, and one of the given names of my daughter and son.

Han is also Chinese in Pinyin, Hànrén (汉人).

Design this template language and engine from the perspective of a linguist,
The procedural expression of grammar and semantics is realized by the engineer's thinking.

This is the Hanjst template language and engine from the jointly collaboration of linguists and computer engineers.

Hanjst is intentionally designed to stop further "Reinventing the wheel" for HTML template engines though it sounds ridiculous.

"**汉吉斯特**" in Chinese.

---
### Why Template?

A _`template engine`_ enables us to use static template files in an application. At runtime, the template engine replaces variables in a template file with actual values, and transforms the template into an final HTML.

MVC separation, see  [ASP.NET MVC Pattern](https://dotnet.microsoft.com/apps/aspnet/mvc) .

Clear and clean codes, see [Why would I use Smarty](https://www.smarty.net/why_use) .

---
### Why Hanjst?

It is easy to create another new template language and engine with JavaScript. therefore, there are too many JavaScript-based templates and corresponding engines for HTML.

Frankly speaking, the basic reason is that it is a simple and easy piece of work to make replaces work with a template and its engine which is designed to parse the template sentences into final representations.

To be complicated, the template language is a new design of expression language. The difficulty of designing a language is beyond imagination. The language must meet the needs of daily usage and high-frequency  communication. The first thing that language designers should consider is that the template language is universally accepted and widely used, so that the language has vitality. Undoubtedly, succinct and ideographic richness are important and priority considerations.

Unfortunately, there is no state of art work for this job prior to Hanjst.
 
 ![Mindmap of templates engines](http://ufqi.com/blog/wp-content/uploads/2018/12/TemplateLanguage_Engine_forWeb.201812.png)
 
Through the analysis of the brain map, we found that there are still two problems in this field that have not been solved, or are not well solved: 
 1) On the server side, is there a template language and engine that can be implemented cross-development languages? 
2) Client/browser terminal, is there a template language and engine that can do without script tags?
 
 What we expect from a client-side template, i.e., JavaScript-based template, are three keys points:
 - Run in client-side, optional in server-side
 - Independent of back-end programming languages
 - As powerful as templates of back-end

Applying these criteria to all of exist JavaScript-based templates, however, it is hard to find one which meets all of these requirements.

Code snippets of a JavaScript-based template: 
```javascript
<script id="template" type="x-tmpl-mustache">
Hello `{`{ name `}`}!
</script>
```
Demerits or dislikes we find in these lines are:
- Block-based expressions
- Not streamlined mark-tags
- No Logic

 As fans of [Smarty,](//www.smarty.net) we would like to design and implement a whole newly-created JavaScript-based template language to cover all scenarios where Smarty has achieved.
 
However, it is NOT Smarty in JavaScript, which has been implemented and found in -GitHub, e.g. JSmarty or SmartyJS. What's more, both of them has not been enforced to act as powerful as that of Smarty in server-side.

From the point of view of [GWA2](/gwa2/index), we would need a template engine to work with all back-end programming languages, i.e., PHP, Java, Perl, Python, Aspx and so on.

That's to say, we cannot use Smarty for GWA2 in PHP and Velocity for GWA2 in Java.

There do have a few of template languages and engines which meet the desirable requirements, but most of them are proprietary software sets and cannot be used in open source as GWA2.

Therefore, the searching space left for us is limited and an encouraged option is to create a new template language and engine.     
 
Combining all those considerations and  bearing expected features and functions in mind, the invented template and its engine, so-called Hanjst, has mertis as:

-   Hanjst's Run-time in client-side, reduce computing render in server-side;
    
-   Hanjst is Language-independent, not-bound with back-end scripts or languages;
    
-   Totally-isolated between MVC, data transfer with JSON;
    
-   Full-support template tags with built-in logic and customized JavaScript functions;
    
-   No more tags languages to be learned, just JavaScript;
    
-   ....

All in one, we believe that Hanjst would be the final JavaScript-based template language, and it has all functions which needed in client-side run-time. Also, any further "reinvent of the wheel" in this field would be meaningless. 

We have integrated Smarty in GWA2PHP and it works very well before. When we have developed GWA2Java, we find that Smarty fans on the Internet had moved Smarty to the Java version, Smarty4J, so we also integrated Smarty4J consequently.

Unfortunately, Smarty4J is a version of about 7-8 years ago, and has not been updated since then, also it is only compatible with the syntax of Smarty 2, which heavily limits the further development of GWA2Java.

So we have committed to make this switch happen. Hanjst will be our default template engine in GWA2 ecosystem since then.

---
#### Related works
1. [Hanjst Homepage](https://ufqi.com/dev/hanjst/)
1. [Hanjst first release blog.](https://ufqi.com/blog/hello-2019-hanjst-init/)
2. [GWA2's default template switch from Smarty to Hanjst.](https://ufqi.com/blog/gwa2-8-years-with-smarty-to-hanjst/)

----
[Back to top](/hanjst/what-is-hanjst)

[Previous](./index) ... [Next](./hanjst-install)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTkxMTc1MTAyNSwxMjA4NzY2OTc2LDE5Mz
czNjU1OTcsLTEwNjAwMzU0NzQsLTc0OTY3NzExNywtMTgwMTY1
MzI0MSwtNDYxMzk4MDQxLDE4MzUyMjcwMTAsNzEyMDY1MzA5LC
0yMzQzNjQ3NDAsNTM1MTUyMjAwLC04NDE1MjI5NTgsMTUyNDAy
ODgsLTQ3NTI2MTg4MSwxMjA5Njc3ODg1LDgwMjA4NTgzNCwtNj
k4NTAxODc2LC05MzMzMDQ0MzNdfQ==
-->