# 六维框架 v0.2 重新编码与反例检验

> 观察截止：2026-07-30  
> 状态：作者已确认的交付四  
> 样本：17份A级完整官方JD；3份Cognition B级样本保留为NA  
> 方法：使用已冻结的六维能力组合框架v0.2进行第二遍编码，不计算总分。

## 1. 编码规则

本轮使用：

- V：价值选择与优先级；
- P：问题结构化与产品定义；
- T：技术判断与系统理解，必须附T-Domain；
- A-S：Agent System；
- A-W：Agent Workflow；
- G-E：Evidence and Evaluation；
- G-R：Risk and Control；
- O：边界转换与组织推动；
- M：研究与测量方法；
- D：端到端交付责任，并增加D-Scope；
- C：客户与商业情境；
- E/I/0/NA：证据类型。

禁止将维度相加形成岗位或候选人总分。

## 2. 17份A级JD重新编码

| ID | 岗位简称 | 能力组合 |
|---|---|---|
| JD001 | Codex Security PM | `V2E P2E T2E[安全/IAM/Agent安全] A(1E,2E) G(2E,2E) O2E；M1E D2E[Product] C1E` |
| JD002 | Codex Deployed PM | `V2E P2E T1E[企业技术集成] A(0,1E) G(0,0) O2E；M0 D2E[Customer] C2E` |
| JD003 | Developer Experience Engineer | `V1E P1E T2E[全栈AI应用/DevEx] A(1I,1E) G(1E,0) O2E；M0 D2E[Product] C1E` |
| JD004 | Deployment Engineering Manager | `V2E P1E T2E[企业AI部署/SDLC] A(1I,2E) G(1E,1E) O2E；M0 D2E[Customer] C2E` |
| JD005 | Claude Code Performance PM | `V2E P2E T2E[模型行为/Agent评测] A(1I,1E) G(2E,1E) O2E；M2E D2E[Product] C1E` |
| JD006 | Developer Productivity PM | `V2E P2E T2E[开发基础设施/CI-CD/AI工具] A(1I,2E) G(2E,2E) O2E；M1E D2E[Organization] C0` |
| JD007 | Model Performance SWE | `V1E P1E T2E[评测基础设施/研究系统] A(0,1E) G(2E,1E) O1E；M2E D2E[System] C0` |
| JD008 | CI/CD Staff SWE | `V1E P0 T2E[CI-CD/发布工程] A(0,1E) G(2E,2E) O1E；M1E D2E[System] C0` |
| JD009 | People Research Scientist | `V1E P1I T1E[People Science/统计] A(0,0) G(2E,1E) O2E；M2E D1E[Research] C0` |
| JD010 | Workforce Planning Lead | `V2E P0 T1E[People Analytics/人力规划] A(0,0) G(1E,1E) O2E；M2E D2E[Organization] C0` |
| JD011 | Agent Harness SWE | `V1E P2E T2E[Agent Harness/平台] A(2E,1I) G(1E,1E) O1E；M1E D2E[System] C0` |
| JD012 | Agent Evaluation SWE | `V1E P1E T2E[Agent评测/测量基础设施] A(1E,0) G(2E,1E) O1E；M2E D2E[System] C0` |
| JD013 | AI Adoption Engineer | `V2E P1E T1E[开发者工具/AI辅助工作流] A(0,1E) G(1E,0) O2E；M1E D2E[Customer] C2E` |
| JD014 | User Researcher | `V1E P1E T1E[用户研究/技术产品] A(0,0) G(2E,0) O2E；M2E D1E[Research] C0` |
| JD015 | Mission Control Staff SWE | `V0 P0 T2E[分布式系统/API/IAM/Agent平台] A(2E,1I) G(1E,2E) O1E；M0 D2E[System] C0` |
| JD016 | Enterprise AI Platform Principal | `V1E P0 T2E[分布式系统/企业AI控制平面] A(2E,1I) G(1E,2E) O1E；M0 D2E[System] C1I` |
| JD017 | Product Operations Manager | `V2E P2E T1E[AI产品运营/自动化] A(0,1E) G(2E,1E) O2E；M1E D2E[Organization] C1E` |

完整结构化结果见`data/jd-six-dimension-coding-v0.2.csv`。

## 3. 编码分布

下表仅描述本轮17份定向探索样本，不代表行业岗位比例。

| 项目 | 核心要求：2 | 至少涉及：≥1 | 无证据：0 |
|---|---:|---:|---:|
| V 价值选择 | 8 | 16 | 1 |
| P 产品定义 | 6 | 13 | 4 |
| T 技术判断 | 11 | 17 | 0 |
| A-S Agent系统 | 3 | 9 | 8 |
| A-W Agent工作流 | 3 | 13 | 4 |
| G-E 证据与评测 | 9 | 16 | 1 |
| G-R 风险与控制 | 5 | 13 | 4 |
| O 组织连接 | 11 | 17 | 0 |
| M 研究与测量 | 6 | 12 | 5 |
| D 端到端责任 | 15 | 17 | 0 |
| C 客户与商业情境 | 3 | 8 | 9 |

这些计数不用于比较岗位价值，也不用于给候选人排名。

## 4. 对v0.2框架的检验

### 4.1 A-S与A-W的拆分有效

A-S=2只出现在Agent Harness、Mission Control和Enterprise AI Platform。这些岗位直接建设Agent循环、工具、会话、任务或控制平面。

A-W=2出现在Codex Security PM、Deployment Engineering Manager和Developer Productivity PM。它们主要设计Agent在真实组织中的权限、审批、执行方式和人机工作流。

