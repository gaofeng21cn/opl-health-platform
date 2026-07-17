# OPL Health Platform 文档索引

Owner: `opl-health-platform`
Purpose: `docs_index`
State: `active_index`
Machine boundary: 本索引只导航人读产品规划。运行状态、发布状态、模型接入、资源调度、账单、证据存储和负责人回执仍归对应 OPL Cloud、App、Framework、领域仓及其真实实现面。

本仓当前保持 `docs-only / MVP-first`。文档只定义医疗行业层的产品需求、责任边界和最小试点路径；不提前创建合同、运行时、服务、账单或临床决策 authority。

## 当前入口

- [路线图与当前差距](./roadmap.md)：唯一当前状态、剩余差距和下一轮工作 owner。
- [产品定位](./product-positioning.md)：面向医院、科室、医生、信息化与 AI 团队的产品角色。
- [目标运营模型](./target-operating-model.md)：医院内各角色如何协作。
- [架构总览](./architecture.md)：Health 医疗行业层与 OPL Cloud 通用底座的边界。
- [OPL Cloud 能力使用方式](./opl-cloud-capability-usage.md)：Health 如何消费 Cloud / App / Framework 能力，不复制其机器真相。

## Canonical 文档映射

本仓不为通用文件名创建第二份 truth：`project` 角色由 [产品定位](./product-positioning.md) 承担，`status / active plan` 角色由 [路线图与当前差距](./roadmap.md) 承担，架构角色由 [架构总览](./architecture.md) 承担。当前 docs-only 阶段的硬边界由根 `AGENTS.md` 与本索引的文档规则共同持有；只有出现无法由现有 owner 承载的 durable 决策时，才新增独立 decisions/invariants 文档。

## 长期主题 owner

| 主题 | Single Source of Truth | 角色 |
| --- | --- | --- |
| 医疗能力包导航 | [医疗能力包](./medical-capability-packs.md) | 只导航 Knowledge、Protocol、Tools 与专病模板 owner |
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

- 每个长期主题只保留一个当前 owner；其他文档只作入口摘要或独有支撑。
- 当前事实、剩余差距和下一轮提示词只写入 [路线图](./roadmap.md)。
- Health 文档描述需要什么，不替 OPL Cloud、App、Framework 或领域仓声明已经实现、可用、发布或 ready。
- 没有真实试点重复结构前，不新增完整 taxonomy、机器合同、运行时或兼容入口。
