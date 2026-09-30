<div align="center">

[English](./README.en.md) | **简体中文**

# ✦ xiaoyu-hue

*一个非程序员出身的普通人，正在把 AI Agent 当成一种新型生产工具，通过实际项目实验它能把非程序员的生产边界推到哪里。*

[![GitHub](https://img.shields.io/badge/GitHub-xiaoyu--hue-181717?style=flat-square&logo=github)](https://github.com/xiaoyu-hue)
[![原创项目](https://img.shields.io/badge/原创项目-4-5B6CD8?style=flat-square)](https://github.com/xiaoyu-hue?tab=repositories)
[![Built with](https://img.shields.io/badge/Built%20with-AI%20Agent-646CFF?style=flat-square)](https://github.com/xiaoyu-hue)
[![最后更新](https://img.shields.io/badge/最后更新-2026--09-9A8CFF?style=flat-square)](https://github.com/xiaoyu-hue)

**四个原创项目 · 全部开源 · 全部如实标注了自己做不到什么**

</div>

---

## 目录

- [我是谁](#我是谁)
- [第一个项目：sonder520](#第一个项目sonder520)
- [第二个想法：Nymir](#第二个想法nymir)
- [XY 系列：xy-club 与 xy-intro-card](#xy-系列xy-club-与-xy-intro-card)
- [四个作品一览](#四个作品一览)
- [快速开始](#快速开始)
- [这场实验在测什么](#这场实验在测什么)
- [我和 AI 的协作方式](#我和-ai-的协作方式)
- [这些项目做不到什么](#这些项目做不到什么)
- [联系与反馈](#联系与反馈)
- [我的局限与选择](#我的局限与选择)

---

## 我是谁

我没有任何编程基础，甚至没有专门去了解过编程。在接触 AI Agent 之前，"把自己的想法做成一个能用的软件"这件事，对我来说不在选项里。

接触 AI Agent 之后，这扇门开了。原来一个不懂代码的人，也能把想法变成网站、Web 应用、甚至 PWA。

我没有打算变成程序员。我做这些项目，是想回答一个具体问题：

> **当生产工具从"编程语言"换成"AI Agent"，一个非程序员到底能走多远？**

下面四个项目就是这个问题的四份答卷。它们不是教程练手作品，是真实在跑、真实有人用的东西——四个都有在线站点，主要项目都带 CI 测试门禁，光 sonder520 一个就跑了 776 项测试。

---

## 第一个项目：sonder520

**从"跟着教程做"到"自己摸索"**

最初是跟着博主的教程，做出了 v1 版本。从那以后，就全是自己摸索了。

我特别喜欢水墨风格和液态玻璃风格，就一直在想：这两种能不能组合在一起？尝试了一下，诶，发现真的可以。后来觉得缺少背景，就用了我最喜欢的壁纸；再后来觉得个性不够，又加了自定义壁纸功能，可以调节透明度来贴合整体风格。

<div align="center">

> **sonder** · 过客 &nbsp;|&nbsp; **520** · 给自己的礼物

</div>

名字就是这么来的。

### 从本地到上线

跟着博主做的版本只能在自己本地看，我就想让其他人也能看看。于是去问 AI 怎么部署上线，它推荐了好几个静态部署平台。

**我第一个部署的是 Netlify** —— 那是我首次亲自完成部署。后来 Netlify 的部署次数用完了，我又配置了 GitHub Pages 和 Cloudflare Pages。后面的部署同步就交给 AI Agent 了。

### 从工作台到个人 OS

从 v1.0 一步步做到 v6.x，12 个模块、776 项测试、PWA 离线可用、可选加密存储。板块几乎够了，但跨板块协作还有很多可以补的地方。

我觉得它现在已经不能叫"个人工作台"了，更像是一个**个人 OS**。

| | |
|---|---|
| 🔗 在线 | [xiaoyu-hue.github.io/sonder520](https://xiaoyu-hue.github.io/sonder520/) |
| 🛠 技术 | HTML / CSS / 原生 JS · IndexedDB · WebCrypto · PWA，零运行时依赖、零构建 |
| 📄 协议 | MIT |

---

## 第二个想法：Nymir

做完 sonder520 之后，我脑子里有另一个问题：

> 有没有一个注重安全、隐私、匿名、**不会被中心化服务器记录**的倾诉聊天的地方？

像抖音、QQ、微信这些都是中心化服务，聊天记录通常存在它们的服务器上。而 Nymir 没有业务服务器，不会记录你的数据——数据只存在你自己的浏览器里。匿名采用端到端加密，随机生成名字，不用注册。

它本质上就是一个**树洞**，一个可以安心倾诉的地方。

<div align="center">

```
用户 A ════ 🔐 ════ P2P 直连 ════ 🔐 ════ 用户 B
                  无业务服务器
```

</div>

视觉体系是液态玻璃风格 ＋ 星空主题。

当然，**这不是绝对安全的**。虽然用的都是前沿技术（X25519 密钥协商、每消息 HKDF、Ed25519 签密文），但我是站在巨人的肩膀上实现自己的想法而已——**我不是密码学专家**。所有已知局限都如实写在了 README 里，没有藏起来。

| | |
|---|---|
| 🔗 在线 | [xiaoyu-hue.github.io/Nymir](https://xiaoyu-hue.github.io/Nymir/) |
| 🛠 技术 | React 19 · TypeScript · Vite · Trystero / WebRTC · 293 项测试 |
| 📄 协议 | AGPL-3.0 |

---

## XY 系列：xy-club 与 xy-intro-card

做完两个给自己用的东西之后，我想做点**别人也能直接拿去用**的。

### xy-club：俱乐部官网模板

市面上多数俱乐部官网要么丑、要么改不动、要么部署麻烦。我想证明一件事：**零构建、零依赖、单 JSON 文件，也能做出液态玻璃质感、带微交互、后台可视化、还能纯静态托管的可复用模板。**

官网与后台共用一份 JSON 数据：后台改什么，前台立刻是什么，不需要重新构建、不需要懂代码。**换一个俱乐部，只需改内容、换主题，不改代码。**

### xy-intro-card：个人介绍名片生成器

同一家族的另一件工具：给成员做个人介绍卡。零依赖单文件——字体、图标、头像全部内嵌，不联网也能打开，发给别人就是一张独立卡片。

| | |
|---|---|
| 🔗 xy-club 在线 | [xiaoyu-hue.github.io/xy-club](https://xiaoyu-hue.github.io/xy-club/) |
| 🔗 xy-intro-card 在线 | [xiaoyu-hue.github.io/xy-intro-card](https://xiaoyu-hue.github.io/xy-intro-card/) |
| 🛠 xy-club | Node.js · Express · JSON 存储 · 123 项测试 · MIT |
| 🛠 xy-intro-card | 单文件 HTML，零依赖、零联网 · MIT |

> `XY` 只是项目系列的命名前缀，**XY俱乐部是默认演示案例，不是专属品牌**——把演示内容换成任意俱乐部/团队，工具逻辑完全不变。

---

## 四个作品一览

<div align="center">∙ ∙ ∙</div>

<table border="1" cellpadding="16" cellspacing="0" width="100%">
<tr>
<td align="center" width="50%">

🌊 &nbsp; <b><a href="https://github.com/xiaoyu-hue/sonder520">sonder520</a></b>
<br><br>
本地个人工作与生活管理工具，数据只存在你的浏览器
<br><br>
<code>12 模块</code> · <code>776 测试</code> · <code>v6.x</code> · MIT

</td>
<td align="center" width="50%">

✦ &nbsp; <b><a href="https://github.com/xiaoyu-hue/Nymir">Nymir</a></b>
<br><br>
匿名树洞 · P2P 加密聊天 · 阅读即焚
<br><br>
<code>293 测试</code> · <code>v1.6.x</code> · AGPL-3.0

</td>
</tr>
<tr>
<td align="center" width="50%">

💎 &nbsp; <b><a href="https://github.com/xiaoyu-hue/xy-club">xy-club</a></b>
<br><br>
可复用的俱乐部官网模板 + 可视化后台
<br><br>
<code>7 种板块</code> · <code>8 套主题</code> · <code>123 测试</code> · MIT

</td>
<td align="center" width="50%">

🪪 &nbsp; <b><a href="https://github.com/xiaoyu-hue/xy-intro-card">xy-intro-card</a></b>
<br><br>
个人介绍名片生成器，双击即用
<br><br>
<code>单文件</code> · <code>2 种模式</code> · MIT

</td>
</tr>
</table>

<div align="center">∙ ∙ ∙</div>

> 另外两个仓库 `cs-self-learning-XY`、`free-programming-books-XY` 是 fork 的学习资料，不是原创作品。

**维护状态（2026-09 更新）**：四个项目都还在维护，但**节奏比之前慢**——主力设备坏了，现在用备用设备更新，等买了新机器会恢复。它们没有被放弃。如果你打算正式用某一个，请先读它自己的 README。

---

## 快速开始

四个项目都有在线版本，**不需要安装任何东西就能直接试**。

| 项目 | 在线体验 | 本地运行 |
|---|---|---|
| 🌊 **sonder520** | [xiaoyu-hue.github.io/sonder520](https://xiaoyu-hue.github.io/sonder520/) | 克隆仓库后，浏览器直接打开 `index.html`（推荐 Chrome / Edge） |
| ✦ **Nymir** | [xiaoyu-hue.github.io/Nymir](https://xiaoyu-hue.github.io/Nymir/) | 克隆 → `cd Nymir` → `npm install` → `npm run dev` |
| 💎 **xy-club** | [xiaoyu-hue.github.io/xy-club](https://xiaoyu-hue.github.io/xy-club/) | 克隆 → `pnpm install`（或 `npm install`）→ `node server.js`；官网 `localhost:3000`，后台 `localhost:3000/admin` |
| 🪪 **xy-intro-card** | [xiaoyu-hue.github.io/xy-intro-card](https://xiaoyu-hue.github.io/xy-intro-card/) | 下载单个 HTML 文件，双击打开即可，断网也能用 |

完整的环境要求与开发命令，见各项目自己的 README。欢迎提 issue 和 PR；**Nymir** 请先读完它的安全局限再决定使用或反馈。
> 提醒：xy-club 后台默认管理密码写在它自己的 README 里，**部署上线前务必先改掉**。

---

## 这场实验在测什么

四个项目不是随便做的，每一个都在回答一个具体问题：

| 项目 | 它在测的边界 |
|---|---|
| **sonder520** | 非程序员做的东西，能有多少工程纪律？——776 项测试、15 份 ADR、分层架构、CI 门禁 |
| **Nymir** | 零基础的人能不能碰密码学？——端到端加密跑通了，但它也是最需要你保持警惕的一个 |
| **xy-club** | 做一个好看、好改、好部署的官网，门槛能压到多低？——零构建、零数据库、单个 JSON 驱动整站 |
| **xy-intro-card** | 工具能简单到什么程度？——一个 HTML 文件，双击打开就能用 |

---

## 我和 AI 的协作方式

我啥也不会，遇到问题就问 AI。但我不是全盘接受它的答案——**我会让它把专业术语翻译成我能懂的话，然后自己斟酌，心中确认了再采纳。**

我经常把天马行空的想法丢给 AI Agent，作为外行，什么想象都有。它有时候会打断我说这个不可行，但同时会给出一个差不多符合我心中预期的替代方案，我就会在它的建议基础上做选择。

<div align="center">

| 我的角色 | AI 的角色 |
|:---:|:---:|
| 提出想法 · 做出判断 · 选择方案 | 翻译术语 · 提供方案 · 执行实现 |

</div>

### 三次判断是我做的

规则好写，真正说明问题的是实际发生过什么。这三个例子都来自上面四个项目的真实过程：

| 发生了什么 | AI 做了什么 | 我的判断 |
|---|---|---|
| **第一次把项目弄上线** | 推荐了好几个静态部署平台 | 它给的是候选清单，不是命令。我第一个亲自部署选了 **Netlify**；免费额度用完后，又自己配了 GitHub Pages 和 Cloudflare Pages。 |
| **水墨＋液态玻璃能不能揉在一起** | 没法保证两种风格能融合 | 我想要，就直接试了。试出来真的可以，还成了 sonder520 整站的视觉基调。**有时候"先试再问"才是对的顺序。** |
| **给 Nymir 的安全划边界** | 顺利写出了加密代码（X25519、HKDF、Ed25519） | 代码不等于担保。我不是密码学专家，所以"未经专业安全审计""不建议用于真实敏感场景"这两句话，是我自己写进 README 的。**AI 的能力边界，得由我来划。** |

这套规则写在每个项目的 `AGENTS.md` 里：需求确认后再开工、大任务拆成可验证的小步骤逐一交付、技术选型附理由并经我批准、不可逆操作（删文件、覆盖代码、付费服务、公开发布）必须先问我、如实说明不确定性、提出方案时必须讲清权衡取舍。

<div align="center">

> ### **代码是 AI 写的，判断是我做的。**

</div>

---

## 这些项目做不到什么

既然是"实验"，就该把失败的部分也写出来。以下都是各项目 README 里如实列出的：

| 项目 | 不适合 / 已知局限 |
|---|---|
| sonder520 | 无跨设备自动同步（需手动导入备份）、无团队协作、不是原生 App、浏览器数据可能被清理 |
| Nymir | **未经专业安全审计**、TOFU 首次见面信任有弱点、公共信令可观察元数据、流量混淆强度有限、无离线收件箱 |
| xy-club | 单密码鉴权无多管理员、无 CSRF 防护、单进程文件读写、无 SSR/SEO、不适合支付类站点 |
| xy-intro-card | 纯前端单文件，无后端存储、无多人协作、无复杂动画 |

**Nymir 尤其要提醒**：作者非程序员出身、代码未经过专业安全审计，**不建议用于真实敏感场景**。

---

## 联系与反馈

很高兴你能看到这里。欢迎反馈，也欢迎告诉我这些项目被怎么用了。

| | |
|---|---|
| 💬 Bug 与想法 | 在对应仓库提 issue。请写清"你做了什么、期望什么、实际发生了什么"，有截图最好 |
| 🤝 Pull Request | 欢迎。涉及结构改动（架构、依赖、安全相关代码）请先开 issue 对齐方向，再动手写代码 |
| 🌏 语言 | 中文、英文 issue 都可以。英文写得简单也没关系，我会借助 AI 阅读 |
| 🙅 不接的 | 付费定制开发、帮别人做安全审计、作业代做、"帮我改我的代码" |
| ⚠️ 关于 Nymir | 请不要用它聊真正敏感的事，理由见上面的局限。安全问题欢迎讨论，但那不构成担保 |

回复可能会慢：我现在用备用设备维护这些项目，所有事都是我一个人在做。

---

## 我的局限与选择

我很清楚自己最大的局限：**缺少编程的硬性技术，很多事情都依赖 AI**。AI 给我建议，我觉得好就采纳，觉得不好就问它还有没有别的方案——就这样一步步做了四个项目。

我也纠结过：是不是占用了 GitHub 的公共空间？要不要设成私有，或者干脆删掉？但我非常敬佩开源精神，所以我的项目都会开源，虽然代码还在持续优化中。

所以你会在这些仓库里看到一些少见的东西：README 里写着"不适合什么场景"、写着"已知局限"、写着"未经专业安全审计"。

<div align="center">

> ### **这不是谦虚，是如实标注。**

</div>

**引用我最喜欢的一句话献给我也献给光临寒舍的各位大佬们“去好奇 去探索 去试试 去检验” 诸君共勉之**

---

<div align="center">

*AI 时代的个体赋能，祝我们共同见证未来的 AGI，共同见证人类的第四次工业革命。*

---

[English](./README.en.md) | **简体中文**

*最后更新：2026-09*

</div>
