# Enterprise Company Research Agent

简体中文 | English below

> 给企业客户做供应商、公司与产品调研的 Agent Skill：先核验对象是谁和现在怎么样，再输出能支持采购、合作、竞品、客户研究和投融资初筛的证据型报告。

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Agent Skill](https://img.shields.io/badge/agent--skill-SKILL.md-blue.svg)](./SKILL.md)
[![GitHub repo](https://img.shields.io/badge/github-flicy%2Fenterprise--company--research--agent-black.svg)](https://github.com/flicy/enterprise-company-research-agent)

Enterprise Company Research Agent 是一个轻量但结构化的 **企业调研 skill**。用户只需要先说清楚想研究谁、为了什么决策，它会帮助 Agent 把公开资料整理成：

- 身份与范围核验
- 从成立/发布到今天的发展脉络
- 产品能力和商业化状态
- 竞品、替代供应商和上下游依赖对比
- 风险、合规、数据安全和交付能力判断
- 可复核的证据账本
- 采购或合作建议

它的重点不是写一篇公司介绍，而是把“能不能采购、能不能合作、能不能依赖、还缺什么尽调”变成可检查的结论。

## 适合什么场景

如果你希望：

- 评估一个新供应商能不能进入采购名单
- 判断一个产品是否真实商用、是否有可信客户
- 对比多个竞品、替代供应商或合作伙伴
- 快速弄清楚某家公司、子品牌、产品线和母公司的关系
- 为采购、法务、风控、安全、销售、战略或投委会准备材料
- 获取最新、准确、带来源的企业和产品研究

那么这个 Skill 就很适合你。

如果你只是需要三句话百科解释、纯营销文案或不需要来源的灵感整理，它通常不是最佳入口。

## 一句话需求进来，它怎么接住

用户不需要先填完整表格，也不需要知道公司法律主体。直接用业务语言说：

```text
帮我调研这家公司能不能作为供应商。
研究 Foodpal 现在是什么情况、产品是什么、团队背景如何。
比较 A、B、C 三家公司，看看哪家更适合进入 shortlist。
```

Agent 会先补齐研究边界，再按企业决策场景选择合适的深度。

| 输入清晰度 | Agent 怎么处理 | 输出重点 |
|---|---|---|
| 只有公司或产品名 | 先确认官网、法律主体、品牌/产品边界和同名实体 | 身份核验、当前状态、未核验项 |
| 已有官网和决策场景 | 直接进入证据检索、产品能力、客户证明和风险分析 | 标准企业调研报告 |
| 已给竞品或备选供应商 | 增加横向对比、替代性和采购建议 | shortlist / vendor comparison |
| 已给风控或合规关注点 | 优先检查诉讼、处罚、认证、数据安全、制裁和出口管制 | 风险 memo 和补充尽调问题 |

## 用户需要输入什么

最小输入：

| 字段 | 示例 |
|---|---|
| 研究对象 | 公司、供应商、产品、品牌、集团、子公司、人物或行业概念 |
| 决策场景 | 采购准入、续约、竞品分析、客户研究、合作评估、投融资初筛或风险预警 |

更好的输入：

| 字段 | 示例 |
|---|---|
| 已知链接 | 官网、产品页、招聘页、新闻稿、工商或监管链接 |
| 地域范围 | 中国、美国、欧盟、东南亚、全球 |
| 关注问题 | 数据安全、交付能力、产品成熟度、价格、诉讼处罚、财务稳定性 |
| 对比对象 | 已知竞品、备选供应商、内部替代方案 |
| 输出要求 | 快速 memo、标准报告、完整尽调；Markdown、PDF、PPT、表格、双语 |

信息不完整也可以启动。Agent 会把合理推断和未核验项标出来，不会把猜测写成事实。

## 用户会得到什么

标准报告通常包含：

1. **决策摘要**：一句话结论、推荐动作、最高风险、最强证据。
2. **身份与范围核验**：法律主体、品牌、产品、母子公司、同名实体排除。
3. **发展脉络**：成立/发布背景、关键节点、战略转向、融资、客户和组织变化。
4. **当前状态**：经营状态、组织信号、融资/收入/客户线索、招聘与扩张迹象。
5. **产品与能力**：核心功能、技术路线、部署方式、价格/合同线索、成熟度。
6. **客户与市场证明**：客户案例、行业分布、采购人群、续费/替换/用户反馈线索。
7. **横向对比**：竞品、替代供应商、上下游依赖、能力/价格/交付/风险矩阵。
8. **风险与合规**：诉讼、处罚、舆情、制裁、出口管制、资质、隐私和安全认证。
9. **情景判断**：最可能、最危险、最乐观三种情景。
10. **证据账本**：已访问来源、关键事实表、冲突事实、不可达来源、下一步尽调问题。

## 和普通搜索 / 公司简介有什么不一样

| 方式 | 重心 | 用户主要得到什么 | 适合什么 |
|---|---|---|---|
| 普通搜索 | 找资料 | 链接、摘要、零散信息 | 快速了解一个名字 |
| 公司简介生成 | 写介绍 | 公司故事、产品描述 | 市场、销售或内部背景材料 |
| **Enterprise Company Research Agent** | 企业决策 | 证据账本、风险判断、横向对比、采购/合作建议 | 供应商准入、竞品研判、合作评估、投融资初筛 |

这个 Skill 最有价值的地方，是把“资料看起来很多”变成“哪些事实可信、哪些结论可用、哪些地方不能下判断”。

## 典型真实场景

| 场景 | 为什么适合这个 Skill | 主要产物 |
|---|---|---|
| 新供应商准入 | 企业需要知道法律主体、交付能力、客户证明和风险 | 供应商准入报告、风险清单、补充尽调问题 |
| 竞品或替代方案 shortlist | 不只是看功能，还要看成熟度、客户、价格和替代风险 | 横向对比表、采购建议、替代性判断 |
| 客户或合作伙伴研究 | 销售/BD 需要理解公司现状、产品和组织信号 | 客户画像、业务线索、合作切入点 |
| 投融资初筛 | 需要快速判断公司是否真实活跃、产品是否成熟 | 初筛 memo、证据等级、风险提示 |
| 品牌/子公司关系混乱 | 同名公司、产品线、海外主体容易混淆 | 身份核验、范围说明、冲突来源 |
| 负面舆情或合规预警 | 单一数据库容易误导，需要多源核验 | 风险 memo、冲突事实表、下一步核查 |

## 默认带上的能力

- **实时核验**：涉及公司现状、融资、法务、产品能力、客户案例、价格、招聘和资质时，默认联网核验。
- **证据优先级**：监管/工商/SEC/交易所文件优先，其次是官网、公告、文档、高管原话、客户案例、招聘、专利、开源仓库、权威媒体和第三方数据库。
- **事实与判断分离**：每个关键判断都要能追溯到事实；推断必须明确标注。
- **对象边界控制**：不把父公司数据误写成子产品数据，不把同名实体混为一谈。
- **采购视角**：报告必须回答“能不能采购、合作或依赖它”，不只讲公司故事。
- **冲突处理**：资料冲突时，把冲突写进证据账本，而不是静默选择一个说法。

## 仓库结构

```text
enterprise-company-research-agent/
├── SKILL.md
├── README.md
├── LICENSE
├── skill.yml
├── agents/
│   └── openai.yaml
└── references/
    └── enterprise-research-playbook.md
```

`SKILL.md` 是薄入口：触发条件、流程、深度控制和硬规则。`references/enterprise-research-playbook.md` 是深度参考：证据分级、检索入口与查询手法、研究模块、低证据协议、报告模板和质检门槛，agent 按需读取。

## 安装

### Codex

```bash
git clone https://github.com/flicy/enterprise-company-research-agent.git
cp -R enterprise-company-research-agent ~/.codex/skills/enterprise-company-research-agent
```

### Claude Code

```bash
git clone https://github.com/flicy/enterprise-company-research-agent.git
mkdir -p ~/.claude/skills
cp -R enterprise-company-research-agent ~/.claude/skills/enterprise-company-research-agent
```

### QClaw / OpenClaw

```bash
git clone https://github.com/flicy/enterprise-company-research-agent.git
# 按你的 QClaw / OpenClaw skills 搜索路径复制本目录，入口保持 SKILL.md。
```

### CodeBuddy / WorkBuddy 相关 coding agent

```bash
git clone https://github.com/flicy/enterprise-company-research-agent.git
mkdir -p .codebuddy/skills
cp -R enterprise-company-research-agent .codebuddy/skills/enterprise-company-research-agent
```

`skill.yml` 是 WorkBuddy 风格的元数据桥接文件；核心入口仍然是 `SKILL.md`。

## 快速开始

在支持 Agent Skills 的客户端里，新开会话后直接说：

```text
使用 enterprise-company-research-agent，调研 [公司/产品名]，场景是 [采购/竞品/合作/投资/风险]。
```

更完整的提示词：

```text
使用 enterprise-company-research-agent 调研 [公司名]。
决策场景：供应商准入。
关注点：法律主体、产品成熟度、客户案例、数据安全、诉讼处罚、交付能力。
对比对象：[竞品 A]、[竞品 B]。
输出：中文标准报告，附证据账本和下一步尽调问题。
```

## 质量与安全

- 这个 Skill 需要联网能力才能回答“最新情况”。没有网络时，必须明确标注当前事实无法核验。
- 不要把第三方数据库当成一手事实；关键数字和结论尽量回到原始来源。
- 不要提交客户资料、内部评审材料、访问 token、私有路径或账号信息到公开仓库。
- README 保持中英双语；`SKILL.md` 和 `references/` 是 agent 指令层，保持中文单语以控制加载成本。报告输出语言跟随用户，双语报告由报告层实现。

## 相关 Skill

| Skill | 用途 |
|---|---|
| [wechat-publish-from-transcript](https://github.com/flicy/wechat-publish-from-transcript) | 把访谈/直播逐字稿变成公众号文章和跨平台内容包 |
| [prepare-livestream-event](https://github.com/flicy/prepare-livestream-event) | 筹备线上直播活动，生成海报、文案和发布清单 |
| [publish-skill-to-github](https://github.com/flicy/publish-skill-to-github) | 把本地 Skill 包发布到 GitHub |

## 许可证

MIT — 见 [LICENSE](./LICENSE)

---

## English Version

> An Agent Skill for enterprise supplier, company, and product research: verify who the subject is and what its current state is, then produce evidence-backed reports for procurement, partnership, competitive analysis, customer research, and investment screening.

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Agent Skill](https://img.shields.io/badge/agent--skill-SKILL.md-blue.svg)](./SKILL.md)
[![GitHub repo](https://img.shields.io/badge/github-flicy%2Fenterprise--company--research--agent-black.svg)](https://github.com/flicy/enterprise-company-research-agent)

Enterprise Company Research Agent is a lightweight but structured **enterprise research skill**. The user only needs to say who they want to research and what decision they need to make. The Skill helps an agent turn public evidence into:

- identity and scope verification
- lifecycle timeline from founding or launch to today
- product capability and commercialization status
- competitor, substitute vendor, and dependency comparison
- risk, compliance, data security, and delivery-capacity judgment
- traceable evidence ledger
- procurement or partnership recommendation

Its job is not to write a company profile. Its job is to make “can we buy from it, partner with it, depend on it, or diligence it further?” inspectable.

## When To Use

Use this Skill when you want to:

- evaluate whether a new supplier should enter a procurement shortlist
- check whether a product is commercially real and has credible customers
- compare competitors, substitute vendors, or potential partners
- clarify relationships between a company, subsidiary, brand, product line, and parent company
- prepare material for procurement, legal, risk, security, sales, strategy, or investment teams
- get current, accurate, source-backed company and product research

It is usually not the best entry point for three-sentence definitions, pure marketing copy, or source-free brainstorming.

## How It Handles A One-Line Request

The user does not need to fill out a full form or know the legal entity first. They can start with business language:

```text
Research whether this company is safe to onboard as a supplier.
Research Foodpal's current state, product, and team background.
Compare company A, B, and C and decide which one should enter the shortlist.
```

The agent first completes the research boundary, then chooses the right depth for the enterprise decision context.

| Input clarity | How the agent handles it | Output focus |
|---|---|---|
| Only company or product name | Verifies website, legal entity, brand/product boundary, and similarly named entities | Identity, current state, unverified items |
| Website and decision context provided | Runs evidence retrieval, product review, customer proof, and risk analysis | Standard enterprise research report |
| Competitors or alternative vendors provided | Adds horizontal comparison, substitutability, and procurement recommendation | Shortlist / vendor comparison |
| Risk or compliance concerns provided | Prioritizes litigation, penalties, certifications, data security, sanctions, and export controls | Risk memo and follow-up diligence questions |

## What The User Should Provide

Minimum input:

| Field | Example |
|---|---|
| Research subject | Company, supplier, product, brand, group, subsidiary, person, or category concept |
| Decision context | Procurement onboarding, renewal, competitive analysis, customer research, partnership review, investment screening, or risk alert |

Recommended additions:

| Field | Example |
|---|---|
| Known links | Official website, product page, hiring page, press release, registry or regulatory link |
| Geography | China, U.S., EU, Southeast Asia, global |
| Focus questions | Data security, delivery capacity, product maturity, pricing, litigation, penalties, financial stability |
| Comparison targets | Known competitors, backup vendors, internal alternatives |
| Output requirements | Quick memo, standard report, full diligence; Markdown, PDF, slides, spreadsheet, bilingual |

Incomplete input is fine. The agent labels reasonable assumptions and unverified items instead of turning guesses into facts.

## What The User Gets

A standard report usually includes:

1. **Decision summary**: one-line conclusion, recommended action, top risks, strongest evidence.
2. **Identity and scope verification**: legal entity, brand, product, parent/subsidiary relationships, and exclusion of similarly named entities.
3. **Lifecycle narrative**: founding/launch background, milestones, strategy shifts, financing, customers, and organizational changes.
4. **Current state**: operating status, organization signals, funding/revenue/customer signals, hiring and expansion signals.
5. **Product and capability**: core functions, technology, deployment, pricing/contract signals, maturity.
6. **Customer and market proof**: customer cases, industries, buyers, renewal/replacement/user-feedback signals.
7. **Horizontal comparison**: competitors, substitute vendors, upstream/downstream dependencies, capability/price/delivery/risk matrix.
8. **Risk and compliance**: litigation, penalties, reputation issues, sanctions, export controls, certifications, privacy, and security posture.
9. **Scenario judgment**: most likely, most dangerous, and most optimistic scenarios.
10. **Evidence ledger**: visited sources, key facts, conflicting claims, unreachable sources, next diligence questions.

## How It Differs From Search Or A Company Profile

| Method | Focus | Main output | Best for |
|---|---|---|---|
| Web search | Finding information | Links, snippets, fragmented facts | Quickly learning a name |
| Company profile generation | Writing a description | Company story and product description | Marketing, sales, or background material |
| **Enterprise Company Research Agent** | Enterprise decision-making | Evidence ledger, risk judgment, peer comparison, procurement/partnership recommendation | Supplier onboarding, competitive analysis, partnership review, investment screening |

The Skill is most useful when “there is a lot of information” needs to become “which facts are reliable, which conclusions are usable, and where we cannot judge yet.”

## Common Scenarios

| Scenario | Why this Skill fits | Main artifacts |
|---|---|---|
| New supplier onboarding | Enterprises need legal entity, delivery capacity, customer proof, and risk checks | Supplier report, risk list, follow-up diligence questions |
| Competitor or substitute shortlist | The decision depends on maturity, customers, pricing, and replacement risk, not only features | Comparison table, procurement recommendation, substitutability judgment |
| Customer or partner research | Sales and BD teams need company state, product context, and organization signals | Customer profile, business signals, partnership entry points |
| Investment screening | Teams need to know whether the company is active and whether the product is mature | Screening memo, evidence grades, risk notes |
| Confusing brand/subsidiary structure | Similar names, product lines, and overseas entities are easy to mix up | Identity verification, scope notes, conflicting sources |
| Negative news or compliance alert | Single databases can mislead; multiple sources need reconciliation | Risk memo, conflict table, next checks |

## Default Capabilities

- **Current verification**: For company status, funding, legal, product capability, customer cases, pricing, hiring, and certifications, browse and verify.
- **Evidence priority**: Prefer regulatory, registry, SEC, and exchange filings; then official pages, announcements, docs, executive statements, customer cases, hiring, patents, repos, reputable media, and third-party databases.
- **Fact/judgment separation**: Every key judgment must trace back to facts. Inference must be labeled.
- **Scope control**: Do not substitute parent-company data for product data or confuse similarly named entities.
- **Procurement lens**: The report must answer whether the subject is safe to buy from, partner with, or depend on.
- **Conflict handling**: When sources conflict, document the conflict in the evidence ledger instead of silently choosing one version.

## Repository Structure

```text
enterprise-company-research-agent/
├── SKILL.md
├── README.md
├── LICENSE
├── skill.yml
├── agents/
│   └── openai.yaml
└── references/
    └── enterprise-research-playbook.md
```

`SKILL.md` is a thin entry point: triggers, flow, depth control, and hard rules. `references/enterprise-research-playbook.md` is the deep reference: evidence grades, search entry points and query craft, research modules, low-evidence protocol, report template, and quality gates, loaded on demand.

## Installation

### Codex

```bash
git clone https://github.com/flicy/enterprise-company-research-agent.git
cp -R enterprise-company-research-agent ~/.codex/skills/enterprise-company-research-agent
```

### Claude Code

```bash
git clone https://github.com/flicy/enterprise-company-research-agent.git
mkdir -p ~/.claude/skills
cp -R enterprise-company-research-agent ~/.claude/skills/enterprise-company-research-agent
```

### QClaw / OpenClaw

```bash
git clone https://github.com/flicy/enterprise-company-research-agent.git
# Copy this directory into your QClaw / OpenClaw skills search path. Keep SKILL.md as the entry point.
```

### CodeBuddy / WorkBuddy-related coding agents

```bash
git clone https://github.com/flicy/enterprise-company-research-agent.git
mkdir -p .codebuddy/skills
cp -R enterprise-company-research-agent .codebuddy/skills/enterprise-company-research-agent
```

`skill.yml` is a WorkBuddy-style metadata bridge. The core entry point remains `SKILL.md`.

## Quick Start

In an Agent Skills compatible client, open a new session and say:

```text
Use enterprise-company-research-agent to research [company/product name] for [procurement/competition/partnership/investment/risk].
```

A fuller prompt:

```text
Use enterprise-company-research-agent to research [company name].
Decision context: supplier onboarding.
Focus: legal entity, product maturity, customer cases, data security, litigation, penalties, delivery capacity.
Compare against: [competitor A], [competitor B].
Output: standard English report with evidence ledger and follow-up diligence questions.
```

## Quality And Safety

- This Skill needs web access for “latest status” research. Without network access, current facts must be labeled unverified.
- Do not treat third-party databases as primary facts. Critical numbers and conclusions should be traced to original sources when possible.
- Do not commit customer data, internal review material, access tokens, private paths, or account information to a public repository.
- The README stays bilingual. `SKILL.md` and `references/` are the agent instruction layer and stay Chinese-only to control context cost; report output language follows the user, and bilingual reports are produced at the report layer.

## Related Skills

| Skill | Purpose |
|---|---|
| [wechat-publish-from-transcript](https://github.com/flicy/wechat-publish-from-transcript) | Turn interview/livestream transcripts into WeChat articles and cross-platform content packs |
| [prepare-livestream-event](https://github.com/flicy/prepare-livestream-event) | Prepare livestream event launches with posters, copy, and publishing checklists |
| [publish-skill-to-github](https://github.com/flicy/publish-skill-to-github) | Publish local Skill packages to GitHub |

## License

MIT — see [LICENSE](./LICENSE)
