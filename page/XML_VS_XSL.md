# XML 和 XSL区别

## XML=可扩展标记语言(eXtensible Markup Language)

可扩展标记语言XML是一种简单的数据存储语言，使用一系列简单的标记描述数据，
而这些标记可用方便的方式建立，虽然 XML 占用的空间比二进制数据要占用更多的空间，
但XML极其简单易于掌握和使用 XML 的简单使其易于在任何应用程序中读写数据，
这使XML很快成为数据交换的唯一公共语言，XML不是一个依附于特定浏览器的语言。

例：

```
<?xml version="1.0"?>
<note
xmlns="http://www.w3school.com.cn" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.w3school.com.cn note.xsd">
    <to>George</to>
    <from>John</from>
    <heading>Reminder</heading>
    <body>Don't forget the meeting!</body>
</note>
```

## XSL=可扩展样式表语言 (EXtensible Stylesheet Language)
XSL 之于 XML ,就像 CSS 之于 HTML。它是指可扩展样式表语言 (EXtensible Stylesheet Language)。
这是一种用于以可读格式呈现 XML 数据的语言。
