# OPL Health Agents

Owner: `opl-health-platform`
Purpose: `medical_agent_and_lifecycle_ssot`
State: `active_planning`
Machine boundary: 本文定义医疗智能体产品需求和人读生命周期，不拥有 OPL Package、运行时、发布、部署、任务状态、质量 verdict 或 owner receipt。

OPL Health Agents 是 OPL Health Platform 的医疗智能体能力层。

它把医学知识、临床规则、医疗工具和专病模板组合成可测试、可审批、可部署、可复查的医疗智能体。

## 智能体类型

| 类型 | 典型任务 |
| --- | --- |
| 专病助手 | 病例整理、指南匹配、随访计划、专病科研 |
| 科研助手 | 文献证据、变量口径、统计流程、报告生成 |
| 质控助手 | 指标核查、流程提醒、异常发现、改进建议 |
| 管理助手 | 科室材料、项目进展、会议汇报、运营分析 |
| 审查助手 | 引用、计算、图表、合规和交付质量检查 |

## 智能体记录

每个医疗智能体应记录：

- 目标用户和适用场景。
- 能力边界。
- 输入和输出。
- 绑定的知识包、规则包和工具包。
- 测试案例和审查结果。
- 版本、负责人和发布范围。

## 生命周期阶段

| 阶段 | 主要产物 | 主要责任人 |
| --- | --- | --- |
| 场景定义 | 用户、任务边界、输入输出、风险点 | 医疗产品负责人、科室专家 |
| 智能体蓝图 | 角色、能力、工具、规则、交付格式 | AI 团队、OMA 语义设计支持 |
| Health 能力绑定 | Knowledge、Protocol、Tools、专病模板 | 医疗内容负责人、信息化团队 |
| 测试与审查 | 测试案例、失败案例、审查记录 | 科室专家、AI 团队 |
| 发布审批 | 版本、权限、资源、适用范围 | 医院管理 owner 与真实发布 owner |
| 工作空间启用 | 获批入口、用户和项目空间 | 对应 Workspace / App / Console owner |
| 任务运行与留证 | 任务、工具调用、产物、审查引用 | 用户、领域 owner、运行与证据 owner |
| 版本更新 | 变更说明、回归检查、重新审批 | 医疗产品、平台和医院 owner |

这张表是责任与产物地图，不是已实现的自动流程，也不把 Health 变成运行或发布 owner。

## 最小试点路径

第一版只规划一个医疗智能体：选择明确专病场景，绑定最小 Knowledge、Protocol、Tools 与 Review 要求，使用固定案例接受专家审查，再由对应产品和运行 owner 决定是否进入工作空间试点。

## 与 OPL Cloud 的关系

Health 定义医疗智能体的产品需求、能力绑定和责任边界。OPL Packages（由 OPL Framework 持有）承载通用 package identity 与生命周期；OPL Cloud、App 和领域 owner 只按各自边界消费确切引用、提供产品或运行面。Health 不创建第二套 package registry、package lock、任务账本或发布状态。
