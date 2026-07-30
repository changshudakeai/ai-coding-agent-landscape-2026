# AI Coding Agent Landscape 2026

## 从代码辅助到 Agent 系统：AI Coding 产品演进如何重塑组织能力与人才需求

本仓库是一项基于产品官方资料与公开招聘岗位的探索性研究，观察截止于 **2026 年 7 月 30 日**。

研究关注的不是模型跑分或产品排名，而是：

> **AI Coding Agent 的产品能力演进，正在如何改变企业的组织能力瓶颈、岗位组合和人才需求？**

## 推荐阅读

1. **快速了解结论：** [`report/executive-summary-v0.1.md`](report/executive-summary-v0.1.md)
2. **阅读完整报告：** [`report/full-report-draft-v0.2.md`](report/full-report-draft-v0.2.md)
3. **复核主张与证据：** [`data/claim-evidence-index-v0.1.csv`](data/claim-evidence-index-v0.1.csv)
4. **查看研究设计：** [`methodology/research-design-v1.md`](methodology/research-design-v1.md)
5. **查看岗位编码：** [`data/jd-open-coding-v0.1.md`](data/jd-open-coding-v0.1.md) 与 [`data/jd-six-dimension-coding-v0.2.csv`](data/jd-six-dimension-coding-v0.2.csv)

## 核心结论

### 1. 产品从代码辅助扩展到 Agent 交付系统

六个核心产品——OpenAI Codex、Anthropic Claude Code、Cursor、Qoder、GitHub Copilot 和 Cognition Devin——均在不同程度上扩展任务委托、执行环境、验证、并行或治理能力。

分析 Agent 能力时，需要同时考虑：

> **模型＋上下文＋工具＋执行环境＋权限＋Harness**

### 2. 能力瓶颈迁移，而不是统一消失

对于目标清晰、上下文充足且结果可验证的任务，规格、环境、权限、验证和审查更可能成为主要约束；对于创新性、高风险和低可验证任务，专业技术判断仍可能是核心瓶颈。

### 3. 企业主要通过既有职能的责任扩展作出响应

岗位样本中的相关责任分布在 Agent 系统、评测、安全、产品、部署、采用、运营和 People 职能中。当前证据更支持既有职能增加新的工作对象和责任，而不是一个已经成熟、独立的 Agent 职业体系。

### 4. 人才 Mapping 应进一步深入到能力瓶颈和证据

本研究提出：

> **能力瓶颈 → 岗位能力原型 → 必需能力组合 → 专业与责任情境 → 直接人才来源 → 相邻人才来源 → 候选人证据 → 风险与待验证项**

岗位名称、专业、年限和公司背景可以用于检索与初筛，但最终判断仍需检查实际任务、专业领域、责任范围、工作产物和结果证据。

## 研究样本

### 产品

- OpenAI Codex
- Anthropic Claude Code
- Cursor
- Qoder
- GitHub Copilot
- Cognition Devin

### 公开岗位

- 20 份定向岗位样本；
- 17 份完整官方 JD；
- 3 份正文不完整但可确认的官方材料；
- Qoder 仅保留官方岗位目录信号，未进入精细编码。

岗位样本不具统计代表性，不能用于推断行业岗位比例、需求规模或增长率。

## 仓库结构

```text
.
├── README.md
├── PROJECT_STATE.md
├── methodology/
│   ├── research-design-v1.md
│   ├── six-dimension-framework-v0.2.md
│   └── talent-mapping-method-v0.1.md
├── report/
│   ├── executive-summary-v0.1.md
│   ├── full-report-draft-v0.2.md
│   ├── product-capability-evolution-matrix-v0.1.md
│   ├── capability-bottleneck-matrix-v0.1.md
│   ├── six-dimension-framework-review-v0.2.md
│   └── ai-organizational-capability-intelligence-role-v0.1.md
├── data/
│   ├── claim-evidence-index-v0.1.csv
│   ├── jd-open-coding-v0.1.md
│   ├── jd-sample-register-v0.1.csv
│   ├── jd-six-dimension-coding-v0.2.csv
│   ├── talent-source-archetype-matrix-v0.1.csv
│   └── target-role-capability-profile-v0.1.csv
├── templates/
│   └── candidate-evidence-card-v0.1.md
└── review/
    ├── full-report-evidence-audit-v0.1.md
    └── publication-consistency-audit-v0.1.md
```

## 证据与版本规则

研究区分：

- **事实**：来源直接记录的可核验信息；
- **公司主张**：厂商对产品、风险或市场的公开陈述；
- **样本归纳**：从本研究样本中归纳出的结构；
- **研究推断**：基于多项证据形成的解释；
- **方法建议**：本研究提出的分析或实践原则。

底层证据等级：

| 等级 | 含义 |
|---|---|
| A | 完整官方证据 |
| B | 不完整但可确认的官方证据 |
| C | 需要交叉核验的外部补充证据 |
| D | 研究者推断或研究过程记录 |
| E | 个人一手案例 |

正文中的 `[Cxx]` 对应 [`data/claim-evidence-index-v0.1.csv`](data/claim-evidence-index-v0.1.csv)。

## 重要限制

- 中国官方岗位样本明显不足；
- 尚未进行独立编码者一致性检验；
- 公开 JD 反映岗位意图，不等于真实组织结构、日常工作或招聘结果；
- 产品官方资料不能独立证明真实可靠性、采用深度、事故率或 ROI；
- 六类岗位能力原型是探索性分析工具，不是行业标准；
- 禁止使用六维框架计算候选人统一总分；
- 不同 T-Domain 不得视为直接可替代；
- 个人案例只用于解释机制；
- 目标岗位官方链接尚未恢复，只作为方法应用案例。

## 作者与 AI 工具分工

仓库所有者负责研究问题、范围选择、阶段审核和最终判断。AI 工具用于公开资料整理、结构化编码、初稿生成、一致性检查和仓库操作。

所有进入主分支的核心内容均经过作者确认。研究中的推断、方法建议和个人案例均按证据边界单独标记。

## Disclaimer

本项目为独立探索性研究，不代表任何产品公司、招聘平台或雇主。产品功能、岗位状态和组织实践可能在观察截止日后发生变化，引用时应结合访问日期和原始来源复核。
