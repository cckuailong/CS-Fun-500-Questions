# X-Forwarded-For 和它的兄弟们

## 解释

### X-Forwarded-For

X-Forwarded-For 是一个扩展头。HTTP/1.1（RFC 2616）协议并没有对它的定义，它最开始是由 Squid 这个缓存代理软件引入，用来表示 HTTP 请求端真实 IP，现在已经成为事实上的标准，被各大 HTTP 代理、负载均衡等转发服务广泛使用，并被写入 RFC 7239（Forwarded HTTP Extension）标准之中

X-Forwarded-For请求头格式非常简单

```
X-Forwarded-For:client, proxy1, proxy2
```

可以看到，XFF 的内容由「英文逗号 + 空格」隔开的多个部分组成，最开始的是离服务端最远的设备 IP，然后是每一级代理设备的 IP。

如果一个 HTTP 请求到达服务器之前，经过了三个代理 Proxy1、Proxy2、Proxy3，IP 分别为 IP1、IP2、IP3，用户真实 IP 为 IP0，那么按照 XFF 标准，服务端最终会收到以下信息：

```
X-Forwarded-For: IP0, IP1, IP2
```

### remoteAddress

是nginx与客户端进行TCP连接过程中，获得的客户端真实地址. Remote Address 无法伪造，因为建立 TCP 连接需要三次握手，如果伪造了源 IP，无法建立 TCP 连接，更不会有后面的 HTTP 请求。

不同语言获取 Remote Address 的方式不一样，例如 php 是 $_SERVER["REMOTE_ADDR"]，Node.js 是 req.connection.remoteAddress，但原理都一样。

### X-Real-IP

是一个自定义头。X-Real-Ip 通常被 HTTP 代理用来表示与它产生 TCP 连接的设备 IP，这个设备可能是其他代理，也可能是真正的请求端。需要注意的是，X-Real-Ip 目前并不属于任何标准，代理和 Web 应用之间可以约定用任何自定义头来传递这个信息

## 结论

对于 Web 应用来说，X-Forwarded-For 和 X-Real-IP 就是两个普通的请求头，自然就不做任何处理原样输出了。这说明，对于直连部署方式，除了从 TCP 连接中得到的 Remote Address 之外，请求头中携带的 IP 信息都不能信。
