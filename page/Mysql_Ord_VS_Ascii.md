# Mysql中ord()和ascii()函数的区别

## 前言

我们都知道，mysql中 ord(), ascii()函数都是返回字符串第一个字符的编码值，
但是他们有什么区别呢？

## 解释

### ASCII(str1)

返回字符串str的最左面字符的ASCII代码值。如果str是空字符串，返回0。如果str是NULL，返回NULL

举例：

1. 简单举例

```
mysql> select ascii('hi');

+————-+
| ascii('hi') |
+————-+
|         104 |
+————-+

1 row in set
```

104是h的ASCII值

2. 如果汉字又如何呢？

```
mysql> SELECT ASCII('简明现代魔法');

+-----------------------------+
| ASCII('简明现代魔法')       |
+-----------------------------+
|                         231 |
+-----------------------------+
1 row in set
```

再来看一个汉字的情况

```
mysql> SELECT ASCII('简');

+--------------+
| ASCII('简')  |
+--------------+
|          231 |
+--------------+
1 row in set
```

下面再看看ord()函数在同样例子的运行情况

### ORD() 函数

ORD() 函数返回字符串第一个字符的ASCII 值。

语法： ORD(string)

举例：

1. 简单例子

```
mysql> SELECT ORD('NowaMagic');

+------------------+
| ORD('NowaMagic') |
+------------------+
|               78 |
+------------------+

1 row in set
```

2. 如果汉字又如何呢？

```
mysql> SELECT ORD('简明现代魔法');

+---------------------+
| ORD('简明现代魔法') |
+---------------------+
|            15183488 |
+---------------------+

1 row in set
```

再来看一个汉字的情况

```
mysql> SELECT ORD('简');

+-----------+
| ORD('简') |
+-----------+
|  15183488 |
+-----------+

1 row in set
```

为什么会有 8 位数那么长呢？原因是数据库使用的字符集问题，此处的数据库使用的是 UTF-8，16位表示一个符号。

下面是各种编码的字符长度：

```
mysql> SHOW CHARACTER SET;

+----------+-----------------------------+---------------------+--------+
| Charset  | Description                 | Default collation   | Maxlen |
+----------+-----------------------------+---------------------+--------+
| big5     | Big5 Traditional Chinese    | big5_chinese_ci     |      2 |
| dec8     | DEC West European           | dec8_swedish_ci     |      1 |
| cp850    | DOS West European           | cp850_general_ci    |      1 |
| hp8      | HP West European            | hp8_english_ci      |      1 |
| koi8r    | KOI8-R Relcom Russian       | koi8r_general_ci    |      1 |
| latin1   | cp1252 West European        | latin1_swedish_ci   |      1 |
| latin2   | ISO 8859-2 Central European | latin2_general_ci   |      1 |
| swe7     | 7bit Swedish                | swe7_swedish_ci     |      1 |
| ascii    | US ASCII                    | ascii_general_ci    |      1 |
| ujis     | EUC-JP Japanese             | ujis_japanese_ci    |      3 |
| sjis     | Shift-JIS Japanese          | sjis_japanese_ci    |      2 |
| hebrew   | ISO 8859-8 Hebrew           | hebrew_general_ci   |      1 |
| tis620   | TIS620 Thai                 | tis620_thai_ci      |      1 |
| euckr    | EUC-KR Korean               | euckr_korean_ci     |      2 |
| koi8u    | KOI8-U Ukrainian            | koi8u_general_ci    |      1 |
| gb2312   | GB2312 Simplified Chinese   | gb2312_chinese_ci   |      2 |
| greek    | ISO 8859-7 Greek            | greek_general_ci    |      1 |
| cp1250   | Windows Central European    | cp1250_general_ci   |      1 |
| gbk      | GBK Simplified Chinese      | gbk_chinese_ci      |      2 |
| latin5   | ISO 8859-9 Turkish          | latin5_turkish_ci   |      1 |
| armscii8 | ARMSCII-8 Armenian          | armscii8_general_ci |      1 |
| utf8     | UTF-8 Unicode               | utf8_general_ci     |      3 |
| ucs2     | UCS-2 Unicode               | ucs2_general_ci     |      2 |
| cp866    | DOS Russian                 | cp866_general_ci    |      1 |
| keybcs2  | DOS Kamenicky Czech-Slovak  | keybcs2_general_ci  |      1 |
| macce    | Mac Central European        | macce_general_ci    |      1 |
| macroman | Mac West European           | macroman_general_ci |      1 |
| cp852    | DOS Central European        | cp852_general_ci    |      1 |
| latin7   | ISO 8859-13 Baltic          | latin7_general_ci   |      1 |
| utf8mb4  | UTF-8 Unicode               | utf8mb4_general_ci  |      4 |
| cp1251   | Windows Cyrillic            | cp1251_general_ci   |      1 |
| utf16    | UTF-16 Unicode              | utf16_general_ci    |      4 |
| cp1256   | Windows Arabic              | cp1256_general_ci   |      1 |
| cp1257   | Windows Baltic              | cp1257_general_ci   |      1 |
| utf32    | UTF-32 Unicode              | utf32_general_ci    |      4 |
| binary   | Binary pseudo charset       | binary              |      1 |
| geostd8  | GEOSTD8 Georgian            | geostd8_general_ci  |      1 |
| cp932    | SJIS for Windows Japanese   | cp932_japanese_ci   |      2 |
| eucjpms  | UJIS for Windows Japanese   | eucjpms_japanese_ci |      3 |
+----------+-----------------------------+---------------------+--------+

39 rows in set
```

### 总结

Mysql中 ascii()函数用来获取字符串的第一个字节，并以ascii形式(0-255)给出，
而ord()函数则是会给出字符串的第一个字符（不同编码一个字符所占字节长度不同）。
如果在ascii字符集上，则ascii()与ord()等效。
