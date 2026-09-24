---
title: Evaluation projects
description: Process Mining offers four evaluation projects to help you understand the product functionality with your own data. The Process Mining plugin \(sn\_po\) is activated by default in all your production instances enabling you to use the evaluation projects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/evaluate-pm.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Explore, Process Mining, Platform Analytics]
---

# Evaluation projects

Process Mining offers four evaluation projects to help you understand the product functionality with your own data. The Process Mining plugin \(sn\_po\) is activated by default in all your production instances enabling you to use the evaluation projects.

## What are evaluation projects

To evaluate Process Mining, a new project type is introduced. You don't need a license to use them, and using one doesn't count against any entitlement or quota.

## How evaluation projects are mined

-   Incident Management and CSM evaluation projects are pre-mined automatically once a month on production instances. Therefore, the results are ready to explore as soon as you open them. You don't need to wait for a mining run to finish.
-   HR and Security Incident evaluation projects mine on demand, scoped to your own data access, since these tables often contain sensitive information.

## Finding evaluation projects

If you're in the Process Mining Workspace and don't yet have any full projects set up, you're guided directly to the available evaluation projects instead of landing on an empty screen. You can also discover and open evaluation projects directly from the Platform Analytics workspace, and from a KPI details page, without switching workspaces first.

## Customizing evaluation projects

Process Mining admins and power users can customize evaluation projects within guardrails that keep them consistent:

-   The 7-day, 3,600-record scope always applies, regardless of customization
-   Admins can add filter conditions to exclude unwanted information \(such as auto-closed or test records\) from an evaluation project's scope

## Turning evaluation projects off

If you don't want any evaluation projects automatically on your instance, an instance-level setting lets you opt out entirely.

The `promin.feature.enable_evaluation` system property helps you enable or disable the evaluation projects. For more information, see [Process Mining properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/components-installed.md).

-   **[Process Mining evaluation project for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/evaluation-pm-inci-manag.md)**  
Process Mining evaluation project for Incident Management enables you to familiarize with improving your process with Process Mining capability.
-   **[Process Mining evaluation project for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/evaluation-pm-csm.md)**  
Process Mining evaluation project for Customer Service Management \(CSM\) enables you to familiarize with improving your process with Process Mining capability.
-   **[Process Mining evaluation project for Human Resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/evaluation-pm-hr.md)**  
Process Mining evaluation project for Human Resources \(HR\) enables you to familiarize with improving your process with Process Mining capability.
-   **[Process Mining evaluation project for Security Incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/evaluation-security.md)**  
Process Mining evaluation project for Security Incident enables you to familiarize with improving your process with Process Mining capability.
-   **[Run the Process Mining evaluation project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/run-evaluation-project.md)**  
Run the Process Mining evaluation project to familiarize with improving your process with Process Mining capability.

**Parent Topic:**[Exploring Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/explore-process-mining.md)

**Related topics**  


[Process Mining architecture]()

[Key features of Process Mining]()

[Process Mining workspace]()

