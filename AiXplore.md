---
type: project
title: "AiXplore — Community Concierge for Senior Immigrants"
status: active
created: 2026-10-16
updated: 2026-10-16
tags: [AiXplore, community-concierge, senior-immigrants, PGP, Super-Visa, SDG-10, SDG-3]
source: []
related: [[项目/AiXplore/AiXplore_Sprint2_Script]]
owner: "Ivy Team"
confidence: high
---

# AiXplore

## 一句话定位

> **AiXplore 是一个多语言、多渠道的社区活动 concierge app，帮 50+ 新移民父母/祖父母（PGP / Super Visa）发现、理解、参加并持续参与附近的社区活动。AI 做匹配、翻译、排程、follow-up。老人看到的是 "图书馆的电脑助手，Sarah 帮我设的"，不是一个 robot。**

## 核心命题

Family reunification 解决了 "团聚"，但没解决 "归属"。50 万 PGP/Super Visa 老人每年到加拿大，面对三个复合障碍：
1. 社区活动散落在几十个网站/calendar，全是 formal English
2. 87% PGP 申请者依赖 sponsor (子女) 才能参与
3. 一次参加 ≠ 习惯，网络/routine 会 fading

**竞品空白**: 没有人做 "帮你找 + 帮你记 + 帮你去 + 帮你再来" 的 loop。Library 有 program 但没 concierge。City 有 calendar 但没人翻译。NGO 有活动但覆盖不到。

## 产品形态

### App-first（不是 WeChat-first）

- **App 是主界面**：日历、朋友、习惯、"跟 Pulong 说话"
- **Channel 是可选的**：App 里 "跟 Pulong 说话" 按钮 → 自动走她选的 channel
  - 中文用户 → WeChat
  - 菲律宾/印度/巴西/墨西哥 → WhatsApp
  - 70+ 只用电话 → 电话
  - 所有人 → SMS 兜底
- **不锁死任何平台**。App 是多语言的，Pulong 推送到对应 channel。

### 多语言支持

| 语言 | Channel | 备注 |
|------|---------|------|
| 中文 (Mandarin/Cantonese) | WeChat | 中国 PGP |
| Tagalog | WhatsApp | 菲律宾 PGP |
| Hindi / Telugu / Tamil | WhatsApp | 印度 PGP |
| Spanish | WhatsApp | 墨西哥 PGP |
| Portuguese | WhatsApp | 巴西 PGP |
| Ukrainian | SMS | 乌克兰难民 |
| 英语 (低素养) | 电话 | 兜底 |

**App 界面随用户语言切换。Pulong 消息也切换。互不影响。**

## Pulong 的身份

### Pulong 是 AI，但不对老人说 "AI"

| 对谁 | 怎么说 | 为什么 |
|------|--------|--------|
| **老人 (Lola)** | "图书馆的**电脑助手**。不是真人，是程序帮你找活动。" | "AI" 对她 = 陌生科技词 = 可能是骗子。"电脑程序" 她懂。 |
| **子女 (Sarah)** | "app 用 AI 帮她匹配活动和翻译" | 她数字素养高，知道是什么 |
| **Library (staff)** | "AI 驱动的社区 engagement 工具" | 他们付钱买 outcome，不是 "AI" 本身 |
| **Pitch (judge)** | "AI-native community concierge" | 这是 tech story |

### 诚实披露原则（道德底线）

**不说 "我不是机器人"。说 "是的，是程序。"**

| 原则 | 落地 |
|------|------|
| 承认自动化 | "这是电脑助手，不是真人看你的消息" |
| 不编造人设 | 不说 "Maria 是你的朋友"，说 "Maria 参加了，反馈好，她下周三也去" |
| 不过度情感化 | 不假装关心，只说事实 + 选项 |
| 给退出选项 | "跟 Sarah 说停就停，24h 删除数据" |
| 具体说存什么 | "只存活动名+日期+反馈。不存身份证/银行/病历" |

**如果她问 "你是机器人吗？"：**
> "是的，我是电脑程序，图书馆的。Sarah 帮你的。我帮你找活动、提醒你。不是真人在看。但所有信息是真的，来自图书馆和活动场地。你随时可以让 Sarah 关掉我。"

