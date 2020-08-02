# html notes basic

## 1. 在vscode中，新建一个html文件，输入!后，选择第一个可以自动生成以下代码

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

## 2. html 格式详解

标签名|定义|说明
--|:--:|--
```<html></html>```|HTML标签|页面中最大的标签，我们成为根标签
```<head></head>```|文档的头部|注意在head标签中我们必须要设置的标签是title
```<titile></titile>```|文档的标题|让页面拥有一个属于自己的网页标题
```<body></body>```|文档的主体|元素包含文档的所有内容，页面内容 基本都是放到body里面的

## 3. 文档声明头
任何一个标准的HTML页面，第一行一定是一个以```<!DOCTYPE ...>```开头的语句。文档声明头，DocTypeDelcaration, 简称DTD

DTD可告知浏览器文档使用哪种HTML或XHTML规范

## 4. 页面语言 lan
指定页面的语言类型

```
<html lang="en">
```
- en：定义页面语言为英语。
- zh-CN：定义页面语言为中文。

## 5. 头标签 head
面试题：
- 问：网页的head标签里面，表示的是页面的配置，有什么配置？
- 答：字符集，关键词，页面描述，页面标题，IE适配，视口，iPhone小图标等等。
  
头标签内部常见标签如下：
- ```<title>```:制定整个网页的标题，在浏览器最上方显示。
- ```<base>```:为页面上的所有链接规定默认地址或默认目标
- ```<meta>```：提供有关页面的基本信息
- ```<body>```: 用于定义HTML文档所要显示的内容，也成为了主题标签。我们所写的代码必须放在此标签内。
- ```<link>```：定义文档与外部资源的关系。
#### meta标签
```
<meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
```
#### （1）字符集 charset
字符集用meta标签中的charset定义，charset就是charactor set（即“字符集”），即网页的编码方式。

上面这行代码非常关键， 是必须要写的代码，否则可能导致乱码。比如你保存的时候，meta写的和声明的不匹配，那么浏览器就是乱码。

utf-8是目前最常用的字符集编码方式，常用的字符集编码方式还有gbk和gb2312等。

#### （2）视口 viewport：
```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
width=device-width ：表示视口宽度等于屏幕宽度。

#### (3) 定义“关键词”

```
<meta name="Keywords" content="网易,邮箱,游戏,新闻,体育,娱乐,女性,亚运,论坛,短信" />
```
这些关键词，就是告诉搜索引擎，这个网页是干嘛的，能够提高搜索命中率。让别人能够找到你，搜索到你。

#### (4)定义“页面描述”

meta除了可以设置字符集，还可以设置关键字和页面描述。

只要设置Description页面描述，那么百度搜索结果，就能够显示这些语句，这个技术叫做SEO（search engine optimization，搜索引擎优化）。

```
<meta name="Description" content="网易是中国领先的互联网技术公司，为用户提供免费邮箱、游戏、搜索引擎服务，开设新闻、娱乐、体育等30多个内容频道，及博客、视频、论坛等互动交流，网聚人的力量。" />
```

上面的几种```<meta>```标签都不用记，但是另外还有一个```<meta>```标签是需要记住的：

```
<meta http-equiv="refresh" content="3;http://www.baidu.com">
```
上面这个标签的意思是说，3秒之后，自动跳转到百度页面。

**title标签**
用于设置网页的标题
title也有助于SEO搜索引擎优化

**base标签**
```
<base href="/">
```
base 标签用于指定基础的路径。指定之后，所有的 a 链接都是以这个路径为基准。

## 6. body 标签

```
<body>标签的属性有：
bgcolor：设置整个网页的背景颜色。
background：设置整个网页的背景图片。
text：设置网页中的文本颜色。
leftmargin：网页的左边距。IE浏览器默认是8个像素。
topmargin：网页的上边距。
rightmargin：网页的右边距。
bottommargin：网页的下边距。
```

```
<body link="read" alink="blue" vlink="green">

</body>

link表示默认显示的颜色
alink表示鼠标点击但还没松开时的颜色
vlin表示点击完成之后显示的颜色
```
---
## 字符集
中文能够使用的字符集
1. UTF-8
2. GBK
   
字库规模：UTF-8 > gb2312
我们用meta标签声明的当前这个html文档的字库，一定要和保存的文件编码类型一样，否则乱码（重点）。

拿 sublime编辑器举例，当我们不设置的时候，sublime默认类型就是UTF-8。而一旦更改为gb2312的时候，就一定要记得设置一下sublime的保存类型： 文件→ set File Encoding to → Chinese Simplified(GBK)。VS Code 的道理一样。

保存大小：UTF-8（更臃肿、加载更慢） > gb2312 （更小巧，加载更快）

总结：

UTF-8：字多，有各种国家的语言，但是保存尺寸大，文件臃肿；
gb2312：字少，只用中文和少数外语和符号，但是尺寸小，文件小巧。