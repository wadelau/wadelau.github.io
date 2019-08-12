# [Hanjst](/hanjst/index)
## Functions, Part-1
### Built-in Functions

As we listed in the previous section, there are so many built-in functions in JavaScript and Hanjst. Those various functions almost cover every single aspect of programming in template language.

Hanjst has the follow directive built-in functions which consists of basic methods and backbone of the template language and its engine.

**1. `{for}`**

The `{for}` `{forelse}` tag is used to create simple loops. `for` is also the reserved key word in JavaScript.

`{forelse}` is executed when the loop is not iterated.

Here is an example of `for`:

```html
{$myArr=[1,2,3]}

<ul>
{for $i in $myArr}
	<li>{$i}: {$myArr[$i]}</li>
{forelse}
	<li>No data.<li>
{/for}
</ul>
```
The template lines will output as below.

```html
<ul>
    <li>0: 1</li>
    <li>1: 2</li>
    <li>2: 3</li>
</ul>
```
Another example use `for` as `for` in pure JavaScript:

```html
<ul>
{for($i=0; $i<10; $i++)}
	<li>{$i}</li>
{/for}
</ul>
```
---

**2. `{foreach}`...`{foreachelse}`**

`{foreach}` is being introduced from Smarty or PHP due to that there is no such function in pure JavaScript.
`{foreach}` empowers the template in almost nearly in nature language. Here are the same example we showed above, but this time we rewrite it with `{foreach}`.

```html
{$myArr=[1,2,3]}

<ul>
{foreach $myArr as $i}
	<li>{$i}: {$myArr[$i]}</li>
{foreachelse}
	<li>No data.<li>
{/foreach}
</ul>
```
Another more complicated data structure is used to demonstrate its powerful expression.


```html
<!-- server-side work -->
{$newsList=[]}
{$newsList[0]=new Object()}
{$newsList[0]['id']=12}
{$newsList[0]['title']='News-Title-12'}
{$newsList[1]=new Object()}
{$newsList[1]['id']=34}
{$newsList[1]['title']='News-Title-34'}
<!-- server-side work, end -->

<ul>
{foreach $newsList as $p}
	<li>
	{foreach $newsList[$p] as $pd}
		<dt>{$pd}: {$newsList[$p][$pd]}</dt>
	{/foreach}
	</li>
{foreachelse}
	<li>No data.<li>
{/foreach}
</ul>
```

This template lines will output pure HTML lines as below.

```html
<!-- server-side work -->
<!-- server-side work, end -->
<ul>
	<li>
		<dt>id: 12</dt>
		<dt>title: News-Title-12</dt>
	</li>
	<li>
		<dt>id: 34</dt>
		<dt>title: News-Title-34</dt>
	</li>
</ul>
```
According to our statistics from projects, `{foreach}` is heavily-used than any other directive functions. Almost every page contains at least one `{foreach}` .


---

**3. `{if}`...`{else if}`...`{else}`**

`{if}` is very similar with `{if}` in pure JavaScript and both share the same qualifiers to server as comparing operators.

```html
{$title='Hello Wordl!'}
{$titleLength=$title.length()}

<p>
{if $titleLength > 50}
	{$titleLength} is greater than 50!
{else if $titleLength > 10}
	{$titleLength} is greater than 10!
{else}
	{$titleLength} is less than 10!
{/if}
</p>
```

The template lines will output as below.

```html
<p>
	12 is greater than 10!
</p>
```

Regarding to the comparing operator, `<` will be escaped as `lt` and `>` will be escaped into `gt`, so as `=` to `eq`.

Hanjst allows embedded template sentences which can be mixed with a normal HTML element.  
However it is error-prone that the confusions raised by the chars of < (less than) and > (greater than).  
To figure it out, we designate “lt” (less than) to represent <, so as “gt” for >. See [Hanjst Debugging](/hanjst/hanjst-debug) .

Let's show it in an example.

```html
{$user['feedback']=2}

<span {if $user['feedback'] lt 3} class="cls2"{else} class="cls3"{/if}>
	This is A SPAN with embedded Tpl sentence.
</span>
```
This template lines will yield an output as below.

```html
<span class="cls2">
	This is A SPAN with embedded Tpl sentence.
</span>
```

This feature mainly comes from the idea of some templates working only in server-side. And also it advances itself over most of other templates in client-side, i.e., JavaScript-based templates engines. 

---

**4. `{while}`...`{whileelse}`**

`{while}` is simple and easy to understand and to deploy in template lines.

Just a few lines of examples.

```html
{$i=0}

<ul>
{while $i<5}
	<li> line {$i} </li>
    {$i++}
{whileelse}
	<li>Out of While.</li>
{/while}
</ul>
```

The expected output will be shown as below.

```html
<ul>
	<li> line 0 </li>
	<li> line 1 </li>
	<li> line 2 </li>
	<li> line 3 </li>
	<li> line 4 </li>
</ul>
```

---

### Custom Functions

(To be continued...)

---

#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


----
[Back to Top](/hanjst/hanjst-function)

[Previous](./hanjst-variable) ... [Next](./hanjst-function-2)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbNjM2NTg2OTUzLC0xNzg0MDE1ODg3LC0xMD
kyMDUyOTQzLDE2NTk0NDE0OTYsNzIyNTY0NzAxLC00OTg5ODk5
OTcsLTEzMTcxNTg0MDYsLTEwNzcwODA5MjBdfQ==
-->