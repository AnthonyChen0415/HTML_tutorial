# HTML学习记录

标签（空格分隔）： HTML 前端入门 CSS

---

按照网站的进度： HTML - XHTML - HTML5 - CSS - CSS3 - TCP/IP

# HTML
## - Hyper Text Markup Language
超文本标记语言，非编程语言
用标记来描述网页，类似我现在使用的MarkDown语言

---

## - HTML tag
成对出现，尖括号包围的关键词
`<html>` `<b> </b>`
```
<html> 与 </html> 之间的文本描述网页
<body> 与 </body> 之间的文本是可见的页面内容
<h1> 与 </h1>     之间的文本被显示为标题
<p> 与 </p>       之间的文本被显示为段落
```
---

## - 使用工具： Notepad++ 或 Atom
可存为 `.htm` `.html`

---

## - 标题，段落，超链接，图像，空元素， 水平线
* HTML标题由 `<h1> - <h6>` 定义
>请确保将 HTML heading标签只用于标题。不要仅仅是为了产生粗体或大号的文本而使用标题。
>注释：浏览器会自动地在标题的前后添加空行。
>注释：默认情况下，HTML会自动地在块级元素前后添加一个额外的空行，比如段落、标题元素前后。

* HTML段落是通过 `<p>` 来定义的，不存在顺序
> 使用空的段落标记 `<p></p>` 去插入一个空行是个坏习惯。用 `<br />` 标签代替它！

* HTML超链接是通过`<a>`来定义的
`<a href="http://www.w3school.com.cn">This is a link</a>`
> http:// 不能缺少，可以使用空链接

* HTML图像是通过`<img>`来定义的
`<img src="w3school.jpg" width="104" height="142" />`
> 宽和高是属性

* 空元素：`<br>` or `<br />`

* 水平线: `<hr />`
* 
---

## HTML标签的属性

> 属性必须以名称/值成对出现   `name = "value" ` ,属性值必须在引号内
> 属性必须在开始标签定义
> 

``` html
<body bgcolor = "yellow">
  <h1 align = "center"> First heading </h1>
  <h2 align = "right"> First heading h2 </h2>
</body>
```

---

## HTML注释
` <!-- This is a comment --> `

>对于 HTML，您无法通过在 HTML代码中添加额外的空格或换行来改变输出的效果。
>当显示页面时，浏览器会移除源代码中多余的空格和空行。所有连续的空格或空行都会被算作一个空格。需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格。

---

## HTML样式
通过定义`style`属性，对元素进行颜色，字体等的调整
```
<h1 style="text-align:center">This is a heading</h1>
<p style="font-family:times;color:green">This text is in Times and green</p>
<p style="font-size:30px">This text is 30 pixels high</p>

```

---

## 文本样式操作
```
<b> This is bold!  </b>
```


tag    |作用       
:---:|:---:
`<b> </b>` | <b> bold </b>
`<i> </i>` | <i> italic  </i>
`<strong> </strong>` | <strong> strong </strong>
`<em> </em> `| <em> emphasized </em>
`<small> </small>` | <small> small </small>
`<large> </large>` | <large> large </large>
`<sub> </sub>`  | This text contains<sub>subscript</sub>
`<sup> </sup>`  | This text contains<sup>superscript</sup>
`<var> </var>`   |  数学元素
`<pre> </pre>`  | 保留了空格和换行
`<code>, <kbd>, <tt>, <samp>, <var>`| 用于显示计算机代码
`<del> </del>`  | <del> deleted </del>
`<ins> </ins>`  | 下划线
`<address> </address>` | 地址
`<bdo dir="rtl"> </bdo>`  bi-directional override| 从右向左输出
`<q>  </q>`  |  <q> 短引用 </q>
`<blockquote> </blockquote>` |  段落引用
`<abbr title="xxx">xxx</abbr> ` | 缩略词
`<cite> </cite>`| <cite>著作标题</cite>


---
## 样式表
使用**外部样式表**，可以通过修改外部文件直接修改页面样式
```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```
使用**内部样式表**，通过`head`部分里的`<style>`标签来定义页面样式
``` html
<head>
<style type="text/css">
body {background-color: red}
p {margin-left: 20px}
</style>
</head>
```
使用**内联样式**， 通过`style`属性对个别部件进行样式定义
```
<p style="color: red; margin-left: 20px">
This is a paragraph
</p>
```
---
### html超链接
```
#  样式
<a href = "url"> Link text </a>

#  target属性
** _blank 会打开一个新窗口
<a href = "url" target = "_blank">  Link text </a>

#  name属性--> anchor 标签超链接
<a name = "label">  Text  </a>    # 创建一个标签
<a href = "#label">  Text </a>    # 指向“label”标签

#  mailto 属性:   %20 用于代指单词中的空格
<a href= "mailto: xxxx@xxx.com"> Link text </a>
<a href= "mailto: xxx@xxx.com?subject = Biao%20Ti"> Link text </a>
```
---
### html图像
```
<img src="/i/ct_netscape.jpg" width = "100" height = "100"/>
<img src="http://www.w3school.com.cn/i/w3school_logo_white.gif" width = "100" height = "100" />
<p> 图像在文本中<img src= "url" align ="center/bottom/top" /> 如何对齐</p>
# 把图像作为超链接使用
<a href = "url"> 
<img src = "url" />
</a>
```
**将图片进行区域分割，分别作为不同的超链接**
```
<img src = "url" usemap = "# name " />

<map name = "name" id = "name">
<area 
shape = "circle/rect"
coords = "xxx,yyy,radius"/ "xxx1,yyy1,xxx2,yyy2"
href = "url"
target = "_blank"
alt = "alternative text" />
</map>

```

---

### html 表格

```
# 表格以 <table>  </table> 开始
# 每行以 <tr> </tr> 开始
# 每行的每一个元素用 <td> </td>
<table border = "1">
<tr>
<td> 元素1 </td>   <td> 元素2  </td>
</tr>
</table>
```

---

### html 列表
#### 无序列表(disc/circle/square三种类型)
<ul type = "circle">
<li> 元素1 </li>
<li> 元素2 </li>
</ul>
#### 有序列表
<ol>
<li> 元素1 </li>
<li> 元素2 </li>
</ol>

---

### <div> <span>