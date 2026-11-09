# OPL Health Tools

Owner: `opl-health-platform`
Purpose: `medical_tool_requirements_ssot`
State: `active_planning`
Machine boundary: 本文定义医疗工具和数据源的产品需求，不证明连接器、权限、院内接口、工具执行或审计能力已经实现。

OPL Health Tools 是 OPL Health Platform 的医疗工具能力层。

它把院内系统、数据库、文献源、分析工具、报告工具和科室接口组织成可授权、可审计、可用于智能体任务的工具包。

## 核心内容

- HIS、EMR、LIS、PACS 等院内系统接入。
- 指南库、文献库和科研数据库。
- 结构化数据库、文件系统和对象存储。
- 统计分析、图表、文档、报告和幻灯片工具。
- 科室或医院内部接口。

## 工具包记录

每个医疗工具包应记录：

- 工具名称。
- 数据范围。
- 权限要求。
- 可执行动作。
- 输入输出格式。
- 调用记录要求。
- 负责人和审批记录。

## 工具分层

| 层级 | 示例 | 目标 |
| --- | --- | --- |
| 数据工具 | 数据库、文件、对象存储 | 提供受控数据访问 |
| 医学工具 | 指南库、文献库、术语库 | 提供专业资料来源 |
| 分析工具 | 统计、图表、报告生成 | 支持科研和质控交付 |
| 系统工具 | HIS、EMR、LIS、PACS | 对接院内业务系统 |

## 与 OPL Cloud 的关系

医疗 Agent 和 App 的外部服务连接复用 Framework 的 [OPL Connect 连接授权接口](https://github.com/gaofeng21cn/one-person-lab/blob/main/docs/specs/connection-authorization.md)，字段和调用边界以[连接授权合同](https://github.com/gaofeng21cn/one-person-lab/blob/main/contracts/opl-framework/connection-authorization-contract.json)为准。

| 层 | 负责人 | Health 侧的设计要求 |
| --- | --- | --- |
| 凭证与原生数据 | provider 或原生系统 owner | 保留原有凭证存储、OAuth 续期、账号切换和业务数据权威；向消费者提供受控调用入口 |
| 连接、授权与调用 | Framework Connect | 引用 provider/account 连接，声明所需 capability，由可信 Host 绑定实际已安装消费者并按 grant 调用 |
| 医疗操作与审查 | 医院及领域 owner | 定义数据范围、可执行动作、医生确认和业务回读；连接 grant 不替代临床操作批准 |

所需连接、capability、风险、结果引用和缺失 provider 必须在试点方案中具体列明。Agent 与按需打开的 UI 使用同一领域入口，不各存一份账户、grant 或凭证；页面和模型上下文只接收脱敏连接及结果。每次调用按公共合同复核安装身份、grant、连接 revision 和 capability；结果未知时先由原 provider 查询，不自动重复写入。模型账号沿用 Gateway 的 Account & Access，设备登录沿用设备 provider 的公开入口。

OPL Fabric 的连接器和执行适配器把获准资源带入工作空间；Console / Control Plane 提供账户与工作空间策略，Workspace 组合已获准能力。它们不从资源挂载推导知识读取权、Connect grant 或医疗动作批准，也不自动把本机连接授权转移到 Cloud；具体执行环境须由对应 owner 定义委派和调用路径。现有 provider 不支持的院内接口仍是待适配需求，由原 owner 与首个医疗消费者共同验证。

OPL Ledger 只保存必要的调用回执和来源引用；医院授权决定、医疗审查结论与业务结果仍由其 owner 持有。本页定义接入要求，不声明相关医院连接已经可用。
