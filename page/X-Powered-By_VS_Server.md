# Http header 中的 X-Powered-By 和 Server

## 解释

### Server

Server 首部包含了处理请求的源头服务器所用到的软件相关信息。 应该避免使用过长或者过于详细的描述作为 Server 的值，因为这有可能泄露服务器的内部实现细节，有利于攻击者找到或者探测服务器信息。

示例

```
Server: Apache/2.4.23 (Win32) OpenSSL/1.0.2j PHP/5.5.38
```

### X-Powered-By

X-Powered-By 是常见的非标准 Http响应头（大多数以 X-开头的都是非标准的头）。这个值的意义用于告知网站是用何种语言或框架编写的。

示例

```
X-Powered-By: PHP/5.2.1
```

## 隐藏响应的Server, X-Powered-By

### 隐藏 X-Powered-By

- 隐藏X-Powered-By

修改 php.ini 文件 设置 expose_php = Off

### 隐藏 Server

- apache 隐藏 server

修改httpd.conf 设置

```
ServerSignature Off
ServerTokens Prod
```

- nginx 隐藏 server

修改nginx.conf  在http里面设置

```
server_tokens off;
```

## 注

服务器除了可以将其返回信息关闭，也可以故意返回错误的信息，对攻击者进行误导。
