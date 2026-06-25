---
title: Scenario analysis using simulation
description: Scenario analysis using simulation is a guided, playbook-driven workflow in the Operational Resilience Workspace. It uses statistical modelling to quantify how critical services perform under adverse-event scenarios. The analysis takes you from scoping a service through to a treatment decision and, optionally, logging operational vulnerabilities and issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/scenario-analysis-in-ws.html
release: australia
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 2
keywords: [Scenario Analysis, Operational Resilience, Playbook, Statistical Model Profile]
breadcrumb: [Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Scenario analysis using simulation

Scenario analysis using simulation is a guided, playbook-driven workflow in the Operational Resilience Workspace. It uses statistical modelling to quantify how critical services perform under adverse-event scenarios. The analysis takes you from scoping a service through to a treatment decision and, optionally, logging operational vulnerabilities and issues.

## Advanced scenario analysis using simulation

Advanced scenario analysis assesses how a critical service performs under adverse conditions using statistical simulation, replacing the legacy free-form and SME-driven flow with an Annual Loss Model that produces quantified financial-risk estimates. Each analysis is scoped to a single service, its dependencies, and one or more scenarios. For the objectives and benefits of running an advanced scenario analysis, see [Scenario analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-ov.md).

## How the analysis progresses

You run an advanced scenario analysis through the **Playbook** tab on a scenario analysis record. The playbook provides a stage panel and an activity stream in the user interface \(UI\); as you complete each step, the playbook locks the selection and advances to the next stage.

The stages progress in a sequence — Scope \(service and dependencies\), Scenarios, Reference Data, Scenario Testing, Results, Treatment Decision, and the optional Operational Vulnerabilities and Issues.

For full details about the playbook interface, the statistical model profile, and the simulation results, see [Building a scenario analysis using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-playbook-experience.md).

## Role-based access

The following roles are required to manage scenario analysis in Operational Resilience.

|Role|Description|
|----|-----------|
|Operational Resilience Manager \(sn\_oper\_res.manager\)|Role that can create, edit, and progress all playbook stages; can mark stages complete; can select **Complete analysis**.|
|Operational Resilience User \(sn\_oper\_res.user\)|Role that can view scenario analysis records and all playbook stages in read-only mode. Cannot create records, add data to any stage, mark stages complete, or delete records.|

**Related topics**  


[Building a scenario analysis using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-playbook-experience.md)

