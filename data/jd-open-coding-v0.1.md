# 20 份代表性 JD 开放编码 v0.1

> 观察截止：2026-07-30  
> 状态：作者已确认的阶段性交付物  
> 方法：第一遍开放编码，不立即套用六维能力框架。  
> 本文件记录岗位实际解决的问题、交付结果、服务对象、协作关系、技术深度和证据边界。

## 1. 样本与证据质量

本轮纳入 20 份岗位：

| 证据级别 | 数量 | 说明 |
|---|---:|---|
| A：完整官方 JD | 17 | OpenAI 4 份、Anthropic 6 份、Cursor 4 份、GitHub 3 份 |
| B：官方 ATS 不完整文本 | 3 | Cognition 3 份，只进行有限编码 |
| 暂不编码 | Qoder | 官方页面可确认岗位目录，但详情正文无法完整读取 |

Qoder 的官方岗位目录显示其招聘覆盖 Agent 研发、产品、运营、解决方案、项目管理、评测及用户研究，但由于岗位正文不足，本轮不以第三方转载补齐。

---

## 2. OpenAI：4 份岗位

### 2.1 Product Manager, Codex Security Controls

- **实际问题**：Agent 获得代码库、工具、凭据和执行权限后，企业如何保持控制。
- **主要交付**：权限模型、审批、审计、回滚、合作伙伴接口和高风险能力上线标准。
- **协作对象**：Codex 研发、安全、Safety、企业客户和安全厂商。
- **技术边界**：要求理解身份、沙箱、Secrets、MCP 和攻击路径，不是纯流程产品岗位。
- **来源**：https://openai.com/careers/product-manager-codex-security-controls-and-partner-interfaces-remote-us/

### 2.2 Deployed Product Manager, Codex

- **实际问题**：客户购买产品后，如何从试验进入真实工作流并扩大使用。
- **主要交付**：部署策略、集成路径、账户扩展、产品反馈和客户内部采用。
- **协作对象**：客户、产品、Deployment Engineering 和 GTM。
- **技术边界**：需要亲自处理 MCP、工具及轻量集成，但不负责核心模型研发。
- **来源**：https://openai.com/careers/deployed-product-manager-codex-san-francisco/

### 2.3 Developer Experience Engineer

- **实际问题**：开发者如何理解、接入并成功使用 Codex 和 API。
- **主要交付**：示例应用、开发者工具、技术内容、演示及开发者旅程优化。
- **协作对象**：产品、研发、研究和 GTM。
- **技术边界**：岗位核心是“亲自构建＋解释＋推广”，不是纯内容运营。
- **来源**：https://openai.com/careers/developer-experience-engineer-san-francisco/

### 2.4 Manager, AI Deployment Engineering—Codex

- **实际问题**：大型企业如何把 Codex 嵌入完整软件开发生命周期。
- **主要交付**：从试点到生产部署、可靠安全的集成方案、规模化推广及部署工程团队建设。
- **协作对象**：企业客户、产品、工程和 GTM。
- **技术边界**：既管理技术团队，也直接参与客户架构、流程和组织采用问题。
- **来源**：https://openai.com/careers/manager-ai-deployment-engineering-codex-munich-germany/

### OpenAI 开放编码观察

OpenAI 没有把企业落地理解成单纯的软件交付，而是拆分为：

> 产品扩展、技术部署、开发者教育和安全控制。

安全产品经理直接参与决定 Agent 能获得多大权限、以何种条件上线，因此安全不是产品完成后的附加合规。

---

## 3. Anthropic：6 份岗位

### 3.1 Product Manager, Claude Code Model Performance

- **实际问题**：如何把底层模型进步转化为开发者实际感知到的能力。
- **主要交付**：Agent 评测、模型发布标准、失败行为分析和产品改进优先级。
- **协作对象**：研究、产品工程、真实用户和竞争评测。
- **技术边界**：要求候选人有构建 Agent 评测的实际经验。
- **来源**：https://job-boards.greenhouse.io/anthropic/jobs/5247640008

### 3.2 Product Manager, Developer Productivity

- **实际问题**：当 Agent 编写、测试和审查更多代码时，企业内部开发系统应如何变化。
- **主要交付**：构建、CI/CD、开发环境、治理框架和 AI 时代生产力指标。
- **协作对象**：研究、基础设施、推理、产品工程和安全。
- **技术边界**：显式处理速度、可靠性、安全和成本取舍。
- **来源**：https://job-boards.greenhouse.io/anthropic/jobs/5220143008

### 3.3 Model Performance SWE, Claude Code

- **实际问题**：Claude Code 如何建立可扩展的评测和研究基础设施。
- **主要交付**：评测框架、实验系统、长期技术架构及产品—研究转换。
- **协作对象**：研究、产品和工程团队。
- **技术边界**：Staff/Principal 级核心工程岗位，要求复杂高风险系统所有权。
- **来源**：https://job-boards.greenhouse.io/anthropic/jobs/5098025008

### 3.4 Staff SWE, Developer Productivity—CI/CD

