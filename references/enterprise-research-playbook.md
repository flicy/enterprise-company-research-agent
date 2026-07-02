# 企业公司调研剧本 / Enterprise Company Research Playbook

## 中文版本

### 1. 研究输入卡

启动时先填这张卡；用户未给的信息可以推断，但要标注。

| 字段 | 说明 |
|---|---|
| 研究对象 | 公司/供应商/产品/集团/子公司/人物/概念 |
| 决策场景 | 采购、准入、续约、竞品、客户、合作、投资、风险预警 |
| 输出深度 | 快速 memo、标准报告、完整尽调 |
| 时间范围 | 默认从成立/发布到今天 |
| 地域范围 | 全球、中国、美国、欧盟、东南亚等 |
| 关注点 | 法务、价格、技术、产品、客户、财务、供应链、数据安全 |
| 交付格式 | Markdown、PDF、PPT、表格、双语 |

### 2. 证据分级

| 等级 | 名称 | 可用于什么结论 |
|---|---|---|
| A | 一手强证据 | 法律主体、财务、价格、产品能力、管理层、公告 |
| B | 一手弱证据 | 官网营销页、创始人访谈、客户案例、产品文档 |
| C | 二手可信证据 | 权威媒体原创、行业报告、第三方数据库 |
| D | 弱证据 | 聚合页、转载、论坛传闻、未登录社交摘要 |
| X | 冲突/不可达 | 只能写入风险和待核验，不得作为确定结论 |

关键结论必须至少有 A/B 级证据；如果只有 C/D，写成推断。

### 3. 企业研究模块

根据场景裁剪，但标准报告至少覆盖这些模块：

1. **Executive decision memo**
   - 一句话结论
   - 推荐动作：通过、谨慎通过、补充尽调、暂缓、淘汰
   - 最高风险 3-5 条
   - 最值得信任的证据 3-5 条

2. **Scope and identity**
   - 法律主体、品牌、产品、母子公司、关联公司
   - 同名实体排除
   - 研究边界

3. **Vertical lifecycle**
   - 成立/发布背景
   - 创始团队/管理层
   - 融资、并购、客户、产品、战略转向
   - 关键阶段与路径依赖

4. **Current company state**
   - 经营状态、注册资本、实缴/股权、员工规模
   - 收入/融资/客户规模（只写可证实或明确推断）
   - 招聘、办公室、组织扩张信号

5. **Product and capability**
   - 核心产品/产品线
   - 当前功能、技术路线、部署方式、价格/合同
   - 产品成熟度：概念、Beta、商用、规模化、衰退

6. **Customer and market proof**
   - 客户案例、行业、采购人群
   - 留存/续费/替换证据
   - 真实用户反馈

7. **Horizontal comparison**
   - 直接竞品
   - 替代供应商
   - 上游/下游依赖
   - 对比维度：能力、价格、交付、资质、生态、风险

8. **Risk and compliance**
   - 法律诉讼、行政处罚、舆情、制裁、出口管制
   - 数据安全、隐私、安全认证、行业资质
   - 供应链、单点依赖、财务稳定性

9. **Cross-axis insight**
   - 历史如何塑造当前能力和风险
   - 竞争格局对未来的影响
   - 最可能/最危险/最乐观情景

10. **Evidence ledger**
    - 已访问来源
    - 关键事实表
    - 冲突事实
    - 失败/不可达来源

### 4. 标准报告模板

```markdown
# [对象] 企业调研报告

研究日期：YYYY-MM-DD
研究场景：[采购/供应商准入/竞品/合作/投资]
结论等级：[通过/谨慎通过/补充尽调/暂缓/淘汰]

## 中文版本

### 1. 决策摘要

> [!info] 一句话结论
> ...

| 项目 | 结论 | 证据等级 |
|---|---|---|
| 推荐动作 | ... | ... |
| 最大风险 | ... | ... |
| 最强证据 | ... | ... |

### 2. 身份与范围

### 3. 纵向：从成立到今天

### 4. 当前状态

### 5. 产品与能力

### 6. 客户与市场证明

### 7. 横向：同类/竞品/替代供应商

### 8. 风险、合规与采购判断

### 9. 横纵交汇洞察

### 10. 证据账本

## English Version

[Mirror the same structure in English.]
```

### 5. 供应商准入评分

| 维度 | 权重建议 | 评分问题 |
|---|---:|---|
| 身份清晰度 | 15% | 法律主体、母子关系、品牌是否清楚 |
| 产品成熟度 | 20% | 是否已商用、是否有稳定客户 |
| 交付能力 | 15% | 团队、实施、支持、SLA 是否可信 |
| 财务/经营稳定性 | 15% | 融资、收入、现金流、招聘、裁员信号 |
| 合规/安全 | 15% | 数据、隐私、认证、处罚、诉讼 |
| 生态与替代性 | 10% | 是否锁定、是否有可替代供应商 |
| 战略匹配 | 10% | 是否符合采购方长期路线 |

