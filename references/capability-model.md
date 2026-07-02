# 能力模型 / Capability Model

## 中文版本

### 1. 产品定位

Enterprise Company Research Agent 是一个面向企业决策的公开产品工具。它帮助用户基于最新公开证据研究公司、供应商、产品、品牌、竞品、客户、合作伙伴或投融资标的，并把分散资料转化为可决策的企业报告。

它不只是生成公司简介，而是回答企业真正关心的问题：对象是谁、现在是否还活跃、产品是否成熟、客户是否可信、能否交付、风险在哪里、是否值得采购、合作或继续尽调。

### 2. 原生能力

| 能力 | 说明 | 用户价值 |
|---|---|---|
| 实时证据检索 | 联网搜索并打开公开来源，优先使用一手证据 | 避免用过期记忆或二手摘要做判断 |
| 对象身份核验 | 区分法律主体、品牌、产品、母子公司、关联公司和同名实体 | 防止把集团、子公司、产品线或同名公司混为一谈 |
| 纵向发展分析 | 梳理从成立/发布到今天的时间线、阶段、战略转向和路径依赖 | 解释一家公司为什么走到今天，而不是只看静态简介 |
| 横向对比分析 | 对比直接竞品、替代方案、上下游依赖和同类供应商 | 支持 shortlist、竞品地图和替代供应商评估 |
| 产品与商业化判断 | 分析产品能力、部署方式、定价/合同线索、客户案例、成熟度 | 判断产品是否能被企业真实采购和落地 |
| 风险与合规判断 | 检查诉讼、处罚、制裁、出口管制、资质、隐私、数据安全和供应链依赖 | 支持采购、法务、风控和安全评审 |
| 证据账本 | 对关键事实标注来源、证据等级、冲突与不可达项 | 让企业内部评审可以复核和追溯 |
| 决策建议 | 输出通过、谨慎通过、补充尽调、暂缓或淘汰 | 把研究材料转化为可执行动作 |

### 3. 用户需要输入什么

最小输入：

| 字段 | 示例 |
|---|---|
| 研究对象 | “某供应商公司”“某 AI 产品”“某集团旗下子品牌” |
| 决策场景 | 采购准入、续约、竞品分析、客户研究、合作评估、投资初筛 |

推荐补充：

| 字段 | 示例 |
|---|---|
| 已知链接 | 官网、产品页、招聘页、新闻稿、工商或监管链接 |
| 地域范围 | 中国、美国、欧盟、东南亚、全球 |
| 关注问题 | 数据安全、交付能力、产品成熟度、价格、诉讼处罚、财务稳定性 |
| 对比对象 | 已知竞品、备选供应商、内部替代方案 |
| 输出要求 | 快速 memo、标准报告、完整尽调；Markdown、PDF、PPT、表格、双语 |

### 4. 用户会得到什么

标准交付包括：

1. **决策摘要**：一句话结论、推荐动作、最高风险、最强证据。
2. **身份与范围核验**：法律主体、品牌、产品、母子公司、同名实体排除。
3. **发展脉络**：成立/发布背景、关键节点、阶段变化、战略转向。
4. **当前状态**：经营状态、组织信号、融资/收入/客户线索、招聘与扩张迹象。
5. **产品与能力**：核心功能、技术路线、部署方式、价格/合同线索、成熟度。
6. **客户与市场证明**：客户案例、行业分布、采购人群、续费/替换/用户反馈线索。
7. **横向对比**：竞品、替代供应商、上下游依赖、能力/价格/交付/风险矩阵。
8. **风险与合规**：诉讼、处罚、舆情、制裁、出口管制、资质、隐私和安全认证。
9. **情景判断**：最可能、最危险、最乐观三种情景。
10. **证据账本**：已访问来源、关键事实表、冲突事实、不可达来源、下一步尽调问题。

### 5. 企业判断框架

报告默认站在企业采购、合作或风险评审视角，而不是媒体写作视角。判断一个对象时，优先回答这些问题：

- **它是谁**：法律主体、实际控制、品牌和产品边界是否清楚？
- **它是否仍在正常运转**：官网、招聘、客户、融资、产品更新、公告是否显示活跃？
- **它能否交付**：团队、实施、支持、SLA、客户案例是否可信？
- **它是否安全合规**：数据、隐私、资质、认证、诉讼、处罚、制裁和出口管制是否有风险？
- **它是否可替代**：是否存在锁定风险，是否有可行替代供应商？
- **它是否值得下一步投入**：应通过、谨慎通过、补充尽调、暂缓还是淘汰？

