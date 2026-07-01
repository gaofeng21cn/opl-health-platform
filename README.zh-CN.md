<p align="center">
  <img src="assets/branding/opl-health-platform-logo.png" alt="OPL Health Platform 标志" width="132" />
</p>

<p align="center">
  <a href="./README.md">English</a> | <a href="./README.zh-CN.md"><strong>中文</strong></a>
</p>

<h1 align="center">OPL Health Platform</h1>

<p align="center"><strong>面向医院的医疗元智能体平台</strong></p>
<p align="center">医学知识 · 临床规则 · 医疗工具 · 专病智能体 · 审查交付</p>

<!--
Owner: `opl-health-platform`
Purpose: `public_health_platform_entry`
State: `planning_public_entry`
Machine boundary: 人读产品与规划入口。通用云能力、工作空间、控制台、资源调度、模型接入、证据记录和运行状态的机器真相，仍以 OPL Cloud、相关实现仓库、服务、合同、运行输出和负责人回执为准。
-->

## 为什么需要 OPL Health Platform

医院正在面对一类新的 AI 需求：能够围绕真实业务持续工作、沉淀专业能力、支撑审查交付的医疗智能体系统。

这类系统需要同时处理医学知识、临床规则、院内数据、专科流程、工具调用、审查记录和交付结果：

- 医生希望智能体理解专科语境、临床规则和患者资料边界。
- 科室希望把专病经验、科研流程和质控要求沉淀成可复用能力。
- 医院希望系统可以私有化部署，接入院内数据和计算资源。
- 管理团队希望看到权限、审计、用量、风险控制和结果来源。
- AI 团队希望用统一框架开发、测试、发布和治理医疗智能体。

**OPL Health Platform 面向医院建设这套医疗元智能体平台。**

它把 OPL Cloud 的通用 AI 基础设施转化为医疗行业产品：在统一的工作空间、管理控制台、资源底座和证据记录之上，定义医学知识包、临床规则包、医疗工具包、专病模板、医疗审查机制和医院部署方案。

## 产品定位

OPL Health Platform 是 OPL 面向医疗行业的产品线入口。

| 层级 | 名称 | 定位 |
| --- | --- | --- |
| 医疗品牌线 | **OPL Health** | 面向医疗机构的 OPL 产品族 |
| 院级主平台 | **OPL Health Platform** | 面向医院的医疗元智能体平台 |
| 智能体构建 | **OPL Health Studio** | 医疗智能体、专病流程、知识包和规则包的开发与配置 |
| 医疗系统接入 | **OPL Health Connect** | HIS、EMR、LIS、PACS、文献库、数据库和院内工具接入 |
| 场景应用集合 | **OPL Health Apps** | 专病智能体、科研助手、质控助手、随访助手和管理助手 |
| 技术底座 | **Powered by OPL Cloud** | 工作空间、控制台、资源、模型接入、计量和证据能力 |

第一阶段先建设 **OPL Health Platform** 的总体规划、能力边界和最小可落地路径。Studio、Connect 和 Apps 可以随着真实场景逐步产品化。

当前阶段的仓库边界保持极薄。机器可读边界见
[`contracts/opl-health-platform-boundary.json`](contracts/opl-health-platform-boundary.json)：
Health 负责医疗产品需求、能力包、审查策略和部署模型；它只消费
OPL Cloud / App / Framework 的引用和回执，不接管运行时、资源调度、账单、
模型接入、证据存储、发布 currentness 或临床决策 authority。

<p align="center">
  <img src="assets/branding/opl-health-platform-overview.png" alt="OPL Health Platform 产品关系图" width="100%" />
</p>

## 核心能力

**OPL Health Agents**<br/>
围绕专病、科研、质控、随访、病历整理、指南匹配、文献证据和管理流程建设可治理的医疗智能体。

**OPL Health Knowledge**<br/>
沉淀指南、共识、教材、文献、医院制度、科室材料和项目资料，并记录来源、版本、适用范围和更新机制。

**OPL Health Protocol**<br/>
把临床路径、质控指标、纳入排除标准、风险分层、随访规范和审查要求整理成可复用规则。

**OPL Health Tools**<br/>
接入院内系统、数据库、文献源、统计分析、图表生成、报告生成和科研工具。

**专病模板**<br/>
围绕高频专科场景提供任务模板、数据要求、审查标准、结果格式和交付路径。

**OPL Health Review**<br/>
为关键任务保留输入来源、运行过程、工具调用、审查结果、负责人和继续入口，支持复查、审计和接力。

**OPL Health Deployment**<br/>
支持院内私有化、专有云和混合部署，适配医院的信息化、安全、权限、数据和计算资源边界。

## 与 OPL Cloud 的关系

OPL Health Platform 是建立在 OPL Cloud 之上的医疗行业产品层。

```text
OPL Health Platform
├─ 医学知识包
├─ 临床规则包
├─ 医疗工具包
├─ 专病模板
├─ 医疗审查机制
└─ 医院部署方案

Powered by OPL Cloud
├─ OPL Gateway    模型接入、密钥、路由、用量
├─ OPL Workspace  在线工作空间和任务会话
├─ OPL Console    用户、权限、资源、账单、审计
├─ OPL Fabric     计算、存储、环境、连接器、智能体注册
└─ OPL Ledger     任务回执、产物来源、审查记录、继续引用
```

OPL Cloud 负责通用能力。OPL Health Platform 负责医疗行业能力和医院产品体验。

## 初步文档

- [产品定位](docs/product-positioning.md)
- [目标运营模型](docs/target-operating-model.md)
- [架构总览](docs/architecture.md)
- [OPL Cloud 通用能力使用方式](docs/opl-cloud-capability-usage.md)
- [场景地图](docs/scenario-map.md)
- [专病科研助手](docs/scenarios/specialty-research-assistant.md)
- [专病质控助手](docs/scenarios/specialty-quality-assistant.md)
- [随访管理助手](docs/scenarios/follow-up-assistant.md)
- [医疗能力包](docs/medical-capability-packs.md)
- [OPL Health Knowledge](docs/opl-health-knowledge.md)
- [OPL Health Protocol](docs/opl-health-protocol.md)
- [OPL Health Tools](docs/opl-health-tools.md)
- [OPL Health Agents](docs/opl-health-agents.md)
- [OPL Health Review](docs/opl-health-review.md)
- [OPL Health Deployment](docs/opl-health-deployment.md)
- [专病模板体系](docs/specialty-template-system.md)
- [医疗智能体生命周期](docs/medical-agent-lifecycle.md)
- [医院部署模式](docs/hospital-deployment-models.md)
- [合规与责任边界](docs/compliance-and-responsibility.md)
- [路线图](docs/roadmap.md)

## 当前状态

本仓库当前承载产品规划、架构边界和医疗行业能力设计。服务代码、运行环境、账单系统、资源调度、模型接入和证据存储由对应实现面承载。

第一阶段目标是把医疗元智能体平台的品牌、边界、能力包、部署路径和与 OPL Cloud 的关系定义清楚，为后续试点和实现提供统一入口。
