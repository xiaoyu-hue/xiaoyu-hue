<div align="center">

[简体中文](./README.md) | **English**

# ✦ xiaoyu-hue

### An ordinary person with no programming background, treating AI Agents as a new kind of production tool — and using real projects to test how far they can push the boundaries of what a non-programmer can build.

[![GitHub](https://img.shields.io/badge/GitHub-xiaoyu--hue-181717?style=for-the-badge&logo=github)](https://github.com/xiaoyu-hue)
[![Original Projects](https://img.shields.io/badge/Original%20Projects-4-4FC08D?style=for-the-badge)](https://github.com/xiaoyu-hue?tab=repositories)
[![Built with](https://img.shields.io/badge/Built%20with-AI%20Agent-646CFF?style=for-the-badge)](https://github.com/xiaoyu-hue)
[![Last update](https://img.shields.io/badge/Last%20update-Sep%202026-9A8CFF?style=for-the-badge)](https://github.com/xiaoyu-hue)

**Four original projects · All open source · All honestly documenting what they can't do**

</div>

---

## Table of Contents

- [All Four Projects at a Glance](#all-four-projects-at-a-glance)
- [Quick Start](#quick-start)
- [Who I Am](#who-i-am)
- [Project 1: sonder520](#project-1-sonder520)
- [The Second Idea: Nymir](#the-second-idea-nymir)
- [The XY Series: xy-club and xy-intro-card](#the-xy-series-xy-club-and-xy-intro-card)
- [What This Experiment Is Testing](#what-this-experiment-is-testing)
- [How I Work with AI](#how-i-work-with-ai)
- [What These Projects Can't Do](#what-these-projects-cant-do)
- [Contact and Feedback](#contact-and-feedback)
- [My Limitations and Choices](#my-limitations-and-choices)

---

## All Four Projects at a Glance

| Project | What it is | Scale | Tech stack | License |
|---|---|---|---|---|
| 🌊 **[sonder520](https://github.com/xiaoyu-hue/sonder520)** | Local personal work & life management tool; your data never leaves your browser | 12 modules · 770+ tests · v6.x | HTML/CSS/vanilla JS · IndexedDB · PWA | MIT |
| ✦ **[Nymir](https://github.com/xiaoyu-hue/Nymir)** | Anonymous tree hole · P2P encrypted chat · messages vanish when read | 293 tests · v1.6.x | React 19 · TypeScript · Vite · WebRTC | AGPL-3.0 |
| 💎 **[xy-club](https://github.com/xiaoyu-hue/xy-club)** | Reusable club website template + visual admin panel | 7 section types · 4 themes · 73 tests | Node.js · Express · JSON | MIT |
| 🪪 **[xy-intro-card](https://github.com/xiaoyu-hue/xy-intro-card)** | Personal intro card generator; just double-click to use | Single file · 2 modes | Single-file HTML | MIT |

**Maintenance status (updated Sep 2026):** all four projects are still maintained, but at a **slower pace than before** — my main device broke, and I'm updating from a backup one until I can get a new machine. They are not abandoned. If you're deciding whether to depend on one of them, please read its own README first.

> The other two repositories, `cs-self-learning-XY` and `free-programming-books-XY`, are forks of learning resources, not original work.

---

## Quick Start

Every project has a live version — you don't need to install anything to try them.

| Project | Try it online | Run it locally |
|---|---|---|
| 🌊 **sonder520** | [xiaoyu-hue.github.io/sonder520](https://xiaoyu-hue.github.io/sonder520/) | `git clone` the repo, then open `index.html` in your browser (Chrome / Edge recommended) |
| ✦ **Nymir** | [xiaoyu-hue.github.io/Nymir](https://xiaoyu-hue.github.io/Nymir/) | `git clone` → `cd Nymir` → `npm install` → `npm run dev` |
| 💎 **xy-club** | [xiaoyu-hue.github.io/xy-club](https://xiaoyu-hue.github.io/xy-club/) | `git clone` → `pnpm install` (or `npm install`) → `node server.js`; site at `localhost:3000`, admin at `localhost:3000/admin` |
| 🪪 **xy-intro-card** | [xiaoyu-hue.github.io/xy-intro-card](https://xiaoyu-hue.github.io/xy-intro-card/) | Download the single HTML file and double-click it — works offline |

Full setup details, environment requirements and dev commands live in each project's own README. Issues and pull requests are welcome; for **Nymir**, please read its security limitations before reporting or depending on it.

---

## Who I Am

I have zero programming background — I've never even gone out of my way to study it. Before I encountered AI Agents, "turning my own ideas into working software" simply wasn't an option for me.

After discovering AI Agents, that door opened. It turns out someone who can't code can still turn ideas into websites, web apps, even a PWA.

I have no plans to become a programmer. I build these projects to answer one concrete question:

> **When the production tool changes from "programming languages" to "AI Agents," how far can a non-programmer actually go?**

The four projects below are four answers to that question. They are not tutorial exercises — they are real things, actually running and actually used: all four have live sites, the main projects pass CI test gates, and sonder520 alone runs 770+ tests.

---

## Project 1: sonder520

**From "following a tutorial" to "figuring it out myself"**

It started with a v1 built by following a blogger's tutorial. Everything after that, I figured out on my own.

I especially love ink-wash style and liquid-glass style, and I kept wondering: could the two be combined? I tried — and it actually worked. Later I felt it lacked a background, so I used my favorite wallpaper; then I felt it lacked personality, so I added a custom-wallpaper feature with adjustable transparency to match the overall look.

<div align="center">

> **sonder** · the passerby &nbsp;|&nbsp; **520** · a gift to myself

</div>

That's where the name comes from.

### From Local to Live

The tutorial version could only run on my own machine, and I wanted other people to see it too. So I asked AI how to deploy it online, and it recommended several static hosting platforms.

**The first platform I deployed to was Netlify** — my first time ever completing a deployment myself. Later, after I ran out of free Netlify deployments, I set up GitHub Pages and Cloudflare Pages as well. From then on, deployment sync has been handed over to the AI Agent.

### From Workspace to Personal OS

From v1.0, step by step, to v6.x: 12 modules, 770+ tests, PWA offline support, optional encrypted storage. The modules are nearly enough — but cross-module collaboration still has plenty of room to grow.

I don't think it can be called a "personal workspace" anymore. It's closer to a **personal OS**.

| | |
|---|---|
| 🔗 Live | [xiaoyu-hue.github.io/sonder520](https://xiaoyu-hue.github.io/sonder520/) |
| 🛠 Tech | HTML / CSS / vanilla JS · IndexedDB · WebCrypto · PWA — zero runtime dependencies, zero build |
| 📄 License | MIT |

---

## The Second Idea: Nymir

After finishing sonder520, another question was on my mind:

> Is there a place to talk things out that puts safety, privacy, and anonymity first — one that **no centralized server can ever log**?

Chat apps like WhatsApp, Telegram, Discord, QQ and WeChat are centralized services: your chat history usually sits on their servers. Nymir has no business servers and doesn't record your data — your data lives only in your own browser. Anonymity is built on end-to-end encryption, names are randomly generated, and there is no sign-up.

At its core, it is a **tree hole** — a safe place to pour your heart out.

<div align="center">

```
User A ════ 🔐 ════ P2P direct connection ════ 🔐 ════ User B
                  No business servers
```

</div>

The visual identity is liquid-glass style + a starry-sky theme.

Of course, **this is not absolutely secure**. The stack is cutting-edge (X25519 key agreement, per-message HKDF, Ed25519 signatures over ciphertext), but I'm only standing on the shoulders of giants to realize my own idea — **I am not a cryptography expert**. Every known limitation is documented honestly in the README. Nothing is hidden.

| | |
|---|---|
| 🔗 Live | [xiaoyu-hue.github.io/Nymir](https://xiaoyu-hue.github.io/Nymir/) |
| 🛠 Tech | React 19 · TypeScript · Vite · Trystero / WebRTC · 293 tests |
| 📄 License | AGPL-3.0 |

---

## The XY Series: xy-club and xy-intro-card

After building two things for myself, I wanted to build something **other people could pick up and use directly**.

### xy-club: A Club Website Template

Most club websites out there are either ugly, hard to customize, or a pain to deploy. I wanted to prove one point: **zero build, zero dependencies, a single JSON file — and you can still get a liquid-glass website with micro-interactions, a visual admin panel, and pure static hosting, as a reusable template.**

The public site and the admin panel share a single JSON data file: whatever you change in the admin panel is instantly what the site shows. No rebuild, no coding. **Switch to another club: change the content, change the theme — never the code.**

### xy-intro-card: A Personal Intro Card Generator

Another tool from the same family: personal intro cards for members. A zero-dependency single file — fonts, icons, and avatars all embedded. It opens even without internet, and sending it to someone is sending one standalone card.

| | |
|---|---|
| 🔗 xy-club Live | [xiaoyu-hue.github.io/xy-club](https://xiaoyu-hue.github.io/xy-club/) |
| 🔗 xy-intro-card Live | [xiaoyu-hue.github.io/xy-intro-card](https://xiaoyu-hue.github.io/xy-intro-card/) |
| 🛠 xy-club | Node.js · Express · JSON storage · 73 tests · MIT |
| 🛠 xy-intro-card | Single-file HTML — zero dependencies, zero network · MIT |

> `XY` is just the naming prefix for this project series. **The "XY Club" is the default demo case, not a dedicated brand** — swap in any club or team's content, and the tool logic stays exactly the same.

---

## What This Experiment Is Testing

The four projects were not built at random. Each one answers a specific question:

| Project | The boundary it probes |
|---|---|
| **sonder520** | How much engineering discipline can a non-programmer's project have? — 770+ tests, 14 ADRs, layered architecture, CI gates |
| **Nymir** | Can someone with zero background work with cryptography? — End-to-end encryption runs fine, but it's also the project that demands the most of your caution |
| **xy-club** | How low can the bar go for a good-looking, easy-to-edit, easy-to-deploy website? — Zero build, zero database, one JSON file drives the whole site |
| **xy-intro-card** | How simple can a tool be? — One HTML file; double-click to open, ready to use |

---

## How I Work with AI

I don't know much of anything, so whenever I hit a problem, I ask AI. But I never take its answers wholesale — **I make it translate the jargon into words I can understand, weigh it myself, and only adopt it once I'm convinced.**

I often toss wild, unfiltered ideas at the AI Agent — as an outsider, my imagination knows no bounds. Sometimes it interrupts and tells me something won't work, but it also offers an alternative that comes close to what I had in mind, and I make my choice based on its suggestions.

<div align="center">

| My role | AI's role |
|:---:|:---:|
| Propose ideas · Make judgments · Choose options | Translate jargon · Offer options · Implement |

</div>

### Three moments where the judgment was mine

Rules are easy to write down; what matters is what actually happened. Three real cases from building these projects:

| What happened | What the AI did | What I decided |
|---|---|---|
| **Going online for the first time** | Recommended several static hosting platforms | It gave me a shortlist, not an order. I picked **Netlify** for my first deployment and did it myself. When I ran out of free deployments, I moved on to GitHub Pages and Cloudflare Pages. |
| **Mixing ink-wash with liquid glass** | Couldn't promise the two styles would work together | I wanted it, so I just tried. It worked — and that combination became sonder520's entire visual identity. **Sometimes "try first, ask later" is the right order.** |
| **Drawing the line on Nymir's security** | Wrote the crypto code (X25519, HKDF, Ed25519) without difficulty | Code is not a guarantee. I'm not a cryptographer, so I wrote "no professional security audit" and "not recommended for real sensitive use" into the README myself. **AI's capability boundary is something I have to draw.** |

These rules live in an `AGENTS.md` in every project: confirm requirements before starting work; break big tasks into small, verifiable steps delivered one by one; every tech choice must come with a reason and my approval; irreversible actions (deleting files, overwriting code, paid services, public releases) require my consent first; uncertainty must be stated honestly; every proposal must explain its trade-offs.

**The code is written by AI. The judgment is mine.**

---

## What These Projects Can't Do

If this is an "experiment," the failures belong on the record too. All of the following are listed honestly in each project's README:

| Project | Not suitable for / Known limitations |
|---|---|
| sonder520 | No automatic cross-device sync (manual backup import only), no team collaboration, not a native app, browser data may be cleared |
| Nymir | **No professional security audit**, TOFU (trust-on-first-use) has weaknesses, public signaling servers can observe metadata, limited traffic-obfuscation strength, no offline inbox |
| xy-club | Single-password auth with no multi-admin support, no CSRF protection, single-process file reads/writes, no SSR/SEO, not suitable for payment sites |
| xy-intro-card | Pure front-end single file, no backend storage, no multi-user collaboration, no complex animations |

**A special warning for Nymir**: the author is not a programmer by training and the code has not been professionally security-audited. **It is not recommended for real, sensitive use cases.**

---

## Contact and Feedback

I'm glad you're here. Feedback is welcome — and so is hearing how these projects are being used.

| | |
|---|---|
| 💬 Bug reports & ideas | Open an issue in the relevant repository. Please include what you did, what you expected, and what happened — screenshots help a lot. |
| 🤝 Pull requests | Welcome. For anything structural (architecture, dependencies, security-related code), please open an issue first so we can agree on the direction before you write code. |
| 🌏 Language | Issues in both Chinese and English are fine. English is fine even if it's simple — I read with AI assistance. |
| 🙅 Not taking | Paid custom development, security audits of other people's projects, homework help, and "please fix my code" requests. |
| ⚠️ About Nymir | Please don't use it for genuinely sensitive conversations — see the limitations above. Security questions are welcome as discussion, not as a guarantee. |

Replies may be slow: I'm maintaining these projects from a backup device, and everything I do goes through one person.

---

## My Limitations and Choices

I know my biggest limitation all too well: **I lack hard programming skills, so much of what I do depends on AI.** AI suggests; if I think a suggestion is good, I take it — if not, I ask whether there's another way. That's how, step by step, these four projects came to be.

I've also wrestled with doubt: am I taking up public space on GitHub? Should I set these repos to private, or just delete them? But I deeply admire the spirit of open source, so all of my projects will stay open — even though the code is still being polished.

That's why you'll find some uncommon things in these repositories: READMEs that state "what this is not suitable for," "known limitations," and "no professional security audit."

**That's not modesty. That's honest labeling.**

**In the words of my favorite saying — offered to myself, and to everyone who visits this little corner of GitHub: "Stay curious. Keep exploring. Give it a try. Put it to the test." May we all keep going.**

---

<div align="center">

*Individual empowerment in the AI era. May we witness the AGI of the future together — and humanity's fourth industrial revolution.*

---

[简体中文](./README.md) | **English**

*Last updated: Sep 2026*

</div>
