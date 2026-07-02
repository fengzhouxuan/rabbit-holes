# 计算机网络 🕳️

从一个具体问题出发——**"NAT 后面的机器，外面怎么访问？"**——一路追根究底，直到能把"打开一个网页"拆到零件级。

## 推荐阅读顺序

| # | 篇 | 一句话 |
|---|---|---|
| 01 | [内网穿透 / NAT](01-intranet-penetration.md) | NAT 放出站、挡陌生入站；穿透靠一条主动建好的隧道反向流回 |
| 02 | [DNS](02-dns.md) | 域名→IP，从根开始层层迭代追问 |
| 03 | [分层与封装](03-layering.md) | TCP/IP 四层模型；数据像套娃一样层层加头 |
| 04 | [逐跳路由 / BGP](04-routing-bgp.md) | IP 不变、MAC 每跳变；全球路由靠 BGP 涟漪式通告 |
| 05 | [TCP](05-tcp.md) | 三次握手 / 四次挥手 / 滑动窗口 / 拥塞控制 |
| 06 | [TLS / HTTPS](06-tls.md) | 防偷听（DH 换钥匙）+ 防冒充（证书信任链） |
| 07 | [WebSocket / socket / HTTP·TCP·UDP](07-websocket.md) | 借 HTTP 升级成双向常开；理清协议与接口 |
| 08 | [负载均衡 / CDN](08-load-balancing-cdn.md) | 一台扛不住怎么分流；内容怎么就近用户 |
| 09 | [HTTP / 缓存 / Cookie / Session](09-http-cache-cookie-session.md) | HTTP 一问一答且无状态；缓存让它少问，Cookie/Session 让它认得你 |

## 一图总览

一次访问大网站，把这些篇章串起来：

![一次访问的完整旅程](assets/full-request-journey.svg)

## 母题

本洞印证的跨领域母题见 [../patterns.md](../patterns.md)：已建立连接双向可走、信任的内置锚点、分层封装、在弱底座上补强抽象、追到底是物理/人/商业。