**为什么不说 "AI" 而说 "电脑助手"：**
- 对 64 岁他加禄语使用者，"AI" 没有意义
- "电脑程序" 她懂（她用手机）
- 这不是欺骗，是 **ethics-aware disclosure**：披露自动化，不用她不懂的词
- Pitch 时这是加分项："我们设计了符合用户认知水平的披露方式"

## 三层结构

```
┌─────────────────────────────────────────────────────┐
│  SUPPLY (数据源)          SERVICE (AI 引擎)    DEMAND (用户) │
│                                                      │
│  Libraries / City     聚合 + 匹配 + 翻译     50+ Senior │
│  / NGOs / Community   / 排程 + follow-up    子女        │
│  centers / 志愿者      / 习惯追踪            (Channel)  │
│                                                      │
│  "发布活动到 feed"     "帮老人找到、记住、    收到推送、   │
│  (form/RSS/CSV)       去、再来"             回 '好'    │
└─────────────────────────────────────────────────────┘
```

- **Supply 不需要知道 Demand 是谁**。它们只发布活动。
- **Demand 不需要知道 Supply 有几家**。她只看到 "周三有种花"。
- **Service (AI) 做中间**：匹配、翻译、排程、追踪。

## 8 个 User Journeys

### J1: 子女装 App (Sarah 手机, 5 分钟, 只做一次)

```
Sarah 手机:
  下载 AiXplore app (icon: 🌿 大, 清晰)
  → "Help your parent" → 登录 (Sarah 账号)
  
  Step 1: "Mama 住哪?" → 15 Wilton Ave, North York
  Step 2: "Mama 讲什么?" → Tagalog
  Step 3: "Mama 喜欢什么?" → 户外 / 社交 / 不赶时间
  Step 4: "Mama 手机用什么?" → WhatsApp
  Step 5: 确认 → "Pulong 已准备好"
  
  → 在 Lola 手机上装好 app (Apple ID 共享)
  → 设好语言: Tagalog · 设好通知: 7am
  → 把手机给 Lola: "妈，我帮你装了图书馆的 app。
     它帮你找附近可以做的事。你不用管，它帮你安排。"
  → 完。
```

### J2: Lola 第一次打开 App (30 秒)

```
Lola 手机, 看到 🌿 图标, 点开:

  ┌─────────────────────────────────┐
  │  [图书馆 logo]  North York PL  │
  │                                 │
  │  Hi Lola,                       │
  │  Sarah (你女儿) 帮你设了这个。  │
  │  这是图书馆的电脑助手。        │
  │  不是真人, 是程序帮你找活动。  │
  │                                 │
  │  它知道的: 你住哪、讲什么语     │
  │  它不知道的: 身份证、银行、病历 │
  │                                 │
  │  明天: 🌿 Garden Club         │
  │  周三 10am · 免费 · Maria 也去 │
  │                                 │
  │  [开始]  [跟 Sarah 确认]       │
  │  By NYPL · 跟 Sarah 说停就停   │
  └─────────────────────────────────┘
```

- **一屏看完**。没有注册、登录、同意条款、完善资料。
- **诚实披露**: "不是真人, 是程序"
- **信任闭环**: "跟 Sarah 确认" 按钮 → 她问女儿 → 女儿说 "对, 图书馆的"

### J3: 日常 (Lola 的 App, 每天 10 秒)

```
7am 推送通知: "🌿 明天 10 点 Garden Club · 25 路 3 站 · Maria 也去"

Lola 看到 → 知道了 → 完。

或者打开 app:
  Home = 一张大卡片:
  "明天: Garden Club
   10:00 · NYCC 正门
   25 路 Wilton Ave 上, 3 站
   免费 · Maria + Ana 也去
   [我要去 ✓]  [不去了]"
  
  就这一个卡片。下面没有 feed。没有推荐。没有 "更多"。
```

### J4: "跟 Pulong 说" (10 秒)

```
App 底部大按钮: "跟 Pulong 说话"
  → 自动选她的 channel (WhatsApp / WeChat / 电话 / SMS)
  → 直接打开对应 app 给 Pulong 发语音/消息
  → 或打电话给 Pulong (真人接, 不是 bot voice)

Lola 说: "下周三我还去"
  → Pulong 记录 → 自动排 → 推通知 "记了，下周三 7am 提醒"
```

