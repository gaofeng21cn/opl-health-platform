# 医疗能力包

Owner: `opl-health-platform`
Purpose: `medical_capability_owner_index`
State: `active_index`
Machine boundary: 本文只导航 Health 人读能力 owner，不定义机器包、安装状态、运行能力或质量结论。

医疗能力包是 OPL Health Platform 组织医疗产品需求的四类人读 owner。具体内容只在对应文档维护，本页不复制第二份清单。

| 能力 | Single Source of Truth | 负责什么 | 不负责什么 |
| --- | --- | --- | --- |
| OPL Health Knowledge | [医学知识](./opl-health-knowledge.md) | 来源、版本、适用范围、维护和审查要求 | 文件存储、数据库运行状态、检索 ready |
| OPL Health Protocol | [临床规则](./opl-health-protocol.md) | 规则依据、输入输出、人工确认和适用边界 | 通用流程引擎、临床决策 authority |
| OPL Health Tools | [医疗工具](./opl-health-tools.md) | 医疗数据源、院内系统和专业工具的产品需求 | 连接器实现、权限系统、工具运行状态 |
| 专病模板 | [专病模板体系](./specialty-template-system.md) | 把知识、规则、工具、审查和交付要求组织成场景入口 | 智能体运行时或交付 ready |

[OPL Health Agents](./opl-health-agents.md) 消费这些能力定义形成医疗智能体产品需求；[OPL Health Review](./opl-health-review.md) 统一持有审查、合规和人工责任边界。OPL Cloud、App、Framework 与领域仓继续持有各自机器合同、运行状态和交付 authority。
