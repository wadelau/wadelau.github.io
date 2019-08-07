
# [Hanjst](/hanjst/index)
## What is Hanjst and Why

### What is Hanjst?

![Hanjst Logo](http://ufqi.com/blog/wp-content/uploads/2019/06/hanjst-logo.201901.jpg)

Han JavaScript Template Language and Engine.

Hanjst is a template language aiming at present a page of Web contents.

Hanjst is a template engine which parse the pages written in Hanjst template language.

Han is the surname of my wife, and one of the given names of my daughter and son.

Han is also Chinese in Pinyin, Hànrén (汉人).

Hanjst is intentionally designed to stop further "Reinventing the wheel" for HTML template engines though it sounds ridiculous.

### Why Hanjst?

It is easy to create another new template language and engine with JavaScript. therefore, there are too many JavaScript-based templates and corresponding engines for HTML.

Frankly speaking, the basic reason is that it is a simple and easy piece of work to make replaces work with a template and its engine which is designed to parse the template sentences into final representations.

Unfortunately, there is no state of art work for this job prior to Hanjst.
 
 ![Mindmap of templates engines](http://ufqi.com/blog/wp-content/uploads/2018/12/TemplateLanguage_Engine_forWeb.201812.png)
 
 What we expect for a client-side template, i.e., JavaScript-based template, are three keys points:
 - Run in client-side, optional in server-side
 - Independent of back-end programming languages
 - As powerful as templates of back-end

Applying these criteria to all of exist JavaScript-based templates, however, it is hard to find one which meets all of these requirements.

 As a fan of [Smarty,](//www.smarty.net) we would like to design and implement a whole newly-created JavaScript-based template language to cover all scenarios where Smarty has achieved.
 
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
eyJoaXN0b3J5IjpbMTIwOTY3Nzg4NSw4MDIwODU4MzQsLTY5OD
UwMTg3NiwtOTMzMzA0NDMzXX0=
-->