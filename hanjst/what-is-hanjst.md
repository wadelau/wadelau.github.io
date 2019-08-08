
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
This is the Hanjst template language and engine.

Hanjst is intentionally designed to stop further "Reinventing the wheel" for HTML template engines though it sounds ridiculous.

"**汉吉斯特**" in Chinese.

### Why Hanjst?

It is easy to create another new template language and engine with JavaScript. therefore, there are too many JavaScript-based templates and corresponding engines for HTML.

Frankly speaking, the basic reason is that it is a simple and easy piece of work to make replaces work with a template and its engine which is designed to parse the template sentences into final representations.

To be complicated, the template language is a new design of expression language. The difficulty of designing a language is beyond imagination. The language must meet the needs of daily usage and high-frequency  communication. The first thing that language designers should consider is that the template language is universally accepted and widely used, so that the language has vitality. Undoubtedly, succinct and ideographic richness are important and priority considerations.

Unfortunately, there is no state of art work for this job prior to Hanjst.
 
 ![Mindmap of templates engines](http://ufqi.com/blog/wp-content/uploads/2018/12/TemplateLanguage_Engine_forWeb.201812.png)
 
 What we expect from a client-side template, i.e., JavaScript-based template, are three keys points:
 - Run in client-side, optional in server-side
 - Independent of back-end programming languages
 - As powerful as templates of back-end

Applying these criteria to all of exist JavaScript-based templates, however, it is hard to find one which meets all of these requirements.

Code snippets of a JavaScript-based template: 
```javascript
<script id="template" type="x-tmpl-mustache">
Hello {{ name }}!
</script>
```
Demerits or dislikes we find in these lines are:
- Block-based expressions
- Not streamlined mark-tags
- No Logic

 As fans of [Smarty,](//www.smarty.net) we would like to design and implement a whole newly-created JavaScript-based template language to cover all scenarios where Smarty has achieved.
 
However, it is NOT Smarty in JavaScript, which has been implemented and found in -GitHub, e.g. JSmarty or SmartyJS. What's more, both of them has not been enforced to act as Smarty in server-side.

From the point of view of [GWA2](/gwa2/index), we would need a template engine to work with all back-end programming languages, i.e., PHP, Java, Perl, Python, Aspx and so on.

That's to say, we cannot use Smarty for GWA2 in PHP and Velocity for GWA2 in Java.

There do have a few of template languages and engines which meet the desirable requirements, but there are all proprietary software sets and cannot be used in open source as GWA2.

Therefore, the searching space left for us is limited and an      
 
In the meantime,  bearing these features and functions in mind, the invented template and its engine, so-called Hanjst, has mertis as:

-   Hanjst's Run-time in client-side, reduce computing render in server-side;
    
-   Hanjst is Language-independent, not-bound with back-end scripts or languages;
    
-   Totally-isolated between MVC, data transfer with JSON;
    
-   Full-support template tags with built-in logic and customized JavaScript functions;
    
-   No more tags languages to be learned, just JavaScript;
    
-   ....

All in one, we believe that Hanjst would be the final JavaScript-based template language, and it has all functions which needed in client-side run-time. Also, any further "reinvent of the wheel" in this field would be meaningless. 

----
[Back to top](/hanjst/what-is-hanjst)

[Back to Up](/hanjst/index)
<!--stackedit_data:
eyJoaXN0b3J5IjpbODc2ODM1NjIxLDcxMjA2NTMwOSwtMjM0Mz
Y0NzQwLDUzNTE1MjIwMCwtODQxNTIyOTU4LDE1MjQwMjg4LC00
NzUyNjE4ODEsMTIwOTY3Nzg4NSw4MDIwODU4MzQsLTY5ODUwMT
g3NiwtOTMzMzA0NDMzXX0=
-->