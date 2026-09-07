# OPL Cloud 通用能力使用方式

Owner: `opl-health-platform`
Purpose: `cloud_capability_consumption_boundary`
State: `active_planning`
Machine boundary: 本文只描述 Health 对 OPL Cloud、App 与 Framework 的产品需求和使用边界，不复制其机器合同、运行状态、账单、调度或负责人回执。

OPL Health Platform 建立在 OPL Cloud 的通用能力之上。

这份文档归 OPL Health Platform 所有，用来说明医疗产品如何使用 Cloud 能力。OPL Cloud 保持通用工作空间、管理、模型接入、资源和证据边界；医疗产品在这些边界之上增加医院角色、医学内容、审查规则和场景体验。

本仓只记录医疗产品对这些能力的需求和引用关系。Workspace、Console、Gateway、Fabric、Ledger 和 OPL Packages 的运行状态、调度、账单、模型路由、证据存储和负责人回执仍由各自实现面负责。只有真实试点形成稳定、重复的结构后，才考虑抽取机器可读合同。

## 已确定的 Cloud 基线

- 医疗平台确定建立在 OPL Cloud 之上，不再另选或自建一套通用云底座。
- Console 负责界面，Control Plane 负责账户、策略和工作空间编排；医疗层通过产品接口接入，不直接访问 Fabric、Ledger 或其数据库。
- OPL Gateway 是稳定的模型接入抽象；医疗层只依赖其公开能力，不绑定当前具体实现。
- Fabric 负责计算、存储、环境、连接器和资源状态，具体部署由明确选择的 Provider 配置决定。
- Ledger 负责回执、对账证据和来源引用，不负责医学审查结论、继续授权或医疗质量判断。
- 医院组织、多角色协作、医疗系统接入和医学审查流程是 Health 试点需要验证的需求；
  对应 Cloud 版本和实例能力从其公开接口及运行结果核验，不在本仓保存可用性结论。

## 能力映射

| Health 需求 | 使用的 Cloud 通用能力 | Health 侧需要想清楚 |
| --- | --- | --- |
| 医生和研究者在线使用医疗智能体 | OPL Workspace | 医疗项目空间展示什么、用户如何进入、任务如何组织 |
| 医院管理用户、科室、审批和预算 | OPL Console / Control Plane | 医院角色、科室结构、审批对象、审查人和预算口径；这些医疗组织能力不能假定已经存在 |
| 医疗智能体调用前沿 AI | OPL Gateway | 医院可用模型、科室额度、任务用量和敏感任务策略 |
| 医疗资料、工具、计算和环境接入 | OPL Fabric | 医学知识、临床规则、工具包和院内资源如何映射到通用资源 |
| 医疗任务保留来源和交付证据 | OPL Ledger | 哪些回执和来源引用进入 Ledger；医学审查结果和继续权限由谁持有 |
| 医疗智能体从设计走向产品入口 | 能力包负责人发布的描述信息、原生载体、OPL Framework 和相应的 Cloud / App 产品面 | 医疗智能体如何绑定知识、规则、工具、审查和责任边界；Health 不接管能力包身份、发布、安装或更新状态 |

## 第一试点的使用方式

专病科研助手优先使用这些 Cloud 能力：

- OPL Workspace：提供科研项目的在线工作入口；医疗项目结构、资料组织和审查反馈是 Health 需要设计的扩展体验。
- OPL Gateway：提供模型接入和用量能力；医院、科室、项目与任务之间的归属规则由试点明确。
- OPL Fabric：接入文献、项目资料库、统计工具、图表工具和报告工具。
- OPL Ledger：保存需要长期保留的任务回执、对账证据和来源引用。
- OPL Console / Control Plane：提供现有账户和工作空间管理能力；科室成员、医疗角色、审批和预算规则属于试点需要验证的扩展需求。

## Health 侧需要继续明确的问题

### Workspace 使用方式

- 专病科研项目空间里展示哪些信息。
- 医生、研究者、审查人分别看到哪些入口。
- 任务、资料、产物、审查反馈如何组织。

### Console 治理方式

- 医院管理员、科室管理员、医生、研究者、审查专家、AI 运维的分工。
- 知识包、规则包、工具包、智能体版本和 Workspace 权限如何审批。
- 科室级试点如何看用量、额度和风险。

### Fabric 资源映射

- 第一试点需要哪些资料源、工具和存储。
- 哪些资源由医院提供，哪些资源由 OPL 托管。
- 医疗用户看到的是产品化选项，而不是底层基础设施。

### Ledger 与医学审查的衔接

- 哪些任务回执和来源引用需要进入 Ledger。
- 医学审查记录由哪个医疗业务负责人或系统持有。
- 审查记录如何引用 Ledger 回执，而不把医学决定交给通用证据服务。

### Gateway 用量方式

- 用量如何归属到医院、科室、Workspace、智能体和任务。
- 哪些模型策略适合医疗试点。
- 第一阶段需要哪些额度和预算控制。

### 医疗智能体部署方式

```text
OPL Meta Agent 支持医疗智能体语义设计
-> 绑定 Health Knowledge / Protocol / Tools / Review
-> 形成由对应负责人验证的医疗智能体能力包引用
-> 管理端审批
-> 对应 OPL Cloud / OPL App / OPL Framework 负责人提供产品或运行面
-> Workspace 使用
-> 医疗业务保存审查决定，Ledger 保存对应回执和来源引用
```

这些问题由 OPL Health Platform 继续规划；OPL Cloud 保持通用能力边界。