## English Version

### 1. Product Positioning

Enterprise Company Research Agent is a public product tool for enterprise decision-making. It helps users research companies, suppliers, products, brands, competitors, customers, partners, or investment targets using current public evidence, then turns scattered information into decision-ready enterprise reports.

It does not merely generate a company profile. It answers enterprise questions: who the subject is, whether it is active today, whether its product is mature, whether its customers are credible, whether it can deliver, where the risks are, and whether it is worth buying from, partnering with, or diligencing further.

### 2. Native Capabilities

| Capability | Description | User Value |
|---|---|---|
| Live evidence retrieval | Searches and opens public sources, prioritizing primary evidence | Avoids outdated memory and weak summaries |
| Identity verification | Separates legal entities, brands, products, parent/subsidiaries, affiliates, and similarly named entities | Prevents entity confusion |
| Lifecycle analysis | Reconstructs timeline, stages, strategy shifts, and path dependence from founding or launch to today | Explains why the company reached its current position |
| Peer and substitute comparison | Compares direct competitors, alternatives, dependencies, and comparable vendors | Supports shortlists, competitor maps, and replacement evaluation |
| Product and commercialization judgment | Reviews capabilities, deployment, pricing/contract signals, customer cases, and maturity | Shows whether the product can be bought and deployed by enterprises |
| Risk and compliance judgment | Checks litigation, penalties, sanctions, export controls, certifications, privacy, data security, and supply-chain dependencies | Supports procurement, legal, risk, and security reviews |
| Evidence ledger | Labels key facts with sources, evidence grade, conflicts, and unreachable items | Makes internal review traceable and auditable |
| Decision recommendation | Recommends approve, approve with caution, request more diligence, pause, or reject | Converts research into action |

### 3. What the User Should Provide

Minimum input:

| Field | Example |
|---|---|
| Research subject | “a supplier company”, “an AI product”, “a subsidiary brand” |
| Decision context | Procurement onboarding, renewal, competitor analysis, customer research, partnership review, investment screening |

Recommended additions:

| Field | Example |
|---|---|
| Known links | Official website, product page, hiring page, press release, registry or regulatory link |
| Geography | China, U.S., EU, Southeast Asia, global |
| Focus questions | Data security, delivery capacity, product maturity, pricing, litigation, penalties, financial stability |
| Comparison targets | Known competitors, backup vendors, internal alternatives |
| Output requirements | Quick memo, standard report, full diligence; Markdown, PDF, slides, spreadsheet, bilingual |

### 4. What the User Gets

Standard delivery includes:

1. **Decision summary**: one-line conclusion, recommended action, top risks, strongest evidence.
2. **Identity and scope verification**: legal entity, brand, product, parent/subsidiary relationships, and exclusion of similarly named entities.
3. **Lifecycle narrative**: founding/launch background, milestones, stage changes, strategy shifts.
4. **Current state**: operating status, organization signals, funding/revenue/customer signals, hiring and expansion signals.
5. **Product and capability**: core functions, technology, deployment, pricing/contract signals, maturity.
6. **Customer and market proof**: customer cases, industries, buyers, renewal/replacement/user-feedback signals.
7. **Horizontal comparison**: competitors, substitute vendors, upstream/downstream dependencies, capability/price/delivery/risk matrix.
8. **Risk and compliance**: litigation, penalties, reputation issues, sanctions, export controls, certifications, privacy, and security posture.
9. **Scenario judgment**: most likely, most dangerous, and most optimistic scenarios.
10. **Evidence ledger**: visited sources, key facts, conflicting claims, unreachable sources, next diligence questions.

### 5. Enterprise Judgment Framework

The report defaults to an enterprise procurement, partnership, or risk-review lens rather than a media-writing lens. When judging a subject, answer these questions first:

- **Who is it**: Are legal entity, control, brand, and product boundaries clear?
- **Is it still active**: Do website, hiring, customers, funding, product updates, and announcements show activity?
- **Can it deliver**: Are team, implementation, support, SLA, and customer cases credible?
- **Is it compliant and safe**: Are there risks in data, privacy, certifications, litigation, penalties, sanctions, or export controls?
- **Is it substitutable**: Is there lock-in risk, and are viable alternatives available?
- **Is it worth the next step**: Should the user approve, approve with caution, request more diligence, pause, or reject?