本样本没有岗位同时获得A-S=2与A-W=2，说明“建设Agent系统”和“设计组织如何使用Agent”是不同能力来源。

### 4.2 G-E与G-R的拆分有效

Agent Evaluation、People Research和User Research主要解决如何产生可信证据；Mission Control、Enterprise AI Platform和Codex Security主要解决权限、策略、审计和风险边界。

评测人才与风险控制人才不能使用单一G分值代替。

### 4.3 T-Domain是必要字段

17份A级JD全部至少需要技术或专业方法判断，但领域包括Agent Harness、分布式系统、安全/IAM、CI/CD、评测工程、企业集成、People Science、人力规划和用户研究。

相同的T分值不代表人才可直接互换。人才Mapping必须同时比较T-Domain及其行为证据。

### 4.4 O的严格定义能够识别反例

Model Performance SWE、CI/CD Staff SWE、Agent Harness、Agent Evaluation、Mission Control和Enterprise AI Platform均为O=1。它们需要跨团队合作，但跨边界转换不是主要交付。

因此，连接能力在部署、采用、产品、研究转化和组织决策岗位中更重要，但不是所有Agent岗位的共同核心要求。

### 4.5 V与O仍需防止重复编码

本轮V=2岗位普遍同时为O=2，因为战略、部署和运营岗位往往既决定方向，也推动多方执行。

两者仍须严格区分：

- V：决定目标、优先级和取舍；
- O：使不同主体围绕目标完成行动和结果。

仅出现“跨团队推动”不能自动同时编码为V2和O2。

## 5. 横向标签检验

### M：有效区分证据生产能力

M2集中于模型性能、Agent评测、People Research、Workforce Planning和User Research。这些岗位需要自行设计实验、数据集、测评、研究或统计模型。

### C：有效分离客户型岗位

C2只出现在Codex Deployed PM、Deployment Engineering Manager和AI Adoption Engineer。其主要结果直接涉及客户采用、生产部署或行为改变。

### D：当前样本出现饱和

17份岗位中15份为D2，主要因为样本偏向高级、Staff、Principal、Lead和Manager岗位。

保留D，但增加`D-Scope`：System、Product、Customer、Organization或Research，用于记录端到端责任的对象，不增加第七个主维度。

## 6. 六类岗位能力原型

### 原型一：Agent系统建设者

`T2 + A-S2 + G-R1/2 + O1 + D2[System]`

代表：Agent Harness、Mission Control、Enterprise AI Platform。

### 原型二：评测与可靠性交付者

`T2 + G-E2 + M1/2 + O1 + D2[System]`

代表：Model Performance SWE、Agent Evaluation、CI/CD。

### 原型三：Agent产品与控制设计者

`V2 + P2 + A-W1/2 + G-E/G-R + O2`

代表：Codex Security PM、Developer Productivity PM、Claude Code Performance PM。

### 原型四：技术型部署与采用连接者

`V2 + T1/2 + A-W1/2 + O2 + D2[Customer] + C2`

代表：Deployed PM、Deployment Engineering Manager、AI Adoption Engineer。

### 原型五：证据—决策转换者

`T1/2[专业方法] + G-E2 + M2 + O2`

代表：People Research、User Research及部分模型性能产品岗位。

### 原型六：组织规划与运营转化者

`V2 + P0/2 + G-E1/2 + O2 + D2[Organization]`

代表：Workforce Planning、Product Operations。

## 7. 关键反例

1. **Agent岗位不一定需要产品定义。** Mission Control和Enterprise AI Platform为P0，但仍是Agent系统关键岗位。
2. **AI公司岗位不一定需要Agent能力。** People Research、Workforce Planning和User Research的A-S/A-W均为0。
3. **采用岗位不等于深度Agent工程岗位。** AI Adoption Engineer的核心是技术可信度、客户工作流和行为改变，而不是建设Agent循环。
4. **Agent带来的新瓶颈可能由传统平台岗位解决。** CI/CD Staff SWE不建设Agent核心，却负责Agent代码产量提升后的测试、合并、发布和回滚瓶颈。

这些反例支持：Agent化正在改变既有职能的工作对象和责任，而不是只创造带有“Agent”名称的新岗位。

## 8. 框架决定

v0.2通过本轮初步检验，暂不增加第七个主维度。

保留：

- V、P、T、A、G、O；
- A-S/A-W；
- G-E/G-R；
- M、D、C；
- T-Domain；
- E、I、0、NA。

新增辅助字段：`D-Scope`。

框架的正确用途是描述岗位解决能力瓶颈时所需的能力组合，并据此寻找具有相似问题解决证据的人才。不得计算总分，不得将不同T-Domain视为直接可替代，也不得宣称连接型人才适用于全部Agent岗位。

## 9. 阶段结论

> **AI Coding Agent相关人才需求不是一种统一的“AI人才能力”，而是由多种能力原型构成。Agent系统岗位以技术、Agent系统和风险控制为核心；评测岗位以技术、证据和测量方法为核心；部署、采用和组织岗位则更依赖价值判断、技术可信度、跨边界转换及端到端结果责任。**

因此，人才Mapping不能从岗位名称直接寻找同名人才，而应沿着以下链条展开：

> **能力瓶颈 → 能力原型 → 专业领域 → 责任情境 → 候选人行为证据**

## 10. 证据与样本边界

- 样本为定向探索样本，不能推断行业岗位比例；
- 中国官方JD样本仍不足；
- 3份Cognition B级样本因正文不完整保留NA；
- 本轮由同一研究过程完成，尚未进行独立编码者一致性检验；
- JD描述的是岗位意图，不等同于真实组织结构或实际招聘结果。

下一阶段进入交付五：人才Mapping方法。