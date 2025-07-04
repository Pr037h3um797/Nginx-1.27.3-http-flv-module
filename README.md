# Nginx-1.27.3-http-flv-module windows 10

Nginx-1.27.3-HTTP-FLV-Module (Windows 10)

这是我为 Windows 10 环境设计的 Nginx RTMP/HTTP-FLV 直播服务器。

我只是重新编译了以下组件的源代码，并未做任何修改：

    Nginx 1.27.3

    nginx-http-flv-module-master

    OpenSSL 1.1.1w

    PCRE 8.45

    zlib 1.3.1

目前我暂不提供源码，主要是考虑到可能不会有太多人使用。该服务器的核心功能由 Nginx 和 nginx-http-flv-module 模块构建。此外，它还包含了一些用于操作便利的中文批处理脚本。

功能特性

该服务器内置了三个网页界面：

    一个基本的简易播放页，用于快速测试。

    一个更复杂的测试播放页，提供更多功能。

    一个由 HTTP-FLV 模块提供的 stat.xml 页面，用于监控推流和拉流的统计信息。

公网访问

为了解决公网直播问题，我使用了 Sakura FRPC。Nginx 配置文件中包含了一个本地代理，旨在解决浏览器混合内容警告。这种设置确保了外部请求通过 HTTPS 处理，而内部代理使用 HTTP，使浏览器感知到的始终是安全的 HTTPS 连接。

重要安全提示

请务必注意，此服务器从根本上没有任何强大的安全措施。 它主要用于个人或受控的测试环境，在没有实施适当安全协议的情况下，不应将其暴露在公共互联网上。



Nginx-1.27.3-HTTP-FLV-Module for Windows 10

This repository contains my Nginx RTMP/HTTP-FLV live streaming server, designed for Windows 10 environments.

I've simply recompiled the source code for the following components without any modifications:

    Nginx 1.27.3

    nginx-http-flv-module-master

    OpenSSL 1.1.1w

    PCRE 8.45

    zlib 1.3.1

While I'm not providing the source code at this time, primarily due to the belief that it might not see widespread use, the server's core functionality is built upon Nginx and the nginx-http-flv-module. It also includes several Chinese-language batch scripts for operational convenience.

Features

The server includes three integrated web interfaces:

    A basic, simple playback page for quick testing.

    A more advanced test playback page with additional features.

    The stat.xml page, provided by the HTTP-FLV module, for monitoring push and pull stream statistics.

Public Network Accessibility

To enable public network live streaming, I've utilized Sakura FRPC. The Nginx configuration incorporates a local proxy designed to mitigate browser mixed content warnings. This setup ensures that while external requests are handled over HTTPS, the internal proxy uses HTTP, allowing the browser to perceive a secure HTTPS connection end-to-end.

Important Security Notice

Please be aware that this server fundamentally lacks any robust security measures. It is primarily intended for personal or controlled testing environments and should not be exposed to the public internet without implementing proper security protocols.

Acknowledgments

All web design and technical support for this project were collaboratively facilitated by resources from Deepseek, Gemini, Cnblogs, and a certain less-than-reputable CSDN.