### J5: 参加后 (in-app, 3 个 tap)

```
周三 12:30pm 通知: "今天怎么样？"
Lola 打开 app:
  [今天开心吗?]
  [😊 好]  [😐 一般]  [😔 不好]
  
点 "好" → "Maria 还在吗？下周三还来吗？" → [来] [不来]
点 "来" → "好，下周三我帮你记了。🌿"
→ Sarah 收到通知: "Mama 参加了 ✓ 说 Maria 很好"
```

### J6: 习惯里程碑 (第 3 周, 全屏, 1 分钟)

```
Lola 打开 app → 全屏:

  ┌─────────────────────────────────┐
  │         🎉 3 周了！            │
  │                                 │
  │  你连续 3 个周三去了           │
  │  Garden Club。                 │
  │                                 │
  │  Maria 参加了, 反馈好。        │
  │  Ana 下周三也去。              │
  │                                 │
  │  "妈妈现在自己出门了，         │
  │   我很放心" — Sarah           │
  │                                 │
  │  [截图发家族群]               │
  │                                 │
  │  By North York Library         │
  └─────────────────────────────────┘
```

**情感时刻。不是 "score 75/100"。是 "你女儿说放心了"。**

### J7: "不去了" (5 秒)

```
Lola 打开 app → 明天 Garden Club 卡片 → 点 "不去了"
  → "好的。这周不去了。你腰好一些的话，下下周三我再问。
     跟 Sarah 说一下？"
  → [说] [不说]
  
点 "说" → Sarah 收到 "Mama 腰疼，暂停了"
→ Pulong 暂停 2 周。之后问 "腰好了吗？"
```

### J8: 子女失联兜底 (Sarah 手机, 被动)

```
Pulong 72h 没收到 Lola 任何回复:
  → Sarah 收到通知: "Mama 48h 没回复了。Pulong 暂停了。要不要打个电话？"
  → Sarah 打电话: "妈，你还好吗？"
  → Lola: "手机没电了。"
  → Sarah 在 app 标记 "Mama 好了" → Pulong 恢复
```

## 诈骗防范设计

| 老人担心的 | App 怎么解决 |
|-----------|-------------|
| "这是什么 app？" | 第一屏: "Sarah 帮你设的。图书馆的。帮你找活动。" |
| "是不是要钱？" | 没有支付、没有订阅、没有 premium。只有免费活动。 |
| "它知道我的信息？" | 第一屏说清: 只知道住哪、讲什么语、喜欢什么。不存身份证/银行/病历。 |
| "怎么退出？" | 底部常驻: "跟 Sarah 说停就停。24h 删数据。" |
| "发件人是谁？" | 每屏右上角: 图书馆 logo + "By North York Public Library"。 |
| "是不是骗子？" | 子女当面装的 + 每屏有机构名 + 不要求任何输入 + 有 "跟 Sarah 确认" 按钮 |

## App 结构 (老人端, 极简)

```
AiXplore App
├── Home (主屏, 唯一)
│   ├── 一张大卡片: "明天/最近的事" (活动名 + 时间 + 路线 + 谁去)
│   ├── [我要去] [不去了] 两个大按钮
│   ├── "跟 Pulong 说话" (大按钮 → 她的 channel)
│   └── 底部: "By NYPL · 跟 Sarah 说停就停"
│
├── 朋友 (3-5 人)
│   ├── 头像 + 名字 + "同组 X 周"
│   └── "下周三谁去"
│
└── 我的
    ├── 语言 / 住哪 / 喜欢什么 (只读, 不能改)
    ├── "我去了 X 次" (大数字)
    └── "跟 Sarah 说停就停" (红色, 常驻)
```

**3 个 tab。没有搜索、feed、推荐、设置、通知管理、"更多"。**

### 子女端 (App 内, Sarah 用)

```
├── Setup (3步, 2分钟, 只做一次)
├── "Mama 这周" (活动 + 状态 + 习惯进度)
├── 通知 feed ("Mama 参加了 ✓" / "72h 没互动")
└── 设置 (通知频率 / channel / 暂停)
```

