# 发布一致性抽查 v0.1

> 抽查日期：2026-07-30  
> 抽查对象：`report/full-report-draft-v0.2.md`、`data/claim-evidence-index-v0.1.csv`、`report/executive-summary-v0.1.md`、`README.md`  
> 范围：仓库内部结构、Claim ID、相对链接、术语、样本数字和发布入口。  
> 本次抽查不等同于重新联网核验全部外部产品页面与招聘页面。

## 1. 抽查结论

当前仓库已具备公开探索性研究作品的完整入口：

- README 提供项目说明、核心结论、阅读顺序和研究边界；
- 执行摘要可供非研究读者快速阅读；
- 完整报告包含七章正文和三个附录；
- 44 项主张—证据索引提供来源定位、反例和公开措辞；
- 方法、数据、模板和阶段复核文件均保留在仓库中。

本轮未发现阻止合并到 `main` 的内部一致性错误。

## 2. Claim ID 抽查

### 索引完整性

- CSV 表头加 C01—C44 共 45 行；
- Claim ID 从 C01 到 C44 连续，无重复编号；
- C24 的证据等级和来源等级为 `NA`，状态为“待补证”；
- C35—C37 保留至附录；
- C07 状态为“合并”，已并入 C01。

### 报告引用

- 完整报告引用 C01—C06、C08—C44；
- 报告未引用 C07，符合其“合并”状态；
- 未发现报告引用不存在的 Claim ID；
- 未发现索引中除 C07 外的核心主张被意外遗漏。

## 3. 样本数字与方法口径

以下数字在 README、执行摘要、完整报告和索引中保持一致：

- 六个核心产品；
- 20 份定向岗位样本；
- 17 份 A 级完整官方 JD；
- 3 份 B 级有限材料；
- Qoder 仅保留岗位目录信号；
- 17 份 A 级 JD 进入第二遍编码；
- 44 项主张—证据记录；
- 六类任务群；
- 六类探索性岗位能力原型；
- 九类能力瓶颈。

报告持续声明定向样本不能用于推断行业岗位比例、规模或增长率。

## 4. 术语一致性

通过的术语规则：

- 使用“Agent 交付系统”，不把产品变化简化为更长代码生成；
- 使用“六类探索性岗位能力原型”，不称为行业标准分类；
- 使用“连接型能力在边界岗位中获得条件性支持”，不泛化为所有 Agent 岗位；
- 区分 A-S/A-W 与 G-E/G-R；
- T-Domain 与 D-Scope 保持为必要情境字段；
- 人才 Mapping 被表述为补充岗位名称搜索的方法建议；
- 不计算岗位或候选人统一总分；
- “数字劳动力管理”只作为受限研究解释，不作为已形成的正式职业体系。

## 5. 内部链接抽查

完整报告引用的以下文件均存在于当前研究分支：

- `data/claim-evidence-index-v0.1.csv`
- `methodology/research-design-v1.md`
- `methodology/six-dimension-framework-v0.2.md`
- `review/full-report-evidence-audit-v0.1.md`
- `report/product-capability-evolution-matrix-v0.1.md`
- `report/capability-bottleneck-matrix-v0.1.md`
- `data/jd-open-coding-v0.1.md`
- `data/jd-sample-register-v0.1.csv`
- `data/jd-six-dimension-coding-v0.2.csv`
- `report/six-dimension-framework-review-v0.2.md`
- `methodology/talent-mapping-method-v0.1.md`
- `templates/candidate-evidence-card-v0.1.md`
- `data/talent-source-archetype-matrix-v0.1.csv`
- `report/ai-organizational-capability-intelligence-role-v0.1.md`
- `data/target-role-capability-profile-v0.1.csv`

README 中列出的执行摘要、完整报告、证据索引、方法和数据入口也均存在。

## 6. 表格与 Markdown 结构

抽查确认：

- 完整报告的产品、岗位分层、能力原型、判断门槛、证据层级和假设表均有完整表头与分隔行；
- 章节层级从七章正文进入附录 A—C，没有标题编号冲突；
- README 目录树与当前发布文件一致；
- CSV 采用单行表头和 44 条主张记录；
- 未发现正文中残留的空表、未闭合代码块或失配的相对路径。

## 7. 保留但不阻塞发布的限制

以下内容仍是研究限制，不是本轮可通过格式校对消除的问题：

- 中国官方岗位样本不足；
- 尚未进行独立编码者一致性检验；
- H3b 缺少同名岗位跨公司配对样本；
- 目标岗位官方链接未恢复；
- 产品和岗位页面可能在观察截止日后变化；
- 未开展产品真实任务性能评测和人才 Mapping 对照实验。

这些限制已在报告、摘要和 README 中披露，因此不阻止作为探索性研究快照发布。

## 8. 发布决定

基于本次内部一致性抽查：

> **当前成果可以合并到 `main`，作为观察截止于 2026-07-30 的公开探索性研究快照。**

后续更新应通过新的分支或 PR 进行，不直接覆盖本次快照的证据边界。
