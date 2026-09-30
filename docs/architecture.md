# 架构总览

Owner: `opl-health-platform`
Purpose: `health_industry_architecture`
State: `active_planning`
Machine boundary: 本文只定义 Health 医疗行业层的人读架构边界，不负责声明 Cloud、App、Framework 的运行、部署或发布状态。

OPL Health Platform 采用“医疗行业层 + OPL Cloud 通用底座”的结构。

```text
医院用户与管理团队
        │
        ▼
OPL Health Platform
├─ OPL Health Knowledge
├─ OPL Health Protocol
├─ OPL Health Tools
├─ OPL Health Agents
├─ 专病模板体系
├─ OPL Health Review
└─ OPL Health Deployment
        │
        ▼
OPL Cloud
├─ OPL Console / Control Plane
├─ OPL Workspace / App 集成
├─ OPL Gateway
├─ OPL Fabric
└─ OPL Ledger
```

## 能力分层

```text
医学资料与规则
├─ OPL Health Knowledge
└─ OPL Health Protocol

工具与资源
├─ OPL Health Tools
└─ OPL Health Deployment

智能体与交付
├─ OPL Health Agents
├─ 专病模板
└─ OPL Health Review
```

## 分工

**OPL Health Platform 负责医疗行业能力。**

它定义医院需要哪些医学知识、临床规则、医疗工具、专病模板、医疗智能体、审查机制和部署方案。

当前阶段只维护产品和架构文档。本仓记录医疗产品需求、能力包、审查策略、部署模型和 Cloud 能力引用关系，不接管通用运行时、工作空间执行、资源调度、模型网关、账单、证据存储或发布状态。只有真实试点形成稳定、重复的结构后，才考虑抽取机器可读合同。

**OPL Cloud 负责通用平台能力。**

它提供工作空间、管理控制台、模型接入、资源连接、计量、任务回执和证据能力。OPL Gateway 是稳定的模型接入产品抽象，本仓不记录或依赖它当前采用的具体实现。

### 已确定的技术边界

| 边界 | OPL Cloud 负责什么 | OPL Health Platform 如何扩展 |
| --- | --- | --- |
| 账户与工作空间 | Console 提供界面，Control Plane 提供账户、策略和工作空间编排接口 | 定义医院、科室、项目和医疗角色需要的产品规则 |
| 模型接入 | OPL Gateway 提供统一的模型接入、路由和用量能力 | 定义医疗场景允许使用的模型、额度和敏感任务策略 |
| 资源与运行环境 | Fabric 通过统一边界管理计算、存储、环境、连接器和实际资源状态 | 定义医学资料、医疗工具和院内资源的接入要求 |
| 回执与来源 | Ledger 保存回执、对账证据和调用方提供的来源引用 | Health 和医院持有医学审查规则、审查结果和继续授权 |
| 服务协作 | Cloud 持有通用服务边界、公开接口和数据 authority；具体拓扑与传输由其实现合同决定 | 医疗层只通过公开接口消费能力，不跨服务写入数据，也不复制通用状态 |

Cloud 的[当前实现架构](https://github.com/gaofeng21cn/opl-cloud/blob/main/docs/implementation-architecture.md)
持有源码拓扑与保留路径；公开发布和实例运行状态分别以其发布负责人和 Instance 回执为准。
本仓不保存跨仓可用性快照。医疗需求如何映射到公开平台能力见
[Cloud 能力使用方式](opl-cloud-capability-usage.md)。

**OPL Framework 和 OPL Meta Agent（OMA）负责智能体构建基础。**

OMA 可支持医疗智能体的语义设计、评估和改进。OPL Framework 持有通用 runtime、Package
发现、carrier 委托和 installed aggregation；研究流程、医学质量判断、阶段与产物权威归
相应领域实现和医院负责人，不能由 Framework 代为签发。

## 最小落地链路

```text
医疗场景定义
→ 医学知识包 / 临床规则包 / 医疗工具包
→ 医疗智能体包
→ 管理端审批
→ 工作空间启用
→ 任务运行
→ 审查与交付记录
```

这一链路先覆盖一个专病或科研场景，再逐步扩展到更多科室和医院级管理能力。

## 规划方法

当前阶段先用真实场景压测平台设计，再进入具体合同和实现。

优先场景是专病科研助手。它可以同时验证医学知识、临床规则、医疗工具、智能体流程、审查记录和工作空间交付，同时把临床决策和患者触达风险控制在较低范围。

专病质控助手和随访管理助手作为扩展场景，用于检查平台是否能够支持更强的数据接入、权限治理、人工确认和责任边界。
