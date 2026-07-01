# 架构总览

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
├─ Workspace / App
├─ Console
├─ Gateway
├─ Fabric
└─ Ledger
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

当前阶段的边界只落在人读产品和架构文档中。本仓只记录医疗产品需求、能力包、审查策略、部署模型和 Cloud 能力引用关系；运行时、工作空间执行、资源调度、模型网关、账单、证据存储、发布 currentness 和 owner receipt 仍归各自实现面。机器可读合同应等试点形成重复结构后再抽取。

**OPL Cloud 负责通用平台能力。**

它提供工作空间、管理控制台、模型接入、资源连接、计量、任务回执和证据记录。

**OPL Framework 和 OMA 负责智能体构建基础。**

OMA 可用于设计、测试和改进医疗智能体；OPL Framework 负责长期任务、阶段推进、文件、证据和交付边界。

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