- **实际问题**：Agent 提高代码产量后，如何避免审查、合并和部署成为瓶颈。
- **主要交付**：AI 辅助审查、CI、合并队列、灰度发布、健康检查和自动回滚。
- **协作对象**：基础设施、产品工程和安全团队。
- **技术边界**：深度平台工程岗位，对“从 Push 到健康生产环境”的完整路径负责。
- **来源**：https://job-boards.greenhouse.io/anthropic/jobs/5271428008

### 3.5 People Research Scientist, Recruiting

- **实际问题**：招聘漏斗、面试方法和人才评估是否有效。
- **主要交付**：验证研究、心理测量、标准指标、分析工具、仪表板和战略建议。
- **协作对象**：招聘、People Analytics 和管理层。
- **技术边界**：要求高级研究方法、统计分析及 SQL、Python 或 R。
- **来源**：https://job-boards.greenhouse.io/anthropic/jobs/5257763008

### 3.6 Workforce Planning Lead

- **实际问题**：公司战略怎样转化为人员数量、结构、地域和能力需求。
- **主要交付**：人员预测模型、Headcount 计划、数据治理和持续调整机制。
- **协作对象**：业务、财务、招聘、HRBP 和人才负责人。
- **技术边界**：核心是把业务战略转译为人力计划，不是普通招聘执行。
- **来源**：https://job-boards.greenhouse.io/anthropic/jobs/5202462008

### Anthropic 开放编码观察

样本中出现两条不同但相互连接的组织线：

1. Claude Code 的模型性能、评测和软件交付基础设施；
2. 招聘研究、人才规划和 People Analytics。

当前证据只能证明 Anthropic 同时建设这两类能力，不能证明第二类岗位由 Claude Code 直接产生。

---

## 4. Cursor：4 份岗位

### 4.1 Software Engineer, Agent Harness

- **实际问题**：模型怎样通过循环、工具、执行环境和 Guardrails 表现为可用 Agent。
- **主要交付**：Agent Harness、工具、模型路由、默认行为、多 Agent 支持和新模型上线。
- **协作对象**：模型、产品和工程团队。
- **技术边界**：深度工程岗位，同时要求在质量、成本和用户体验之间进行产品判断。
- **来源**：https://cursor.com/hi/careers/software-engineer-agent-harness

### 4.2 Software Engineer, Agent Evaluation and Quality

- **实际问题**：如何将“Agent 好不好”转化为可操作、可持续改进的测量系统。
- **主要交付**：数据集、离线回放、评分器、回归告警、仪表板和用户反馈循环。
- **协作对象**：产品、数据和工程团队。
- **技术边界**：相邻经验可能来自搜索质量、排序、实验平台和测量系统。
- **来源**：https://cursor.com/fr/careers/software-engineer-agent-evaluation-and-quality

### 4.3 AI Adoption Engineer

- **实际问题**：大型工程组织购买 Cursor 后，怎样真正改变工作方式。
- **主要交付**：Hackathon、Champion 网络、工作流改造和可持续使用行为。
- **协作对象**：客户工程师、管理层、产品和客户团队。
- **技术边界**：不是只讲幻灯片的培训师，而是需要现场排障并获得工程师信任的技术实践者。
- **来源**：https://cursor.com/careers/ai-adoption-engineer

### 4.4 User Researcher

- **实际问题**：不同能力层级和工作流的开发者究竟需要什么。
- **主要交付**：访谈、可用性测试、问卷、实验及影响路线图的用户洞察。
- **协作对象**：产品、设计、工程和用户。
- **技术边界**：不负责核心 Agent 系统建设，但需在技术产品环境中把定性与定量证据转化为产品决策。
- **来源**：https://cursor.com/cn/careers/user-researcher

### Cursor 开放编码观察

Cursor 将三个问题分得较清楚：

> **如何运行 → 如何衡量 → 如何被组织采用。**

这说明产品完成编码任务只是第一层，质量判断和行为改变也构成独立工作。

---

## 5. GitHub：3 份岗位

### 5.1 Staff SWE, Mission Control

- **实际问题**：不同 IDE、CLI、网页和云端 Agent 会话如何拥有统一生命周期、权限和远程控制。
- **主要交付**：Session 与 Task API、Agent Registry、远程 Steering、策略执行和 Agent Host Protocol。
- **协作对象**：Copilot 各产品表面、平台和安全团队。
- **技术边界**：深度 Go、分布式系统、身份授权和跨客户端架构岗位。
- **来源**：https://www.github.careers/careers-home/jobs/5611?lang=en-us

### 5.2 Principal SWE, Enterprise AI Platform

- **实际问题**：企业中的 Agent 如何跨 IDE、CLI、MCP 和长任务环境安全一致地运行。
- **主要交付**：企业 AI 平台、身份、策略、控制平面和平台架构。
- **协作对象**：产品、安全、平台和企业客户相关团队。
- **技术边界**：高度依赖分布式系统、企业安全、Developer Tooling 和 Agent 平台经验。
- **来源**：https://www.github.careers/early-in-career/jobs/5481?lang=en-us

### 5.3 Senior Product Operations Manager

