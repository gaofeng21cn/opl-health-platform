# 路线图与当前差距

Owner: `opl-health-platform`
Purpose: `single_active_truth_plan`
State: `active_planning`
Machine boundary: 本文只维护 Health 人读规划的当前状态、剩余差距和下一轮工作。它不证明服务、部署、运行、发布、临床质量或 owner acceptance；这些事实归对应实现、运行输出和负责人回执。

## 目标态

OPL Health Platform 以医疗行业层消费 OPL Cloud、App、Framework 和领域能力，在一个真实专病场景中把医学知识、临床规则、医疗工具、医疗智能体、人工审查、责任边界和医院部署要求组织成可评审的 MVP 方案。

当前阶段仍是 `docs-only / MVP-first`。只有真实试点形成重复、稳定结构后，才评估是否需要机器合同或实现仓；本仓不提前持有运行时、服务、账单、资源调度、证据存储、发布 currentness 或临床决策 authority。

## 当前状态摘要

| 主题 | 当前状态 | 边界 |
| --- | --- | --- |
| 产品定位与目标运营模型 | `documented` | 已定义医院、科室、医生/研究者、信息化与 AI 团队角色；不是已上线产品证明 |
| Health / Cloud 分工 | `documented` | Health 定义医疗产品需求；Cloud / App / Framework 保留各自机器与运行真相 |
| 长期主题 owner | `consolidated` | Knowledge、Protocol、Tools、专病模板、Agents、Review、Deployment 各有一个人读 owner |
| 场景地图 | `documented` | 专病科研为第一试点建议；质控与随访用于边界压测 |
| 专病 MVP | `not_selected` | 尚未确定具体专病、科室 owner、资料边界和验收场景 |
| 实现与 Live Evidence | `out_of_scope_for_current_phase` | 文档、设计和链接检查不证明真实部署、运行或医疗质量 |

## 当前差距

1. 由医院或科室 owner 选定一个具体专病科研场景，明确用户、人群、任务和人工负责人。
2. 新增一份专病 MVP 试点文档，引用而不复制 Knowledge、Protocol、Tools、Review 与 Deployment owner。
3. 明确试点所需的最小资料、规则、工具、输入输出、人工确认点、交付物和退出条件。
4. 逐项映射需要消费的 OPL Cloud、App、Framework 与领域能力引用，不把需求写成已经实现或 ready。
5. 由医疗、信息化和产品 owner 审阅责任边界，再决定是否进入实现评估。

## 后续阶段

### 单场景试点

只完成一个专病 MVP 方案和 owner review；不同时扩张到多个专科、质控或患者触达场景。

### 医院级管理

仅在单场景试点证明重复需求后，再规划多智能体、多能力包、组织权限、资源和审查策略。

### 产品矩阵扩展

仅在真实场景成熟后，再评估 OPL Health Studio、OPL Health Connect 与 OPL Health Apps 是否需要独立产品面。

## 下一轮 Agent Prompt

### Write scope

- `docs/scenarios/<selected-specialty>-research-mvp.md`
- `docs/scenario-map.md`
- `docs/roadmap.md`
- 必要时仅更新被该试点直接引用的长期主题 owner

### Non-goals

- 不新增 contracts、schemas、service code、runtime、billing、resource scheduler 或 release/readiness claim。
- 不复制 OPL Cloud、App、Framework、MAS 或其他领域仓的机器合同和实现说明。
- 不把质控或随访场景一并扩成第二、第三条实施线。

### Live truth inputs

- 医院或科室 owner 提供的具体专病、用户、人群、资料范围、责任人和验收目标。
- 本仓 [文档索引](./README.md)、[场景地图](./scenario-map.md) 与各长期主题 owner。
- OPL Cloud、App、Framework 和领域仓当前公开边界及可消费引用；必须 fresh 读取，不从本仓旧描述推断。

### Verification commands

- 全仓 Markdown 相对链接扫描。
- 被替代主题、旧路径和重复标题扫描。
- `git diff --check`。

### Completion gate

- 只有一份专病 MVP 试点 owner 文档。
- 专病、用户、输入、输出、能力引用、人工确认、责任边界和验收条件完整。
- 未声明任何未被 owner evidence 支撑的实现、部署、运行、质量或 ready 状态。
- 所有当前差距回写本文件，文档索引无重复 owner。

### Foldback target

- 当前状态、剩余差距和后续提示词折回 `docs/roadmap.md`。
- 新增或移除入口只更新 `docs/README.md`；根 README 继续保持公开产品叙事。
