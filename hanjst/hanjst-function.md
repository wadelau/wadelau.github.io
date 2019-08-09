# [Hanjst](/hanjst/index)
## Functions, Part-1
### Built-in Functions

As we listed in previous section, there are so many built-in functions in JavaScript and Hanjst. Those various functions almost cover every single aspect of programming in template language.

Hanjst has the follow directive built-in functions which consists of basic methods and backbone of the template language and its engine.

1. `{for}`

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

2. `{foreach}`...`{foreachelse}`

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
{$newsList=[]}
{$newsList[0]=new Object()}
{$newsList[0]['id']=12}
{$newsList[0]['title']='News-Title-12'}
{$newsList[1]=new Object()}
{$newsList[1]['id']=34}
{$newsList[1]['title']='News-Title-34'}
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
<ul>
	<li>
		<dt>id: 12</dt>			<dt>title: News-Title-12</dt>		</li>	<li>			<dt>id: 34</dt>			<dt>title: News-Title-34</dt>		</li></ul>
```

---

3. `{if}`...`{else if}`...`{else}`



4. `{while}`...`{whileelse}`


### Custom Functions
....


#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


----
[Back to Top](/hanjst/hanjst-function)

[Previous](./hanjst-variable) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjEzMjA4NTY2NiwtMTMxNzE1ODQwNiwtMT
A3NzA4MDkyMF19
-->