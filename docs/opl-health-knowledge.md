# OPL Health Knowledge

Owner: `opl-health-platform`
Purpose: `medical_knowledge_requirements_ssot`
State: `active_planning`
Machine boundary: 本文定义医学知识的来源、版本、适用范围和维护要求，不证明知识库已构建、已更新、可检索或通过医学审查。

OPL Health Knowledge 是 OPL Health Platform 的医学知识能力层。

它把指南、共识、教材、文献、医院制度、科室资料和项目材料整理成可引用、可更新、可审查的医学知识包，为医疗智能体提供专业语境和证据基础。

## 核心内容

- 临床指南和专家共识。
- 教材、综述和高质量文献。
- 医院制度、科室规范和操作流程。
- 科研项目资料、研究方案和历史报告。
- 专病知识结构、术语表和关键指标定义。

## 知识包记录

每个医学知识包应记录：

- 名称和适用科室。
- 来源和引用方式。
- 版本和更新时间。
- 适用范围。
- 维护负责人。
- 审查记录。

## 使用方式

OPL Health Knowledge 服务于三类场景：

| 场景 | 用法 |
| --- | --- |
| 专病智能体 | 提供疾病背景、诊疗路径、指标定义和输出依据 |
| 科研任务 | 提供文献证据、研究方案、变量口径和报告素材 |
| 质控与管理 | 提供制度、指标、流程和审查标准 |

## 与 OPL Cloud 的关系

Health 的知识需求复用 Framework 的[知识来源与记忆政策](https://github.com/gaofeng21cn/one-person-lab/blob/main/docs/policies/knowledge-source-and-memory-policy.md)和[知识来源接口](https://github.com/gaofeng21cn/one-person-lab/blob/main/docs/specs/knowledge-sources.md)。Framework 持有来源绑定、范围与版本校验、冻结上下文、消费回执及条件写回；Health 与医院指定负责人持有医学内容、审查和适用性判断。

| 资料类型 | 正文与维护责任 | Health 的消费方式 |
| --- | --- | --- |
| 产品方法与通用医学材料 | 对应能力包及医学内容负责人 | 引用包内知识 catalog 和已审阅版本 |
| 个人、团队、主题或项目知识 | 用户或机构批准的原库与维护者 | 通过获授权的来源登记与工作区绑定按需读取；已有 Obsidian 或 Markdown 目录可继续持有唯一可编辑正文 |
| 患者记录、医院数据库和原生业务资料 | 医院系统或其原生 provider | 由[医疗工具](opl-health-tools.md)取得获准的业务对象与来源引用；不因接入知识需求而迁入个人库 |

试点为每项知识需求写明用途、语义负责人、scope、必要性、有效期和写回负责人，再由获授权的控制面绑定实际来源。当前 Framework 的本地来源接口面向 Markdown；数据库与其他原生存储按各自公开接口消费，不能把文件挂载或一份摘要当作已具备相同知识授权与版本语义。缺少适配时在试点方案中记录所缺入口及 owner。

Agent 使用知识时保留本次接受版本与来源引用；必要来源失效或撤权时先处理缺口。正文修订通过原处编辑复核或提案、审阅、条件写回进入原源，临床知识的语义接受仍由医学负责人作出。消费回执和运行快照不是新的可编辑知识主库。

OPL Fabric 可提供获准的文件、数据库和机构资料接入，OPL Workspace 组合这些资源与知识消费能力。跨执行环境须明确来源访问、数据处理面和委派范围，不自动继承本机来源授权。需要长期保留的任务回执和来源引用可以进入 OPL Ledger；本仓只定义上述试点要求，实际接口支持和接入结果由对应 owner 验证。
