# UTF8 与 UTF8-BOM 的差异

UTF8-BOM编码的字符串比UTF8编码的字符串，多了前缀\xEF\xBF\xBD，肉眼是看不出来的，解析出来的字符串的长度也正常

比如使用 Encoding.Utf8.GetBytes("123456") 获取字节流

- UTF8-BOM编码为9位
- UTF8编码为6位

分别通过上面的字节流通过Encoding.Utf8.GetString()，得到的都是"123456"

但是：

以UTF8-BOM编码的字符串写库的时候（Oracle、MySql）都会出现异常
