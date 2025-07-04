# Nginx-1.27.3-http-flv-module
这是我的 Nginx RTMP/HTTP-FLV 直播服务器。

我只是重新编译了 Nginx 1.27.3、nginx-http-flv-module-master、OpenSSL 1.1.1w、PCRE 8.45 和 zlib 1.3.1 的源代码，没有进行任何修改。

我懒得提供源码了，反正应该没人用的吧……

这个服务器由 Nginx 和 nginx-http-flv-module 模块构成，里面做了几个中文批处理脚本。

内置了三个网页：一个是简易的播放页，一个是复杂一些的测试播放页，还有一个是 HTTP-FLV 附带的 stat.xml，用于监控推流和拉流。

我使用 Sakura FRPC 解决了公网直播问题，Nginx 配置文件内置了一个本地代理，用于解决浏览器混合内容问题：外部请求是 HTTPS，内部代理使用 HTTP，浏览器只能看到 HTTPS 连接。

这个服务器基本上没有任何安全措施！
——————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————————
This is my nginx rtmp/http-flv live server

I have merely recompiled the source code for Nginx 1.27.3, nginx-http-flv-module-master, OpenSSL 1.1.1w, PCRE 8.45, and zlib 1.3.1, without any modifications.

Here's the professional English translation of your text:

"I'm disinclined to provide the source code, as it's unlikely anyone would use it anyway.

This server is composed of Nginx and the nginx-http-flv-module. It includes several Chinese batch scripts.

It has three built-in web interfaces: a simple playback page, a more complex test playback page, and the stat.xml page provided by http-flv for monitoring push and pull streams.

I use Sakura FRPC to address public network live streaming issues. The Nginx configuration file includes a local proxy to resolve browser mixed content warnings: external requests are HTTPS, the internal proxy uses HTTP, and the browser only perceives the HTTPS connection.

This server fundamentally lacks any security measures!"
