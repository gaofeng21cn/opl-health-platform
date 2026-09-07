<p align="center">
  <img src="assets/branding/opl-health-platform-logo.png" alt="OPL Health Platform logo" width="132" />
</p>

<p align="center">
  <a href="./README.md"><strong>English</strong></a> | <a href="./README.zh-CN.md">中文</a>
</p>

<h1 align="center">OPL Health Platform</h1>

<p align="center"><strong>A medical meta-agent platform for hospitals</strong></p>
<p align="center">Medical knowledge · clinical rules · medical tools · specialty agents · review and delivery</p>

<!--
Owner: `opl-health-platform`
Purpose: `public_health_platform_entry`
State: `planning_public_entry`
Machine boundary: Human-readable product and planning entry. Machine truth for generic cloud capabilities, workspace runtime, console, resource scheduling, model access, evidence records, and operational status remains with OPL Cloud, owning implementation repositories, services, contracts, runtime outputs, and owner receipts.
-->

## Why OPL Health Platform

Hospitals need AI systems that go beyond one-off answers or a single chatbot.
They need medical agent systems that can work across real clinical, research,
quality, and operational workflows.

Those systems must handle medical knowledge, clinical rules, hospital data,
specialty workflows, tool use, review records, and deliverable outputs:

- Clinicians need agents that understand specialty context, clinical rules, and
  patient-data boundaries.
- Departments need reusable disease workflows, research processes, and quality
  requirements.
- Hospitals need private, dedicated, or hybrid deployment options that fit local
  data and compute boundaries.
- Management teams need permissions, audit records, usage, risk control, and
  traceable output provenance.
- AI teams need one governed way to develop, test, publish, and operate medical
  agents.

**OPL Health Platform is planned as that medical meta-agent platform for hospitals.**

It uses OPL Cloud as the established technical substrate and extends its general
AI infrastructure into a healthcare product layer:
medical knowledge packs, clinical rule packs, medical tool packs, specialty
templates, medical reviewer gates, and hospital deployment models on top of a
shared workspace, console, resource substrate, and evidence record.

## Product Positioning

OPL Health Platform is the healthcare product-line entry for OPL.

| Layer | Name | Role |
| --- | --- | --- |
| Healthcare brand line | **OPL Health** | OPL product family for medical institutions |
| Hospital platform | **OPL Health Platform** | Medical meta-agent platform for hospitals |
| Agent building | **OPL Health Studio** | Development and configuration of medical agents, specialty workflows, knowledge packs, and rule packs |
| Medical integration | **OPL Health Connect** | HIS, EMR, LIS, PACS, literature, database, and hospital tool connections |
| Scenario products | **OPL Health Apps** | Specialty agents, research assistants, quality assistants, follow-up assistants, management assistants |
| Technical substrate | **Powered by OPL Cloud** | Workspace, console, resources, model access, metering, and evidence capabilities |

The first phase starts from one real specialty scenario and validates the
medical capability packs, human review boundary, and hospital deployment path.
Studio, Connect, and Apps can become separate product surfaces as real hospital
needs mature.

OPL Cloud is the selected technical substrate. Its current operational state
must be verified in the Cloud and deployment-instance repositories. This repository owns healthcare product
requirements, capability packs, review policy, and deployment models. It does
not duplicate the generic runtime, resource scheduler, billing, model-access,
evidence-storage, or release mechanisms. Medical judgment and clinical
responsibility remain with the hospital and its designated professionals.

## Current Build Boundary

This repository currently contains product and architecture documentation. Its
next step is one specialty MVP pilot that defines the scenario, minimum
knowledge and rules, required tools, human review points, responsibility
boundaries, and the OPL Cloud, OPL App, and OPL Framework capabilities it uses.

The healthcare platform has not entered service implementation or hospital
deployment. This phase does not add a second cloud service, billing system,
resource scheduler, or evidence system, and it does not present design
documents as released, deployed, or medically accepted product capability.

<p align="center">
  <img src="assets/branding/opl-health-platform-overview-v2.png" alt="OPL Health Platform specialty MVP product vision" width="100%" />
</p>

## Core Capabilities

**OPL Health Agents**<br/>
Governed medical agents for specialty disease workflows, research, quality
control, follow-up, record organization, guideline matching, evidence review,
and operational processes.

**OPL Health Knowledge**<br/>
Guidelines, consensus documents, textbooks, literature, hospital policies,
department material, and project material with source, version, scope, and
update records.

**OPL Health Protocol**<br/>
Reusable clinical pathways, quality indicators, inclusion and exclusion
criteria, risk stratification rules, follow-up rules, and review requirements.

**OPL Health Tools**<br/>
Hospital systems, databases, literature sources, statistical analysis, charting,
report generation, and research tools.

**Specialty templates**<br/>
Task templates, data requirements, review standards, result formats, and
delivery paths for high-value specialty scenarios.

**OPL Health Review**<br/>
Input provenance, execution traces, tool calls, reviewer results, owners, and
continuation entries for important tasks.

**OPL Health Deployment**<br/>
Private, dedicated, and hybrid deployment paths aligned with hospital security,
permissions, data, and compute boundaries.

## Relationship With OPL Cloud

OPL Health Platform is not a second cloud platform. It is the healthcare product
layer built on OPL Cloud.

```text
OPL Health Platform
├─ Medical knowledge packs
├─ Clinical rule packs
├─ Medical tool packs
├─ Specialty templates
├─ Medical reviewer gates
└─ Hospital deployment models

Powered by OPL Cloud
├─ OPL Gateway    model access, keys, routing, usage
├─ OPL Workspace  online workspaces and task sessions
├─ OPL Console    accounts, workspaces, quotas, administration
├─ OPL Fabric     compute, storage, environments, connectors
└─ OPL Ledger     receipts, reconciliation evidence, provenance refs
```

OPL Cloud provides the generic substrate. OPL Health Platform provides the
medical industry layer, medical review policy, and hospital product experience.
Ledger can retain caller-provided receipts and provenance references, but it
does not own medical conclusions, review decisions, or continuation authority.

## Documentation

- [Documentation Index](docs/README.md)
- [Current Roadmap And Gaps](docs/roadmap.md)
- [Product Positioning](docs/product-positioning.md)
- [Scenario Map](docs/scenario-map.md)

Current pilot selection, remaining gaps, and implementation entry conditions
are maintained only in [Roadmap](docs/roadmap.md).