- **实际问题**：高速迭代的开发者 AI 产品组合如何稳定发布，并用 AI 改造自身运营流程。
- **主要交付**：发布准备、跨团队节奏、风险指标、AI 自动化路线图和采用效果。
- **协作对象**：Product、Engineering、Marketing、Revenue 和 Support。
- **技术边界**：不要求核心平台编码，但要求识别高价值 AI 自动化场景。
- **来源**：https://www.github.careers/careers-home/jobs/5516?lang=en-us

### GitHub 开放编码观察

当 Agent 嵌入大型软件平台后，组织开始处理：

- 会话和任务统一管理；
- 身份、委托和策略跨产品执行；
- 多产品发布与商业团队协同；
- 内部运营流程自身的 Agent 化。

---

## 6. Cognition：3 份 B 级样本

以下岗位来自官方 Ashby 招聘系统，但正文不完整，只进行有限编码。

### 6.1 Deployed Engineer—APAC

- **可确认定位**：面向客户的技术专家，负责售前技术环节、产品演示、Pilot，并帮助工程组织找到适合委托给 Devin 的用例。
- **无法确认**：完整结果指标、具体技术栈和内部协作机制。
- **来源**：https://jobs.ashbyhq.com/cognition/b73fd66a-f43b-4240-95c2-7a76b4ffb0c6

### 6.2 Applied AI Transformation Manager—APAC

- **可确认定位**：面向战略客户的技术型顾问和运营者，从前期战略、价值对齐一直推动到项目交付。
- **无法确认**：是否亲自实施技术方案、量化价值的具体方法。
- **来源**：https://jobs.ashbyhq.com/cognition/be59ef70-1b34-4af5-a831-da964a6d3869

### 6.3 Product Engineer

- **可确认定位**：识别现有产品与理想状态之间的差距，并与工程、产品、GTM 和 Design Partner 合作推进产品。
- **无法确认**：具体产品模块、成功指标和技术深度要求。
- **来源**：https://jobs.ashbyhq.com/cognition/439404bb-3185-4d22-b6df-4a5e39a510d6

---

## 7. 开放编码后自然出现的岗位任务群

这些任务群来自第一遍开放编码，不是预设的六维模型。

### 7.1 Agent 运行系统

涉及 Agent 循环、工具、会话与任务平台、执行环境、模型选择、身份、远程控制和跨产品基础设施。

### 7.2 测量、验证与交付质量

涉及 Agent 评测、真实用户反馈、回归检测、代码审查、CI/CD、上线和回滚标准。

### 7.3 安全、权限和控制

涉及身份、权限、Secrets、工具与网络访问、审批、审计、停止和回滚。

### 7.4 企业部署与采用

涉及技术集成、客户用例发现、Pilot、工作流改造、Champion 建设、生产部署和实际使用。

### 7.5 用户与产品学习

涉及用户需求、使用轨迹、产品假设、模型行为、路线图和开发者教育。

### 7.6 组织运营与人才决策

涉及产品发布运营、内部 AI 工作流、招聘评估有效性、人员预测、数据治理和战略—人力计划转换。

---

## 8. 对上一阶段推断的检验

上一阶段提出：

> AI Coding Agent 可能把部分软件生产活动转化为对数字执行者的管理。

岗位证据提供了部分支持。企业确实在配置人员负责：

- 定义 Agent 行为和工具；
- 管理 Agent 会话和任务；
- 设计评测和发布门槛；
- 决定权限和审批；
- 管理后台 Agent 的生产部署；
- 推动组织采用；
- 建立 AI 产品发布和运营体系。

但现有证据不支持“数字劳动力管理部门已经独立成型”。这些职责目前大多仍分布在工程、产品、安全、Developer Productivity、客户成功和产品运营中。

因此，修正表述为：

> **Agent 化正在为传统职能增加新的管理对象与责任，而不是立即产生一个完全独立的新职业体系。**

---

## 9. 反例与边界

1. **技术专业门槛没有普遍下降。** Staff 或 Principal 级平台岗位仍要求复杂系统所有权、分布式系统和安全架构经验。
2. **新岗位名称未必代表全新职业。** Deployed PM、AI Adoption Engineer 和 AI Transformation Manager 与解决方案工程、技术咨询、客户成功和产品运营存在连续性。
3. **跨职能协作不是所有岗位的核心筛选标准。** 部分核心平台岗位最终仍以深度系统设计和生产工程能力为主。
4. **中国样本仍明显不足。** Qoder 只有岗位目录证据，字节、腾讯及其他国内官方 JD 仍需继续补充。

---

## 10. 阶段判断

> **AI Coding Agent 的组织影响并不只是增加“Agent 工程师”。企业正在围绕完整交付闭环，将 Agent 运行、评测、治理、部署、采用和运营责任配置到一组相互连接的岗位中；但这些责任目前多嵌入既有工程、产品、安全和客户职能，而非形成完全独立的新职业体系。**

## 11. 下一步

在隔离分析中对本轮样本进行第二遍编码：

- 使用六维候选框架；
- 为每项编码保留原始依据；
- 检查重复维度和无法解释的岗位；
- 主动寻找不支持“连接型人才需求上升”的样本；
- 中国岗位证据不足问题单独保留，不以推断补齐。
