---
name: enterprise-company-research-agent
description: Use when an enterprise user needs fresh, source-backed research on a supplier, vendor, company, product, competitor, partner, customer, or acquisition target for procurement, risk, strategy, sales, partnership, or due-diligence decisions.
license: MIT
metadata:
  compatibility: Works with Agent Skills / SKILL.md compatible coding agents. Requires web access for current company, product, legal, pricing, and risk research.
---

# Enterprise Company Research Agent

## 中文

### 核心定位

这是一个面向 toB 企业客户的公司、供应商与产品深度调研 Agent。它以实时证据检索、企业身份核验、纵向发展脉络、横向竞品/替代方案对比、风险合规判断和采购决策建议为核心能力，输出可用于采购、供应商准入、竞品研判、合作伙伴评估、客户研究和投融资初筛的证据型研究报告。

必须先联网核验。不要用记忆回答“最新情况”。当资料冲突时，以一手来源和可复核证据为准，并把冲突写进报告。

### 用户需要输入什么

最小输入：

- 研究对象名称：公司、供应商、产品、品牌、集团、子公司、人物或行业概念。
- 决策场景：采购、供应商准入、续约、竞品分析、客户研究、合作伙伴评估、投融资初筛或风险预警。

更好的输入：

- 官网、产品链接、所在国家/地区、目标市场、已知法人主体。
- 重点关注：价格、产品能力、客户案例、技术路线、数据安全、合规资质、诉讼处罚、交付能力、财务稳定性。
- 需要比较的竞品或替代供应商。
- 交付深度和格式：快速 memo、标准报告、完整尽调；Markdown、PDF、PPT、表格或双语版本。

如果用户没有提供完整信息，先基于公开资料补全范围，并在报告中标注假设与未核验项。

### 用户会得到什么

- 一份结论先行的企业调研报告。
- 对象身份与范围核验：法人主体、品牌、产品、母子公司和同名实体排除。
- 从成立/发布到今天的关键时间线、战略转向、融资、客户、产品和组织变化。
- 当前产品能力、商业化状态、客户证明、定价/合同线索和交付能力判断。
- 与直接竞品、替代供应商和上下游依赖的横向对比。
- 风险、合规、数据安全、诉讼处罚、经营稳定性和供应链依赖分析。
- 采购或合作建议：通过、谨慎通过、补充尽调、暂缓或淘汰。
- 证据账本：已访问来源、关键事实、冲突事实、不可达来源和下一步尽调问题。

### 何时使用

用于这些请求：

- 调研供应商、厂商、渠道商、合作伙伴、客户公司、竞品、收购标的。
- 研究某公司及其核心产品、产品线、子品牌、母公司关系。
- 给采购、法务、风控、销售、战略或投委会提供决策材料。
- 用户要求“最新、准确、可靠、尽调、供应商评估、公司研究、竞品分析、风险分析、横纵分析”。

不要用于简单名词解释、纯营销文案、只需要三句话摘要的问答。

### 使用流程

1. **锁定研究范围**
   - 识别对象：公司、供应商、产品、人物、集团/子公司、行业概念。
   - 识别企业场景：采购/供应商准入、竞品、客户研究、合作伙伴、投融资、舆情风险。
   - 如果对象可能是子产品或子公司，默认研究用户点名对象，并标注母公司/兄弟产品边界。

2. **建立证据账本**
   - 必须联网搜索并打开来源。
   - 优先级：监管/工商/SEC/交易所文件 > 公司官网/公告/定价/文档 > 创始人或高管原话 > 客户案例/招聘/专利/开源仓库 > 权威媒体原创 > 第三方数据库 > 聚合转载。
   - 每条关键结论标注：已核验、强推断、弱推断、未证实、冲突。

3. **纵向分析**
   - 还原从成立/发布到今天的时间线、关键战略转向、融资/组织/产品/客户节点。
   - 对供应商研究，额外追踪：法律主体、股权与控制、经营状态、资质认证、交付能力、诉讼/处罚/负面新闻。

4. **横向分析**
   - 识别直接竞品、替代方案、上游/下游依赖、同类供应商。
   - 做当前截面对比：产品能力、价格/合同、客户与案例、财务/规模、合规、交付风险、生态依赖。

5. **横纵交汇**
   - 说明历史决策如何塑造今天的竞争位置与供应商风险。
   - 给出 3 个情景：最可能、最危险、最乐观。
   - 输出可执行建议：通过、谨慎通过、补充尽调、暂缓、淘汰。

6. **交付**
   - 默认生成一个完整 Markdown 报告；若用户需要，可再生成 PDF/幻灯片/表格摘要。
   - 如果用户要求双语交付，必须在同文件写“中文版本 + English Version”，或创建 `*-zh.md` 与 `*-en.md` 成对文件。

### 需要按需读取的参考文件

- 需要理解产品能力模型、输入输出边界和企业级判断框架时，读取 `references/capability-model.md`。
- 需要完整企业研究模块、证据分级、输出模板时，读取 `references/enterprise-research-playbook.md`。

### 企业级硬规则

- **最新性**：涉及公司现状、价格、融资、法务、合规、产品能力、客户案例、管理层、招聘、资质时，必须联网核验。
- **事实与判断分离**：报告中的每个判断都要能追溯到事实；推断必须明确标注。
- **不要用父公司数据替代子产品数据**：如果只有集团数据，写清楚“集团层面”，不得冒充为产品/子公司数据。
- **不要把第三方数据库当一手事实**：企查查、天眼查、Crunchbase、PitchBook、Similarweb 等只能作为线索或二级来源，关键数字要找原始来源。
- **采购视角**：企业报告必须回答“能不能合作/采购/依赖它”，而不只是讲公司故事。
- **来源透明**：报告末尾列出已访问来源、失败来源、冲突来源。

