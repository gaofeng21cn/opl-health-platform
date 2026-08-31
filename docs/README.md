# OPL Health Platform 文档索引

Owner: `opl-health-platform`
Purpose: `docs_index`
State: `active_index`
Machine boundary: 本索引只导航人读产品规划。运行状态、发布状态、模型接入、资源调度、账单、证据存储和负责人回执仍归对应 OPL Cloud、OPL App、OPL Framework、领域仓及其真实实现面。

OPL Cloud 已经确定为本平台的技术底座，并达到管理员运营下基本可用的阶段。本仓当前仍以产品文档和最小可行试点为主，只定义医疗行业层的需求、责任边界和试点路径；不提前创建通用合同、运行时、服务、账单或临床决策权。

## 当前入口

- [路线图与当前差距](./roadmap.md)：统一维护当前状态、剩余差距和下一轮工作负责人。
- [产品定位](./product-positioning.md)：面向医院、科室、医生、信息化与 AI 团队的产品角色。
- [目标运营模型](./target-operating-model.md)：医院内各角色如何协作。
- [架构总览](./architecture.md)：Health 医疗行业层与 OPL Cloud 通用底座的边界。
- [OPL Cloud 能力使用方式](./opl-cloud-capability-usage.md)：医疗平台如何使用 Cloud、OPL App 和 OPL Framework 能力，并区分当前基线与医疗扩展需求。

## 权威文档映射

本仓不为同一主题创建第二份当前事实：[产品定位](./product-positioning.md) 负责产品角色，[路线图与当前差距](./roadmap.md) 负责当前状态和工作计划，[架构总览](./architecture.md) 负责架构边界。当前文档规划阶段的硬边界由根 `AGENTS.md` 与本索引共同维护；只有出现无法由现有文档承载的长期决策时，才新增独立的决策或不变量文档。

## 长期主题负责人

| 主题 | 权威文档 | 角色 |
| --- | --- | --- |
| 医疗能力包导航 | [医疗能力包](./medical-capability-packs.md) | 只导航 Knowledge、Protocol、Tools 与专病模板的权威文档 |
| 医学知识 | [OPL Health Knowledge](./opl-health-knowledge.md) | 来源、版本、适用范围和维护责任 |
| 临床规则 | [OPL Health Protocol](./opl-health-protocol.md) | 规则依据、人工确认和适用边界 |
| 医疗工具 | [OPL Health Tools](./opl-health-tools.md) | 工具需求、授权和审计要求 |
| 专病模板 | [专病模板体系](./specialty-template-system.md) | 场景输入、输出、审查与交付结构 |
| 医疗智能体与生命周期 | [OPL Health Agents](./opl-health-agents.md) | 智能体类型、绑定、阶段和最小试点路径 |
| 医学审查、合规与责任 | [OPL Health Review](./opl-health-review.md) | 审查对象、证据要求、人工责任边界 |
| 医院部署 | [OPL Health Deployment](./opl-health-deployment.md) | 私有化、专有云、混合部署与科室试点规划 |

## 场景

- [场景地图](./scenario-map.md)
- [专病科研助手](./scenarios/specialty-research-assistant.md)：第一试点建议。
- [专病质控助手](./scenarios/specialty-quality-assistant.md)：第二阶段对照场景。
- [随访管理助手](./scenarios/follow-up-assistant.md)：高风险后置场景。

## 文档规则

- 每个长期主题只保留一份当前权威文档；其他文档只作入口摘要或补充独有信息。
- 当前事实、剩余差距和下一轮提示词只写入 [路线图](./roadmap.md)。
- Health 文档描述需要什么，不替 OPL Cloud、OPL App、OPL Framework 或领域仓声明已经实现、可用或发布。
- 没有真实试点形成重复结构前，不新增完整分类体系、机器合同、运行时或兼容入口。
