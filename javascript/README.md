# JavaScript 🕳️

从一个朴素问题出发——**"JavaScript 不是只有一门语言吗，为什么还分浏览器、Node.js、运行时？"**——一路追到 JS 引擎、宿主环境、事件循环和异步 API 的边界。

## 推荐阅读顺序

| # | 篇 | 一句话 |
|---|---|---|
| 01 | [JavaScript 运行时](01-js-runtime.md) | JS 引擎只负责执行语言本身；宿主运行时补出事件循环、异步 API、GC、内存边界和 native bridge 等能力 |
| 02 | [事件循环 vs 游戏帧循环](02-event-loop-vs-game-loop.md) | `Promise.then` 是 JS 微任务，不是下一帧；Cocos 的 `scheduleOnce` / `update` 属于引擎帧调度 |

## 母题

本洞继续印证 [../patterns.md](../patterns.md) 里的"分层 + 封装"和"在更弱的底座上补出更强的抽象"：ECMAScript 只定义语言核心，真正能做事的应用能力由宿主环境和引擎调度在外面补齐。
