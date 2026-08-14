# Kimi Design Refer

> A portable Agent Skill for a **Kimi-inspired quiet computational design system**, extended with a restrained **Zine Editorial** layer.
>
> 一个把「审美」变成可重复调用设计规则的 Agent Skill。

`kimi-design-refer` 不是一条固定 Prompt，也不是只会生成某一种海报的模板。

它是一层 **Design Reference / Style Router**：让 Codex、Cursor、Trae、OpenHands 或其他支持 Agent Skills / 本地指令文件的 Agent，在设计网站、PPT、PDF、海报、社交媒体图片、信息图与动态视觉时，可以先加载同一套视觉语言，再完成具体任务。

当前系统包含：

- **7 个 Kimi Core Families**：偏计算、研究、证据、实验与技术叙事；
- **5 个 Zine Editorial Families**：偏纸张、档案、极端留白、印刷与诗性编辑；
- **6 种 Medium Routes**：Web、PPT/PDF、Poster、Infographic、Motion、Review；
- **Kimi × Zine Blend**：允许一个 Core Family 与一个 Zine Family 按强度融合。

---

## 设计核心

Kimi Design Refer 的基础公式是：

```text
quiet field
+ bounded evidence system
+ technical hierarchy
+ visible process
+ restrained anomaly
```

可以理解为：

> **一个安静的大场域 + 一个受控的信息事件 + 清晰的技术层级 + 可见的思考过程 + 一个克制的异常点。**

它刻意避免把「AI 感」理解成蓝紫渐变、发光大脑、玻璃卡片、赛博城市和满屏节点。

这里更强调：

- 大面积留白；
- 一个主视觉事件；
- 轨道、测量、索引、点云、证据、状态变化等 reasoning traces；
- 微型注释与编号；
- 黑 / 白 / 灰为基础的克制颜色体系；
- 过程感，而不是纯装饰。

---

# 12 Visual Families

## Kimi Core Families

| Family | 中文 | 核心视觉 | 适合 |
| --- | --- | --- | --- |
| `black-orbit` | 黑域轨道 | 黑色场域、巨大轨道/膜结构、细线节点 | Agent Network、生态、协作、系统 |
| `pixel-moon` | 像素登月 | 黑白像素、Dither、月球/入口、低比特界面 | 开源、开发者、探索、Builder Culture |
| `white-lab` | 白场实验室 | 冷白实验场、测量工具、点云、等高线 | 研究、工具、模型架构、分析流程 |
| `cosmic-index` | 宇宙索引 | 浅色知识场、天体标本、索引、Serif + Mono | 研究发布、知识、模型、报告 |
| `gray-proofboard` | 灰域证据板 | 中灰场、一个证据碎片、`001 /`、微注释 | 产品能力、案例、规则、研究结论 |
| `kinetic-glyph` | 字符变形 | 一个符号在笔触 / 粒子 / 几何之间变化 | Slogan、版本发布、抽象概念 |
| `simulation-window` | 模拟窗口 | 单一高信息彩色窗口 + 安静单色外壳 | 数据模拟、3D、Demo、动态结果 |

### Core Family 的共同底层

每一个 Kimi Core Family 都应该保留至少几个共同特征：

```text
极端场域对比
单一生成系统
受控的信息密度
技术层级
一个异常点
过程 > 装饰
```

---

## Zine Editorial Extension

Zine Extension 不是把所有 Kimi 设计都变成“旧纸风”。

它是一个可选的编辑层，用于引入：

- 70%–90% 的极端留白；
- 一个很小的视觉事件；
- 纸张、扫描、Xerox、Risograph、Halftone 等 reproduction language；
- 稀疏的 Serif / Mono / Typewriter typography；
- 一个清晰的高饱和色锚点。

当前整理为 5 个可稳定调用的家族：

