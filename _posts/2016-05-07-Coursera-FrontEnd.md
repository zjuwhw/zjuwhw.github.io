---
layout: post
title:  "Coursera-Frontend学习笔记"
date:   2016-05-07
tags: [cs, mooc]
---
注：本文为Front-End技术HTML，CSS和JavaScript的学习笔记，内容来自Coursera课程[《HTML, CSS, and JavaScript for Web Developers》](https://www.coursera.org/learn/html-css-javascript-for-web-developers/)

## CSS
```
p {
	color: blue;
}
```
- `p` is Selector
- 'color: blue;' is Declaration
- 'color' is Property
- 'blue' is Value

```
/* element selector */
p {
	color: blue;
	text-align: center;
	font-size: 20px;
	font-weight: bold;
	font-style: italic;
	background-color: green;
	opacity: .6;
}


/* class selector */
.blue {
	color: blue;
}

<p class = "blue"> ... </p>
<div class = "blue"> ... </div>


/* id selector */
#name {
	color: blue;
}

<p id = "name"> ... </p>

/* grouping selectors */
div, .blue {
	color: blue;
}
```
combing selectors

```
/* element with class selector */
p.big {
	font-size: 20px;
}

<p class = "big"> ... </p>


/* child selector */
article > p {
	color: blue;
}

<article>
	<p>  ... </p>
</article>


/* Descendant selector */
article p {
	color: blue;
}

<article>
	<div><p> ... </p></div>
</article>
```