评分建议：

- 80-100：通过
- 65-79：谨慎通过，附条件
- 50-64：补充尽调
- 35-49：暂缓
- 0-34：淘汰

### 6. 质检门槛

交付前逐项检查：

- 是否打开并引用了当前日期附近的一手来源？
- 公司法律主体和产品/品牌是否分清？
- 是否把父公司数据误写成子产品数据？
- 是否有证据账本和冲突事实表？
- 是否明确区分事实、推断、观点？
- 是否回答了企业决策问题，而不是只写故事？
- 是否列出未核验项和下一步尽调问题？
- 如果用户要求双语交付，Markdown 是否包含完整中文和英文版本？

## English Version

### 1. Research Intake Card

Fill this card first. Infer missing fields when reasonable, but label the inference.

| Field | Description |
|---|---|
| Subject | Company, supplier, product, group, subsidiary, person, or concept |
| Decision context | Procurement, onboarding, renewal, competitor, customer, partnership, investment, risk alert |
| Depth | Quick memo, standard report, full diligence |
| Time range | Default from founding or launch to today |
| Geography | Global, China, U.S., EU, Southeast Asia, etc. |
| Focus | Legal, price, technology, product, customers, finance, supply chain, data security |
| Format | Markdown, PDF, slides, spreadsheet, bilingual |

### 2. Evidence Grades

| Grade | Name | Can support |
|---|---|---|
| A | Strong primary evidence | Legal entity, financials, pricing, product capability, executives, official announcements |
| B | Weaker primary evidence | Marketing pages, founder interviews, customer cases, docs |
| C | Credible secondary evidence | Original reputable media, analyst reports, third-party databases |
| D | Weak evidence | Aggregators, reposts, forum rumors, unauthenticated social snippets |
| X | Conflicting or unreachable | Risk notes and follow-up only |

Key conclusions need A/B evidence. If only C/D evidence exists, state the claim as an inference.

### 3. Enterprise Research Modules

Use these modules as the standard set and trim by context:

1. **Executive decision memo**: conclusion, recommendation, top risks, strongest evidence.
2. **Scope and identity**: legal entity, brand, product, parent/subsidiaries, exclusions.
3. **Vertical lifecycle**: origin, founders, financing, customers, products, strategy shifts, path dependence.
4. **Current company state**: operating status, capital, ownership, employees, revenue/funding/customer signals.
5. **Product and capability**: product lines, functionality, technology, deployment, pricing, maturity.
6. **Customer and market proof**: cases, industries, buyers, retention/replacement evidence, user feedback.
7. **Horizontal comparison**: direct competitors, substitute suppliers, dependencies, comparison matrix.
8. **Risk and compliance**: litigation, penalties, sanctions, export controls, data security, certifications, supply chain, stability.
9. **Cross-axis insight**: how history shaped capability and risk; scenarios.
10. **Evidence ledger**: visited sources, key facts, conflicts, unreachable sources.

### 4. Standard Report Template

Use the Chinese template above and mirror the same structure in English when bilingual Markdown is required.

### 5. Supplier Qualification Scoring

| Dimension | Suggested weight | Question |
|---|---:|---|
| Identity clarity | 15% | Are legal entity, parent/subsidiary, and brand relationships clear? |
| Product maturity | 20% | Is it commercial and used by stable customers? |
| Delivery capability | 15% | Are implementation, support, and SLA credible? |
| Financial/operating stability | 15% | What do funding, revenue, hiring, layoffs, and cash signals show? |
| Compliance/security | 15% | What do privacy, security, certifications, penalties, and litigation show? |
| Ecosystem and substitutability | 10% | Is there lock-in? Are alternatives available? |
| Strategic fit | 10% | Does the vendor match the buyer's long-term direction? |

Recommendation bands:

- 80-100: approve
- 65-79: approve with caution
- 50-64: request more diligence
- 35-49: pause
- 0-34: reject

### 6. Quality Gates

Before delivery, verify:

- Did you open and cite recent primary sources?
- Are legal entity, product, and brand separated?
- Did you avoid substituting parent data for product data?
- Is there an evidence ledger and conflict table?
- Are facts, inferences, and opinions separated?
- Does the report answer the enterprise decision question?
- Are unverified items and next diligence questions listed?
- If bilingual delivery was requested, does Markdown include complete Chinese and English versions?
