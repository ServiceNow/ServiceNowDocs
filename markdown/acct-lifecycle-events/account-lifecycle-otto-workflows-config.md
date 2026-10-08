---
title: Configure agentic workflows for Customer Success Management
description: Duplicate and activate the Customer Success Management agentic workflows, and complete any additional setup a specific workflow requires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-otto-workflows-config.html
release: brazil
topic_type: concept
last_updated: "2026-09-22"
reading_time_minutes: 2
keywords: [configure agentic workflows, Customer Success Management]
breadcrumb: [Configure ServiceNow Otto for TMT, Configure, Customer Success Management]
---

# Configure agentic workflows for Customer Success Management

Duplicate and activate the Customer Success Management agentic workflows, and complete any additional setup a specific workflow requires.

Role required: admin

Agentic workflows included with the base system are read-only. Before you use one, duplicate it and activate it, along with any AI agents and triggers it depends on. See [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md) and [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-aia-use-case.md). This applies to every workflow below; the sections that follow list only what's *additionally* required for that specific workflow.

## Monitor engagement health

-   Activate the Monitor engagement health flow so the workflow runs on its scheduled job. See [Activate a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/flow-activate.md).
-   The workflow only monitors engagements with the **AI Health Monitor** flag enabled \(maximum 10 per customer success manager\). See [Create an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-create-engage.md).
-   By default, each individual health metric is monitored. To monitor only the overall health score instead, set the **sn\_cust\_succ\_ai\_agent\_enable\_health\_monitor\_metrics** system property to **false**.
-   For any health definition, specify the **Context** for the data source to control how color banding is applied. See [Set up the color banding table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-setup-color-banding.md).

## Recommend risk signal solutions

-   Configure the Engagement risk solutions decision table to map risk categories to Customer Success definitions. See [Using decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/using-decision-builder.md) and [Create a customer success definition record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-create-ale-defn.md).
-   The solution subflow must accept a **Risk system ID** input and return a **Generated record** output \(the table name and sys\_id of the solution record\). Additional inputs, such as a due date, can be added as needed.

## Support renewals and expansion

-   Activate the Renewal Insight Engine skill; it's inactive by default. See [Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-skill.md).
-   Configure the Renewal analysis AI agent's fields: engagement adoption source sysID, contract adoption source sysID, health source sysID, time period, and metric aggregation type.
-   Set the source and context tables for each sysID in the Data Context Engine. See [Configure the Data context engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-setup-dce.md).

## Draft and schedule touchpoint meetings

-   Activate the meeting proposal generator skill on the AI Skills page to trigger this workflow. See [Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-skill.md).
-   Configure the generic prompt in the OneExtend Capability table: set **Default** to **True** for your LLM provider's Generic Prompt definition.

## Squad resource identifier

-   Assign customer success roles to the squad members this workflow recommends; they aren't granted automatically. See [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AssignARoleToAUser.md).
-   In the workflow's Edit trigger form, turn on **Active** so the AI agent can trigger autonomously.

## Product release email communication

-   Install the AI Agents for Customer Success Management plugin. See [Plugins activated with Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-required-plugins.md).

    **Important:** Source topics disagree on this plugin's ID \(sn\_cust\_succ\_ai\_ag vs. com.sn\_cust\_succ\_ai\_agent\) — confirm before publishing.

-   Activate the product release content generator skill on the AI Skills page. See [Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-skill.md).

**Related topics**  


[ServiceNow Otto agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-otto-workflows.md)

[Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md)