## English

### Core Purpose

This skill provides an enterprise-grade company, supplier, and product research agent. Its core capabilities are live evidence retrieval, entity verification, lifecycle analysis, peer and substitute comparison, risk and compliance judgment, and procurement-ready recommendations. It produces evidence-backed reports for supplier qualification, vendor diligence, competitive analysis, partnership review, customer research, and investment screening.

Always verify current facts online. Do not answer “latest status” from memory. When sources conflict, prefer primary evidence and document the conflict.

### What the User Should Provide

Minimum input:

- Research subject: company, supplier, product, brand, group, subsidiary, person, or category concept.
- Decision context: procurement, supplier onboarding, renewal, competitive analysis, customer research, partnership review, investment screening, or risk alert.

Better input:

- Official website, product link, country/region, target market, known legal entity.
- Focus areas: pricing, product capability, customer proof, technology, data security, compliance certifications, litigation, penalties, delivery capacity, financial stability.
- Known competitors or substitute vendors to compare.
- Desired depth and format: quick memo, standard report, full diligence; Markdown, PDF, slides, spreadsheet, or bilingual output.

If the user does not provide full context, infer the missing scope from public evidence and label assumptions and unverified items in the report.

### What the User Gets

- A decision-first enterprise research report.
- Identity and scope verification: legal entity, brand, product, parent/subsidiary relationships, and exclusion of similarly named entities.
- A timeline from founding or launch to today, including strategy shifts, financing, customers, product changes, and organizational signals.
- Current product capability, commercialization status, customer proof, pricing/contract signals, and delivery-capacity assessment.
- Horizontal comparison against direct competitors, substitute vendors, and upstream/downstream dependencies.
- Risk, compliance, data security, litigation, penalty, operating-stability, and supply-chain analysis.
- Procurement or partnership recommendation: approve, approve with caution, request more diligence, pause, or reject.
- Evidence ledger: visited sources, key facts, conflicting claims, unreachable sources, and next diligence questions.

### Use Cases

Use this skill for:

- Researching suppliers, vendors, channel partners, customers, competitors, partners, or acquisition targets.
- Mapping a company, its core products, subsidiaries, parent company, and product lines.
- Preparing decision material for procurement, legal, risk, sales, strategy, or investment committees.
- Requests involving latest facts, due diligence, supplier evaluation, company research, competitive analysis, risk analysis, or horizontal-vertical analysis.

Do not use it for simple definitions, pure marketing copy, or tiny Q&A summaries.

### Operating Flow

1. **Scope the target**
   - Identify whether the subject is a company, supplier, product, person, group/subsidiary, or category concept.
   - Identify the enterprise decision context: procurement, supplier onboarding, competitor analysis, customer research, partnership, investment, or reputation risk.
   - If the subject is a sub-product or subsidiary, default to the named subject and clearly separate parent/sibling scope.

2. **Build an evidence ledger**
   - Browse and open sources.
   - Source priority: regulatory / registry / SEC / exchange filings > official company pages, announcements, pricing, docs > founder/executive statements > customer cases, hiring, patents, repos > original reputable media > third-party databases > aggregators.
   - Label key claims as verified, strong inference, weak inference, unverified, or conflicting.

3. **Run the vertical axis**
   - Reconstruct the lifecycle from founding or launch to today: strategy shifts, financing, organization, product, customers, and incidents.
   - For supplier research, also track legal entity, ownership/control, operating status, certifications, delivery capacity, litigation, penalties, and negative news.

4. **Run the horizontal axis**
   - Identify direct competitors, substitutes, upstream/downstream dependencies, and comparable vendors.
   - Compare current position: capabilities, pricing/contracts, customers/cases, financial scale, compliance, delivery risk, ecosystem dependencies.

5. **Cross the axes**
   - Explain how historical choices created the current competitive position and supplier risk profile.
   - Provide three scenarios: most likely, most dangerous, most optimistic.
   - Give a decision recommendation: approve, approve with caution, request more diligence, pause, or reject.

6. **Deliver**
   - Default to one complete Markdown report; generate PDF, slides, or spreadsheet summary only when requested.
   - If the user requests bilingual delivery, write “中文版本 + English Version” in one file or create paired `*-zh.md` and `*-en.md` files.

### Reference Files

- Read `references/capability-model.md` when you need the product capability model, input/output boundary, and enterprise judgment framework.
- Read `references/enterprise-research-playbook.md` when you need the full enterprise module set, evidence grading, and report template.

### Enterprise Rules

- **Freshness**: For current status, pricing, funding, legal, compliance, product capability, customer cases, executives, hiring, or certifications, browse and verify.
- **Separate facts from judgment**: Every judgment must trace back to facts. Mark inference explicitly.
- **Do not substitute parent data for product data**: Label parent/group-level data clearly.
- **Do not treat third-party databases as primary facts**: Use databases as leads unless original filings or announcements confirm the claim.
- **Procurement lens**: Enterprise reports must answer whether the company is safe to buy from, partner with, or depend on.
- **Source transparency**: End with visited sources, failed sources, and conflicts.
