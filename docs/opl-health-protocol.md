# OPL Health Protocol

Owner: `opl-health-platform`
Purpose: `clinical_rule_requirements_ssot`
State: `active_planning`
Machine boundary: 本文定义临床规则的产品需求、依据和人工确认边界，不拥有规则运行时、临床决策 authority、部署状态或质量 verdict。

OPL Health Protocol 是 OPL Health Platform 的临床规则能力层。

它把临床路径、质控指标、纳入排除标准、风险分层、随访规则和审查要求整理成可复用、可审批、可追踪的规则包。

## 核心内容

- 临床路径和诊疗流程。
- 质控指标和管理口径。
- 纳入标准、排除标准和分层规则。
- 随访周期、提醒条件和结果格式。
- 科研筛选、数据核查和报告审查规则。

## 规则包记录

每个临床规则包应记录：

- 规则名称。
- 适用场景。
- 规则依据。
- 输入要求。
- 输出格式。
- 人工确认点。
- 负责人和审查记录。

## 规则类型

| 类型 | 说明 |
| --- | --- |
| 路径规则 | 组织诊疗、科研或质控流程 |
| 筛选规则 | 支持病例、文献、项目或数据筛选 |
| 分层规则 | 支持风险分层、优先级和任务分派 |
| 审查规则 | 检查引用、计算、格式、合规和交付质量 |

## 与 OPL Cloud 的关系

规则包是医疗智能体产品需求的一部分。其可消费引用由对应 package、领域和平台 owner 管理；Workspace 或其他产品面可以展示 owner 提供的结果与引用，Ledger 等证据面可以记录相应回执。Health 不创建第二套 package registry、运行状态或 receipt authority。
