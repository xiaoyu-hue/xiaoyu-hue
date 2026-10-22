<div align="center">

[English](./README.en.md) | **简体中文**

# ✦ xiaoyu-hue

*一个非程序员出身的普通人，正在把 AI Agent 当成一种新型生产工具，通过实际项目实验它能把非程序员的生产边界推到哪里。*

[![GitHub](https://img.shields.io/badge/GitHub-xiaoyu--hue-181717?style=flat-square&logo=github)](https://github.com/xiaoyu-hue)
[![原创项目](https://img.shields.io/badge/原创项目-7-5B6CD8?style=flat-square)](https://github.com/xiaoyu-hue?tab=repositories)
[![Built with](https://img.shields.io/badge/Built%20with-AI%20Agent-646CFF?style=flat-square)](https://github.com/xiaoyu-hue)
[![最后更新](https://img.shields.io/badge/最后更新-2026--10-9A8CFF?style=flat-square)](https://github.com/xiaoyu-hue)

**七个原创项目 · 全部开源 · 都尽量如实标注了各自的局限**

[📝 我的主站 →](https://xiaoyu-hue.github.io/)

</div>

---

## 目录

- [我是谁](#我是谁)
- [第一个项目：sonder520](#第一个项目sonder520)
- [第二个想法：Nymir](#第二个想法nymir)
- [XY 系列：xy-club 与 xy-intro-card](#xy-系列xy-club-与-xy-intro-card)
- [综合信息聚集地：九溪 jiuxi](#综合信息聚集地九溪-jiuxi)
- [随时刻流动的背景主题：时念 shinian](#随时刻流动的背景主题时念-shinian)
- [与书共度的时光：书时 TailTale](#与书共度的时光书时-tailtale)
- [七个作品一览](#七个作品一览)
- [快速开始](#快速开始)
- [这场实验在测什么](#这场实验在测什么)
- [我和 AI 的协作方式](#我和-ai-的协作方式)
- [这些项目做不到什么](#这些项目做不到什么)
- [联系与反馈](#联系与反馈)
- [我的局限与选择](#我的局限与选择)
- [许可证](#许可证)

---

## 我是谁

我没有任何编程基础，甚至没有专门去了解过编程。在接触 AI Agent 之前，"把自己的想法做成一个能用的软件"这件事，对我来说不在选项里。

接触 AI Agent 之后，这扇门开了。原来一个不懂代码的人，也能把想法变成网站、Web 应用、甚至 PWA。

我没有打算变成程序员。我做这些项目，是想回答一个具体问题：

> **当生产工具从"编程语言"换成"AI Agent"，一个非程序员到底能走多远？**

下面七个项目就是这个问题的七份答卷。它们不是教程练手作品，是真实在跑、真实有人用的东西——七个都有在线站点，主要项目都带 CI 测试门禁，光 sonder520 一个就跑了 776 项测试。

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
| 📄 协议 | MIT（代码）/ CC BY 4.0（文档） |

---

## 第二个想法：Nymir

做完 sonder520 之后，我脑子里有另一个问题：

> 有没有一个注重安全、隐私、匿名、**聊天内容不被业务服务器留存**的倾诉聊天的地方？

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
| 📄 协议 | AGPL-3.0（代码）/ CC BY-NC-SA 4.0（文档） |

---

## XY 系列：xy-club 与 xy-intro-card

做完两个给自己用的东西之后，我想做点**别人也能直接拿去用**的。

### xy-club：俱乐部官网模板

市面上多数俱乐部官网要么丑、要么改不动、要么部署麻烦。我想验证一件事：**零构建、零依赖、单 JSON 文件，能否做出液态玻璃质感、带微交互、后台可视化、还能纯静态托管的可复用模板。**

官网与后台共用一份 JSON 数据：后台改什么，前台立刻是什么，不需要重新构建、不需要懂代码。**换一个俱乐部，一般改改内容、换套主题就行，基本不用碰代码。**

### xy-intro-card：个人介绍名片生成器

同一家族的另一件工具：给成员做个人介绍卡。零依赖单文件——字体、图标、头像全部内嵌，不联网也能打开，发给别人就是一张独立卡片。

| | |
|---|---|
| 🔗 xy-club 在线 | [xiaoyu-hue.github.io/xy-club](https://xiaoyu-hue.github.io/xy-club/) |
| 🔗 xy-intro-card 在线 | [xiaoyu-hue.github.io/xy-intro-card](https://xiaoyu-hue.github.io/xy-intro-card/) |
| 🛠 xy-club | Node.js · Express · JSON 存储 · 123 项测试 · MIT（代码）/ CC BY 4.0（文档） |
| 🛠 xy-intro-card | 单文件 HTML，零依赖、零联网 · MIT（代码）/ CC BY 4.0（文档） |

> `XY` 只是项目系列的命名前缀，**XY俱乐部是默认演示案例，不是专属品牌**——把演示内容换成任意俱乐部/团队，工具逻辑完全不变。

---

## 综合信息聚集地：九溪 jiuxi

做完前面几个"给自己或给别人用的工具"之后，我想做一件不一样的事：**把信息聚成一个我个人顺手用的综合信息聚集地——以 AI 为主，热点新闻为辅。**

九溪不是一个聊天机器人，而是一个**信息集合**——用时间线把 AI 发展脉络铺开、用工具箱把值得一试的开源项目列出来、用读书推荐把资料指给你。

说句实话，免得被误读成权威推荐：时间线加进去**主要是为了页面更好看**；工具箱和读书推荐里的清单，**大部分是我让 AI 帮我推荐的，我自己也没全读完**。所以本意是自用，不是"我逐条读过、用过、判断过"的专家清单。

它现在有三块内容：一条 AI 发展时间线（国内外并重）、一个 AI 工具箱（含完整的 AI Agent 主线）、一份读书推荐（每本配客观推荐语和可在线阅读的链接）；规模分别是 192 / 40 / 37。

| | |
|---|---|
| 🔗 在线 | [xiaoyu-hue.github.io/jiuxi](https://xiaoyu-hue.github.io/jiuxi/) |
| 🛠 技术 | Astro 7 · Tailwind v4 · 零运行时依赖 · 双站部署（Cloudflare Pages 主 + GitHub Pages 备）· CI 安全门禁 |
| 📄 协议 | Apache-2.0（代码）/ CC BY-NC 4.0（内容） |

---

## 随时刻流动的背景主题：时念 shinian

前面几个项目都是"工具"，时念的初衷是做一款**随真实时刻、四季与天气变化的背景主题**——一个装在手机里的"活着的窗景"。

它的主角是一片天空：随真实时刻、四季与天气流动，黎明到深夜七段色阶连续过渡；时钟、倒数日、许愿池、实时天气（覆盖 57 个中国主要城市，直连 Open-Meteo 免密钥）都浮在液态玻璃卡片上。打开它，看到的不是冷冰冰的时刻，而是一方正在流动的天——本质上是一张会随时间变色的动态壁纸。

它面向手机优先：安卓 App（Capacitor 封装）+ 网页版，本地优先、可选加密存储。

| | |
|---|---|
| 🔗 在线 | [xiaoyu-hue.github.io/shinian](https://xiaoyu-hue.github.io/shinian/) |
| 🛠 技术 | TypeScript（esbuild 编译进 IIFE）· 原生 JS 零构建 · Capacitor 安卓封装 · 本地优先 + 可选加密存储 |
| 📄 协议 | MIT（代码）/ CC BY-NC-SA 4.0（文档） |

---

## 与书共度的时光：书时 TailTale

前面几个项目都是"工具"，书时想试试另一件事：**让读书这件事本身变得有牵挂。**

它的玩法一句话能说完：**读书记时长金币，金币养宠物。** 电子书导入浏览器本地，打开书籍即开始计时——阅读每 30 分钟 +10 金币，每日打卡、读完一本书都有奖励；金币喂给一只像素猫，它有三属性、有好感度、有成长阶段，连续阅读 30 分钟还会蹭屏幕撒娇。金币只能靠阅读赚取，**不可购买**——没有支付，没有账号，没有服务器。

书架支持 TXT / EPUB / PDF 三种格式，按文件内容指纹记忆进度，同一本书换设备能续读；阅读器做了统一的滑动翻页手势，iOS 与安卓都真机验证过。它还能接入 AI 解读书（用户自带密钥、浏览器直连），生成全书大纲或针对这本书提问。

名字的由来：**书时**，取"与书共度的时光"之意；**TailTale**，是"猫尾（tail）"与"故事（tale）"的双关——一条尾巴和一个故事，讲的都是陪伴。

| | |
|---|---|
| 🔗 在线 | [tailtale-520.pages.dev](https://tailtale-520.pages.dev/) |
| 🛠 技术 | React 18 · TypeScript · Vite · PWA · epubjs / pdfjs-dist 按需加载 · IndexedDB · 73 项测试 |
| 📄 协议 | Apache-2.0（代码）/ CC BY-NC 4.0（文档） |

---

## 七个作品一览

<div align="center">∙ ∙ ∙</div>

<table border="1" cellpadding="16" cellspacing="0" width="100%">
<tr>
<td align="center" width="50%">

🌊 &nbsp; <b><a href="https://github.com/xiaoyu-hue/sonder520">sonder520</a></b>
<br><br>
本地个人工作与生活管理工具，数据只存在你的浏览器
<br><br>
<code>12 模块</code> · <code>776 测试</code> · <code>v6.x</code> · MIT（代码）/ CC BY 4.0（文档）

</td>
<td align="center" width="50%">

✦ &nbsp; <b><a href="https://github.com/xiaoyu-hue/Nymir">Nymir</a></b>
<br><br>
匿名树洞 · P2P 加密聊天 · 阅读即焚
<br><br>
<code>293 测试</code> · <code>v1.6.x</code> · AGPL-3.0（代码）/ CC BY-NC-SA 4.0（文档）

</td>
</tr>
<tr>
<td align="center" width="50%">

💎 &nbsp; <b><a href="https://github.com/xiaoyu-hue/xy-club">xy-club</a></b>
<br><br>
可复用的俱乐部官网模板 + 可视化后台
<br><br>
<code>7 种板块</code> · <code>8 套主题</code> · <code>123 测试</code> · MIT（代码）/ CC BY 4.0（文档）

</td>
<td align="center" width="50%">

🪪 &nbsp; <b><a href="https://github.com/xiaoyu-hue/xy-intro-card">xy-intro-card</a></b>
<br><br>
个人介绍名片生成器，双击即用
<br><br>
<code>单文件</code> · <code>2 种模式</code> · MIT（代码）/ CC BY 4.0（文档）

</td>
</tr>
<tr>
<td align="center" width="50%">

🗺️ &nbsp; <b><a href="https://github.com/xiaoyu-hue/jiuxi">九溪 jiuxi</a></b>
<br><br>
AI 信息聚集地 · 时间线 / 工具箱 / 读书推荐
<br><br>
<code>192 时间线</code> · <code>40 工具</code> · <code>37 书</code> · Apache-2.0（代码）/ CC BY-NC 4.0（内容）

</td>
<td align="center" width="50%">

🌌 &nbsp; <b><a href="https://github.com/xiaoyu-hue/shinian">时念 shinian</a></b>
<br><br>
手机里的活窗景 · 流动天空 + 时钟倒数日
<br><br>
<code>安卓 App</code> · <code>网页版</code> · 本地优先 · MIT（代码）/ CC BY-NC-SA 4.0（文档）

</td>
</tr>
<tr>
<td align="center" colspan="2">

📚 &nbsp; <b><a href="https://github.com/xiaoyu-hue/tailtale">书时 TailTale</a></b>
<br><br>
游戏化阅读器 · 读书记时长金币，金币养宠物
<br><br>
<code>73 测试</code> · <code>v1.7.0</code> · Apache-2.0（代码）/ CC BY-NC 4.0（文档）

</td>
</tr>
</table>

<div align="center">∙ ∙ ∙</div>

> 另外三个仓库 `cs-self-learning`、`free-programming-books` 是 fork 的学习资料，`rea` 是 fork 的逆向工程工具（来源 `morluto/rea`）——都不是原创作品。

**维护状态（2026-10 更新）**：七个项目都还在维护，但**节奏比之前慢**——主力设备坏了，现在用备用设备更新，等买了新机器会恢复。它们没有被放弃。如果你打算正式用某一个，请先读它自己的 README。

---

## 快速开始

七个项目都有在线版本，**基本不用安装就能直接试**。

| 项目 | 在线体验 | 本地运行 |
|---|---|---|
| 🌊 **sonder520** | [xiaoyu-hue.github.io/sonder520](https://xiaoyu-hue.github.io/sonder520/) | 克隆仓库后，浏览器直接打开 `index.html`（推荐 Chrome / Edge） |
| ✦ **Nymir** | [xiaoyu-hue.github.io/Nymir](https://xiaoyu-hue.github.io/Nymir/) | 克隆 → `cd Nymir` → `npm install` → `npm run dev` |
| 💎 **xy-club** | [xiaoyu-hue.github.io/xy-club](https://xiaoyu-hue.github.io/xy-club/) | 克隆 → `pnpm install`（或 `npm install`）→ `node server.js`；官网 `localhost:3000`，后台 `localhost:3000/admin` |
| 🪪 **xy-intro-card** | [xiaoyu-hue.github.io/xy-intro-card](https://xiaoyu-hue.github.io/xy-intro-card/) | 下载单个 HTML 文件，双击打开即可，断网也能用 |
| 🗺️ **九溪 jiuxi** | [xiaoyu-hue.github.io/jiuxi](https://xiaoyu-hue.github.io/jiuxi/) | 克隆仓库后，参考其 README 的本地构建说明（Astro 项目，需 Node 环境） |
| 🌌 **时念 shinian** | [xiaoyu-hue.github.io/shinian](https://xiaoyu-hue.github.io/shinian/) | 安卓 App 需 Capacitor 构建；网页版可直接打开，详见仓库说明 |
| 📚 **书时 TailTale** | [tailtale-520.pages.dev](https://tailtale-520.pages.dev/) | 克隆 → `cd tailtale` → `npm install` → `npm run dev`（需 Node.js 20+） |

完整的环境要求与开发命令，见各项目自己的 README。欢迎提 issue 和 PR；**Nymir** 请先读完它的安全局限再决定使用或反馈。
> 提醒：xy-club 后台默认管理密码写在它自己的 README 里，**部署上线前务必先改掉**。

---

## 这场实验在测什么

七个项目不是随便做的，每一个都在回答一个具体问题：

| 项目 | 它在测的边界 |
|---|---|
| **sonder520** | 非程序员做的东西，能有多少工程纪律？——776 项测试、15 份 ADR、分层架构、CI 门禁 |
| **Nymir** | 零基础的人能不能碰密码学？——端到端加密跑通了，但它也是最需要你保持警惕的一个 |
| **xy-club** | 做一个好看、好改、好部署的官网，门槛能压到多低？——零构建、零数据库、单个 JSON 驱动整站 |
| **xy-intro-card** | 工具能简单到什么程度？——一个 HTML 文件，双击打开就能用 |
| **九溪 jiuxi** | 非程序员能不能攒出一个顺手用的信息聚集地？——192 条时间线（偏观赏性）、40 个工具、37 本书，内容手工整理，工具与书单多为 AI 推荐、并非逐条亲测 |
| **时念 shinian** | 纯前端能不能做出"有生命感"的界面？——天空随真实时刻与天气流动，零动画库原生实现 |
| **书时 TailTale** | 游戏化能让读书变得有牵挂吗？——读书记时长金币、金币养猫，金币不可购买，无支付闭环 |

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

规则好写，真正说明问题的是实际发生过什么。这三个例子都来自上面七个项目的真实过程：

| 发生了什么 | AI 做了什么 | 我的判断 |
|---|---|---|
| **第一次把项目弄上线** | 推荐了好几个静态部署平台 | 它给的是候选清单，不是命令。我第一个亲自部署选了 **Netlify**；免费额度用完后，又自己配了 GitHub Pages 和 Cloudflare Pages。 |
| **水墨＋液态玻璃能不能揉在一起** | 没法保证两种风格能融合 | 我想要，就直接试了。试出来真的可以，还成了 sonder520 整站的视觉基调。**有时候"先试再问"反而是更顺的顺序。** |
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
| 九溪 jiuxi | 内容由作者手工整理（非全量自动抓取）；时间线偏观赏性，工具箱与读书清单多为 AI 推荐、并未逐条亲测；部分外链依赖第三方可用性；更新频率取决于作者时间 |
| 时念 shinian | 纯前端数据存本地、网页版功能少于安卓 App（如系统通知仅 App 支持）、天气依赖 Open-Meteo 接口 |
| 书时 TailTale | 纯前端数据存浏览器本地（清理浏览器数据前需先导出备份）、AI 解读首期仅支持 TXT/EPUB 且需用户自带 DeepSeek 密钥、工具箱（M4）尚未上线、依赖近两年版本的 Chrome/Edge/Safari |

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

我很清楚自己最大的局限：**缺少编程的硬性技术，很多事情都依赖 AI**。AI 给我建议，我觉得好就采纳，觉得不好就问它还有没有别的方案——就这样一步步做了七个项目。

我也纠结过：是不是占用了 GitHub 的公共空间？要不要设成私有，或者干脆删掉？但我非常敬佩开源精神，所以我的项目都会开源，虽然代码还在持续优化中。

所以你会在这些仓库里看到一些少见的东西：README 里写着"不适合什么场景"、写着"已知局限"、写着"未经专业安全审计"。

<div align="center">

> ### **与其说谦虚，不如说是把边界说清楚。**

</div>

**引用我最喜欢的一句话，也送给看到这里的你：“去好奇 去探索 去试试 去检验”——共勉。**

---

## 许可证

本仓库（xiaoyu-hue/xiaoyu-hue，即个人主页的源仓库）的内容采用 **知识共享 署名-非商业性使用 4.0 国际许可协议（CC BY-NC 4.0）**。

- 你可以：**署名**后分享、转载，或基于本仓库内容做**非商业**用途的再创作。
- 你不可以：将本仓库内容用于**商业目的**（如直接售卖、以盈利为导向的二次分发）。
- 各子项目（sonder520、Nymir、xy-club、xy-intro-card、九溪 jiuxi、时念 shinian、书时 TailTale）的代码与文档采用各自独立的许可证，且**代码与文档往往不是同一个许可证**（例如多数项目的文档为 CC 系列、九溪内容为非商业、书时代码为 Apache-2.0）。请以各项目仓库内的 `LICENSE` 与 `LICENSE-DOCS` 文件为准——本仓库的 CC BY-NC 4.0 只覆盖**本仓库自身**的文字与编排内容。

许可证完整文本见仓库根目录 [`LICENSE`](./LICENSE) 文件，或访问 <https://creativecommons.org/licenses/by-nc/4.0/deed.zh>。

---

<div align="center">

*AI 时代的个体赋能，慢慢来，一起看它会把普通人推到哪一步。*

---

[English](./README.en.md) | **简体中文**

*最后更新：2026-10*

</div>
