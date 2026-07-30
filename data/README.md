# 数据目录说明

本目录保存研究中的结构化底稿。CSV 文件采用 UTF-8 编码，字段名使用英文，便于后续用 Excel、Python 或数据可视化工具处理。

## 文件

- `product-mapping.csv`：产品样本、入口、产品形态与研究状态。
- `company-mapping.csv`：公司类型、核心资源、产品组合与人才研究状态。
- `talent-role-mapping.csv`：岗位族群、职责、能力和典型背景。
- `job-posting-analysis.csv`：逐条公开招聘岗位的结构化样本。

## 通用值规范

### 研究状态

- `candidate`：候选样本，尚未完成基础核验；
- `verified`：核心字段已由官方来源核验；
- `in_research`：正在进行深度研究；
- `completed`：已完成当前版本分析；
- `needs_review`：因时间或产品变化需要复核。

### 置信度

- `high`
- `medium`
- `low`
- `unrated`

### 缺失值

使用空值，不使用 `0`、`unknown` 或推测性内容填充。确实不适用时使用 `N/A`。

## 数据录入要求

1. 动态字段必须填写 `accessed_date` 或 `collected_date`。
2. 产品功能和公司信息优先关联官方来源。
3. 评分字段必须能够追溯到测试记录或明确证据。
4. 公开岗位失效后将 `posting_status` 改为 `closed` 或 `expired`，不删除历史记录。
5. 不收集私人联系方式、家庭信息或其他与职业研究无关的数据。
6. AI 生成或补全的字段在人工核验前不得标记为 `verified`。

## 版本管理

对字段结构的重大修改应在 Pull Request 中说明：

- 新增或删除了哪些字段；
- 是否影响既有记录；
- 是否需要迁移或重新编码；
- 数据快照日期是否变化。