| Family | 中文 | 核心视觉 | 适合 |
| --- | --- | --- | --- |
| `zine/micro-archive` | 微型档案 | 80% 左右留白 + 一个小型档案证据 | 研究封面、观点、规则记录 |
| `zine/dual-memory` | 双联记忆 | 两个小画面形成前后 / 对比关系 | Signal vs Noise、前后变化、双状态 |
| `zine/color-cutout` | 色块剪贴 | 图像碎片 + 一个强烈高饱和色块 | Campaign、事件、冲突、重点信息 |
| `zine/type-relic` | 文字遗物 | Typography 本身成为主视觉标本 | Slogan、章节页、品牌声明 |
| `zine/orbit-notes` | 漂移注记 | 小主体 + 远距离注释 / 日期 / 坐标 | 研究笔记、地图、技术叙事 |

---

# Kimi × Zine

一个设计可以：

1. 只使用一个 **Kimi Core Family**；
2. 只使用一个 **Zine Editorial Family**；
3. 使用 **一个 Core + 一个 Zine** 进行融合。

不要平均混合所有家族。

推荐的融合强度：

```text
zine-light    15–25%
zine-medium   30–45%
zine-full     60–80%
```

例如：

```text
Core family: gray-proofboard
Zine family: zine/micro-archive
Zine intensity: medium
```

得到的就不是纯数字证据板，也不是纯独立杂志，而是：

> Kimi 的理性、计算、证据感
> +
> Zine 的纸感、档案感、诗性留白。

---

# Supported Mediums

调用 Skill 时，可以先声明媒介：

```text
web-ui
ppt-pdf
poster-social
infographic
motion
review-only
```

### `web-ui`

适合网站、Landing Page、产品页和 Dashboard 的视觉方向。

优先保证真实 UI 可用性、HTML/CSS 文本可读性，再应用大场域、编号章节、证据窗口和克制交互。

### `ppt-pdf`

适合研究报告、机构资料、发布 Deck。

重点不是逐页随机换风格，而是建立一条贯穿 Title → Chapter → Evidence → Data → Closing 的视觉主线。

### `poster-social`

适合海报、公众号封面、小红书、社交媒体视觉。

应把内容收敛成：

```text
一个命题
+ 一个视觉事件
+ 一个明确 Family
```

### `infographic`

准确性优先于艺术性。

能用 HTML / SVG / Vector / Editable Layout 表达的文字与数据，不应该全部交给图片模型随机绘制。

### `motion`

先选一个 Motion Verb：

```text
orbit
converge
calibrate
reveal
index
dissolve
simulate
```

然后让动作继承静态视觉系统，而不是单独做一套“炫酷动效”。

### `review-only`

用于审查已经完成的设计。

Agent 会重点检查：

- Family Fidelity
- Negative Space
- Information Density
- Hierarchy
- Reasoning Trace
- Color Discipline
- Originality
- Readability

---

# Installation

## Codex

```bash
git clone https://github.com/78tyih/kimi-design-refer.git \
  ~/.codex/skills/kimi-design-refer
```

如果 Skill 没有立即出现，重新启动对应 Agent / Codex 会话。

## Other Agent Runtimes

如果你的 Agent 支持本地 Skills / Instructions，把整个仓库复制或克隆到对应的 Skills 目录即可。

核心入口文件是：

```text
SKILL.md
```

即使运行环境不支持自动发现 Skill，也可以让 Agent 读取 `SKILL.md` 与 `references/` 后执行。

---

# Quick Start

最简单的调用方式：

```text
Use $kimi-design-refer.

为这个 AI 产品设计一张宣传海报。
```

指定 Family：

```text
Use $kimi-design-refer.

Medium: poster-social
Family: black-orbit
Density: whisper

为一个 AI × Trading 产品设计海报。
```

使用 Zine：

```text
Use $kimi-design-refer.

Medium: poster-social
Family: zine/micro-archive

做一张研究型海报。
保持约 80% 留白，只保留一个小型证据事件。
```

混合调用：

