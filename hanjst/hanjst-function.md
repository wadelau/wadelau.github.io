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
	<li>{$i}
{/for}
```

3. {foreach}...{foreachelse}
4. {if}...{else if}...{else}
5. {while}...{whileelse}


### Custom Functions
....


#### Related works

1. [Hanjst Demo Page](https://ufqi.com/dev/hanjst/)


----
[Back to Top](/hanjst/hanjst-function)

[Previous](./hanjst-variable) ... [Next](./)

[Back to Up](/hanjst/index)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1ODg2MzM5NiwtMTA3NzA4MDkyMF19
-->