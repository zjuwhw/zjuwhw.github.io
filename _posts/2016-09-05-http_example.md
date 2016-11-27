---
layout: post
title: HTTP请求和返回示例
date: 2016-09-05
tags: ["cs"]
---

以GeneDock官网（[https://genedock.com](https://genedock.com)）为例，用各种软件（curl，HTTPie，Postman REST Client，python的request）进行请求和返回。

## Curl

```
$curl -v https://genedock.com


* Rebuilt URL to: https://genedock.com/
*   Trying 182.92.0.168...
* Connected to genedock.com (182.92.0.168) port 443 (#0)
* TLS 1.2 connection using TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
* Server certificate: *.genedock.com
* Server certificate: RapidSSL SHA256 CA - G3
* Server certificate: GeoTrust Global CA
> GET / HTTP/1.1
> Host: genedock.com
> User-Agent: curl/7.43.0
> Accept: */*
>
< HTTP/1.1 200 OK
< Server: nginx/1.6.0
< Date: Mon, 05 Sep 2016 05:58:07 GMT
< Content-Type: text/html; charset=utf-8
< Content-Length: 8856
< Connection: keep-alive
< Set-Cookie: session=eyJfaWQiOnsiIGIiOiJaREZsWm1ObU16UTFabVJtWlRSa016ZGlabU5rWldWaU5qWmpPVFJoTTJJPSJ9fQ.Cq6a7w.LUjBEmjf-e6B_4aGSpSHElVIVzg; HttpOnly; Path=/
<
<!DOCTYPE html><html lang="zh-CN"><head><title>GeneDock</title><meta charset="utf-8"><meta content="IE=edge" http-equiv="X-UA-Compatible"><meta content="width=1200" name="viewport"><meta content="GeneDock,www.genedock.com,genedock.com,genedock,北京聚道,聚道科技,基因数据云服务,北京聚道科技有限公司,GeneDock,北京GeneDock" name="Keywords"><meta content="GeneDock,www.genedock.com,genedock.com,genedock,北京聚道,聚道科技,基因数据云服务,北京聚道科技有限公司,GeneDock,北京GeneDoc
......
```

`-v`参数显示整个http通信过程。更多可以参考[阮一峰博客《curl网站开发指南》](http://www.ruanyifeng.com/blog/2011/09/curl.html)。

- 请求部分：

```
> GET / HTTP/1.1
> Host: genedock.com
> User-Agent: curl/7.43.0
> Accept: */*
```

`GET`是http动词，`HTTP/1.1`是HTTP的版本，`Host`是服务端的主机，`User-Agent`是发送请求的应用名称，`Accept`是可以接受何种类型的返回。

- 返回部分：

```
< HTTP/1.1 200 OK
< Server: nginx/1.6.0
< Date: Mon, 05 Sep 2016 05:58:07 GMT
< Content-Type: text/html; charset=utf-8
< Content-Length: 8856
< Connection: keep-alive
< Set-Cookie: session=eyJfaWQiOnsiIGIiOiJaREZsWm1ObU16UTFabVJtWlRSa016ZGlabU5rWldWaU5qWmpPVFJoTTJJPSJ9fQ.Cq6a7w.LUjBEmjf-e6B_4aGSpSHElVIVzg; HttpOnly; Path=/
```

`200`是status code（状态码），`Server`是客户端应用软件的名字和版本号，`Date`是消息产生的时间或者时间戳，`Content-Type`是返回body的对象类型，`Content-Length`是返回body的长度或者大小，`Connection`是允许客户端和服务端指定请求-返回链接的选项，`Set-Cookie`是用来设置客户端的一个token，让服务端来识别身份。

返回的body部分是一个html文件。

## HTTPie

```
$http --print=HhBb https://genedock.com


GET / HTTP/1.1
Accept: */*
Accept-Encoding: gzip, deflate
Connection: keep-alive
Host: genedock.com
User-Agent: HTTPie/0.9.3



HTTP/1.1 200 OK
Connection: keep-alive
Content-Encoding: gzip
Content-Type: text/html; charset=utf-8
Date: Mon, 05 Sep 2016 06:34:50 GMT
Server: nginx/1.6.0
Set-Cookie: session=eyJfaWQiOnsiIGIiOiJZbUk1T0dReVpqbGhaakU0WkdObU1UazJaV05rTW1Fd05qVmtOakUzWW1ZPSJ9fQ.Cq6jig.rBqTiAoOL8QJj68W06WNs8lxlSY; HttpOnly; Path=/
Transfer-Encoding: chunked

<!DOCTYPE html><html lang="zh-CN"><head><title>GeneDock</title>
....
```

更多httpie的参数可见[https://github.com/jkbrzt/httpie](https://github.com/jkbrzt/httpie)

## Postman REST Client

![](/images/Postman-1.png)

![](/images/Postman-2.png)

![](/images/Postman-3.png)

## Python的Request包

```
$ python
Python 2.7.10 (default, Oct 23 2015, 19:19:21)
[GCC 4.2.1 Compatible Apple LLVM 7.0.0 (clang-700.0.59.5)] on darwin
Type "help", "copyright", "credits" or "license" for more information.

>>> import requests
>>> r = requests.get("https://genedock.com")
>>> print r.request.headers
{'Connection': 'keep-alive', 'Accept-Encoding': 'gzip, deflate', 'Accept': '*/*', 'User-Agent': 'python-requests/2.11.1'}

>>> print r.headers
{'Content-Encoding': 'gzip', 'Transfer-Encoding': 'chunked', 'Set-Cookie': 'session=eyJfaWQiOnsiIGIiOiJaakkzTnpZd09UQmtNRFEyWkdNM016a3paR0ZoWVRFNVpUWXhPVFJqWXprPSJ9fQ.Cq6lCQ.KzSeM-tEKnZxK8bvVi77qZSJnPQ; HttpOnly; Path=/', 'Server': 'nginx/1.6.0', 'Connection': 'keep-alive', 'Date': 'Mon, 05 Sep 2016 06:41:13 GMT', 'Content-Type': 'text/html; charset=utf-8'}

>>> print r.status_code
200

>>> print r.content
<!DOCTYPE html><html lang="zh-CN"><head><title>GeneDock</title>
```