### Staff 端 (Web Dashboard, 图书馆用)

```
├── Dashboard (KPI + alerts + 活动热度)
├── Seniors (列表 + 详细档案 + journey timeline)
├── Activities (列表 + 发布表单)
├── Pulong Log (每条消息 + 回复)
├── Feed Sources (RSS/iCal/CSV 管理)
└── Weekly Report (给 Director 看的)
```

## 关键设计约束

### 信任

- 子女当面装 app (不是老人自己下载)
- 第一屏必须提到子女名字 + 机构名 (双信任锚)
- 诚实披露: "是电脑助手, 不是真人" (不说 "AI", 不说 "我不是机器人")
- "跟 Sarah 确认" 按钮 (信任闭环)
- 每屏有图书馆 logo (机构背书)

### 简洁

- 一屏一件事
- 大字体 (≥14px), 大按钮 (≥48px)
- 不要求老人输入任何东西 (全部 tap / 语音)
- 一条消息只说一件事
- 不编造社交关系 ("Maria 参加了" 而不是 "Maria 是你的朋友")

### 安全

- 不要求验证身份
- 不推荐付费活动 (Pilot 只有免费)
- 一天不超过 2 条通知
- 老人说 "不去" 就不追问
- 72h 无互动 → 通知子女 (不是通知老人)
- "跟 Sarah 说停就停, 24h 删数据"

### 不过度

- 不创建 multi-agent 架构 (Pilot 不需要)
- 不做 microservices (Pilot 一个 app + 一个 feed 就够)
- 不做 "AI 朋友" (Pulong 是工具, 不是陪伴)
- 不假装关心 ("Maria 反馈好" 而不是 "Maria 很想见你")
- 不做 "智能推荐 feed" (每天 1 个活动, 不是 50 个)

## 三个 Stakeholder

| 角色 | 用什么 | 打开频率 | 做什么 |
|------|--------|---------|--------|
| **Beneficiary (50+ senior)** | App (辅) + Channel (主, WeChat/WhatsApp/SMS/电话) | Channel: 每天。App: 每周 1-2 次, 30 秒 | 收到通知 / 回 "好" / 参加 / 形成习惯 |
| **Channel (子女, 30-50)** | App | 1 次 setup + 偶尔看通知 | setup / 看 "Mama 这周" / 72h 失联时打电话 |
| **Payer (City / Library)** | Web Dashboard | 每天 | 看报告 / 发布活动 / 处理 alerts |

## North Star Metric

**Meaningful community participations per active user per month** (参加了 + 还会再来)

辅助指标:
- Return rate: 去了 3+ 次的 senior 占比 (习惯建立率)
- 子女 "放心分": "Mama 不需要我帮她找活动了" 的占比
- Library "触达分": 通过 AiXplore 触达的 PGP senior 数 (vs 之前的 0)

## 当前状态

**Sprint 2** — 已完成 pitch (PPT + script)，prototype 进行中。

## 文件

| 文件 | 说明 |
|------|------|
| `AiXplore_Sprint2_Script.md` | Sprint 2 pitch 口播稿 |
| `AiXplore_Sprint2_Presentation.pptx` | Sprint 2 PPT |
| `prototype/AiXplore_Workstation_v2.html` | Staff dashboard 原型 (6 pages + phone simulator) |
| `prototype/AiXplore_Senior_App.html` | 老人 app 端原型 (v1, 需按新设计更新) |
| `docs/generate_sprint2_*.py` | PPT 生成脚本 |

## 变更记录

| 日期 | 变更 |
|---|---|
| 2026-09-18 | 从 AI-Literacy-Bridge 分拆 |
| 2026-10-16 | 确认三层结构、子女 setup 为 trust anchor、Return 为飞轮 |
| 2026-10-16 | **重大更新**: (1) App-first 取代 WeChat-first, 多渠道不锁死平台; (2) Pulong 身份: AI 但披露为 "电脑助手", 不说 "AI", 不说 "我不是机器人"; (3) 8 个 user journey 定义; (4) 诈骗防范 4 重设计; (5) 道德底线: 不编造人设, 不过度情感化, 给退出选项; (6) App 极简: 3 tab, 没有搜索/feed/设置 |
