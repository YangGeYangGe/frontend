# html notes

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