# 跨洞母题 🧵

跨主题反复出现的思维模式。每发现一个新洞印证了某个母题，就回来加一条——这一页越长，说明你越接近"事物背后共通的道理"。

## 已建立的连接，双向都能走

一旦连接由内向外建好，两个方向就都能走，不必再发起"陌生入站"。

- [内网穿透](networking/01-intranet-penetration.md)：本地主动建隧道并保持，外部请求借它**反向流回**内网。
- [WebSocket](networking/07-websocket.md)：客户端建好连接，服务器借**同一条连接的回程**主动推消息。

## 信任 / 解析追到底，必有内置锚点

任何"层层往上问"的体系，最底下必须有个"出厂就钉死、不再往下问"的锚点，否则无限递归、永远落不了地。

- [DNS](networking/02-dns.md)：根服务器 IP 内置在软件里；本地 DNS 的地址靠 DHCP 自动给。
- [TLS](networking/06-tls.md)：根证书出厂内置在操作系统 / 浏览器里。

## 分层 + 封装

每层只管自己那一级抽象，上下互不干涉；数据层层加头（封装）、层层拆头（解封装）。

- [分层与封装](networking/03-layering.md)：IP / TCP / HTTP 各管一层。
- [WebSocket / socket](networking/07-websocket.md)：socket 是接口、不是协议。
- [负载均衡](networking/08-load-balancing-cdn.md)：L4 看 IP+端口，L7 看 HTTP 内容。

## 在更弱的底座上补出更强的抽象

底层常常只给一个很朴素、甚至有缺陷的能力；上层靠编号、约定、状态表、签名、缓存等机制，补出应用真正想要的高级能力。

- [TCP](networking/05-tcp.md)：IP 只尽力而为，TCP 用序号、确认、重传补出可靠有序字节流。
- [HTTP / Cookie / Session](networking/09-http-cache-cookie-session.md)：HTTP 天生无状态，Cookie + Session 在独立请求之间补出登录态；缓存给重复请求补"记忆"。
- [数据库](database/01-storage-pages-buffer-wal.md)：普通文件和磁盘只提供朴素读写，数据库用页、索引、缓存池和日志补出可靠、可查询、可恢复的账本。
- [JavaScript 运行时](javascript/01-js-runtime.md)：ECMAScript 只定义语言核心，浏览器和 Node.js 作为宿主补出网络、文件、DOM、定时器和事件循环。

## 追到最底，是物理 / 人 / 商业

技术链条总有落地的地基——不是某个中央调度，而是物理规则、人工配置、商业合同。

- [路由与 BGP](networking/04-routing-bgp.md)：路由表的尽头是 IANA 发号 + 各家人工配 BGP 邻居 + 商业互联协议。
