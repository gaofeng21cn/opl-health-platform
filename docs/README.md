# OPL Health Platform 文档索引

Owner: `opl-health-platform`
Purpose: `docs_index`
State: `active_index`
Machine boundary: 本索引只导航人读产品规划。运行状态、发布状态、模型接入、资源调度、账单、证据存储和负责人回执仍归对应 OPL Cloud、OPL App、OPL Framework、领域仓及其真实实现面。

本索引按唯一主题导航。产品阶段与试点缺口见路线图，文档维护和退役规则只在根
[AGENTS.md](../AGENTS.md)维护。

## 当前入口

- [路线图与当前差距](./roadmap.md)：维护试点状态、剩余决策和进入实现的条件。
- [产品定位](./product-positioning.md)：面向医院、科室、医生、信息化与 AI 团队的产品角色。
- [目标运营模型](./target-operating-model.md)：医院内各角色如何协作。
- [架构总览](./architecture.md)：Health 医疗行业层与 OPL Cloud 通用底座的边界。
- [OPL Cloud 能力使用方式](./opl-cloud-capability-usage.md)：医疗平台如何使用 Cloud、OPL App 和 OPL Framework 能力，并区分当前基线与医疗扩展需求。

## 权威文档映射

根 README 是双语公开介绍；产品定位定义用户和品牌，目标运营模型定义医院角色与协作，
架构定义行业与通用平台的分工，Cloud 使用方式定义集成需求。场景地图比较候选，
每份场景文档只持有该场景的输入输出、人工确认与交付要求。

## 长期主题负责人

| 主题 | 权威文档 | 角色 |
| --- | --- | --- |
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