```text
Use $kimi-design-refer.

Medium: poster-social
Core family: gray-proofboard
Zine family: zine/color-cutout
Zine intensity: medium

为产品的新功能发布设计海报。
```

---

# Example — PropFirm.TV

我们使用同一套内容测试过全部视觉家族。

基础文案：

```text
propfirm.tv
Prop Firm Intelligence

规则追踪 · 出金资讯 · 平台对比 · 市场动态

Track. Compare. Decide.
```

例如：

```text
Use $kimi-design-refer.

Medium: poster-social
Family: cosmic-index

为 PropFirm.TV 设计一张 4:5 宣传海报。
主题是 Prop Firm intelligence / market observation。
保持大量安静区域，只使用一个主要 intelligence specimen。
```

或者：

```text
Use $kimi-design-refer.

Medium: poster-social
Core family: gray-proofboard
Zine family: zine/micro-archive
Zine intensity: medium

为 PropFirm.TV 做一张规则变更专题海报。
使用一个钴蓝色证据碎片作为唯一高饱和色。
不要做成 SaaS Dashboard。
```

---

# Review an Existing Design

你也可以不让 Skill 生成，而是让它当 Art Director：

```text
Use $kimi-design-refer in review-only mode.

Review this page against the selected visual family.
Give me the three highest-impact fixes first.
```

建议 Review 时不要只评价“好不好看”，而是判断：

```text
这个结果到底属于哪个 Family？
主视觉事件是否明确？
留白是否真的承担结构作用？
有没有真实的 reasoning trace？
色彩是不是被当成标点，而不是气氛滤镜？
是不是又滑回了 generic AI / SaaS aesthetic？
```

---

# Design Boundaries

Kimi Design Refer **不是 Moonshot AI / Kimi 官方品牌规范**。

这是一个非官方、原创重组的审美参考系统。

请不要：

- 复制 Kimi / Moonshot 的官方 Logo；
- 复刻某一张官方 Campaign 的完整构图；
- 把生成结果描述成 Kimi 官方设计；
- 把所有 Family 混合成一种没有边界的“高级感”；
- 用品牌名称替代真正的视觉规则。

我们希望复用的是：

> **visual grammar，而不是 source identity。**

---

# Project Structure

```text
kimi-design-refer/
├── SKILL.md
├── README.md
├── THIRD_PARTY_NOTICES.md
│
└── references/
    ├── philosophy.md
    ├── style-families.md
    └── zine-editorial-extension.md
```

`SKILL.md` 是 Agent 执行入口。

`references/style-families.md` 描述 12 个视觉家族。

`references/zine-editorial-extension.md` 描述 Zine Family 与 Kimi × Zine 的融合规则。

---

# Inspirations & Credits

Kimi Design Refer 是一个原创、非官方的视觉参考系统。

它受到两个公开 MIT 项目的高层设计系统思路启发：

- [`Fannie0715/kimi-inspired-poster`](https://github.com/Fannie0715/kimi-inspired-poster)
- [`LiamGvchi/gc-minimal-zine-poster`](https://github.com/LiamGvchi/gc-minimal-zine-poster)

其中 Zine Editorial Extension 借鉴并重新组织了极端留白、单一小型视觉事件、稀疏编辑字体、单一高饱和色锚点，以及 print / scan reproduction 等高层视觉机制。

本仓库不包含、也不声称拥有任何 Kimi / Moonshot 官方 Campaign Asset、Logo、原始视觉素材或第三方示例图。

详见 [`THIRD_PARTY_NOTICES.md`](./THIRD_PARTY_NOTICES.md)。

---

# Philosophy

我们更关心的不是：

> “怎么写一条像 Kimi 的 Prompt？”

而是：

> **怎么把审美拆成可以被 Agent 稳定理解、调用、组合、检查和迭代的 Design System？**

Prompt 会变，模型会变，生成工具也会变。

但一套结构化的视觉语言可以继续被复用。

这就是 `kimi-design-refer` 想做的事情。
