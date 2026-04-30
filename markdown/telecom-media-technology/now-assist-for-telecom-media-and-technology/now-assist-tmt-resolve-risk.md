---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) Recommend risk signal solutions agentic workflow
description: Use the Recommend risk signal solutions agentic workflow to monitor and mitigate risks in customer engagements with minimal user intervention.
locale: en-US
release: yokohama
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customer success agentic workflows, Use agentic workflows, Now Assist for Telecommunications, Media and Technology \(TMT\), Telecommunications, Media, and Technology]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) Recommend risk signal solutions agentic workflow

Use the Recommend risk signal solutions agentic workflow to monitor and mitigate risks in customer engagements with minimal user intervention.

## Recommend risk signal solutions agentic workflow overview

Use the Recommend risk signal solutions agentic workflow to:

-   Monitor engagements and retrieve all applicable risks.
-   Provide real-time risk analysis and generate detailed reports.
-   Identify common solutions and provide proactive recommendations.

Customer success managers can collaborate with customer success squad members to monitor risks, perform real-time risk analysis, generate detailed reports with proactive recommendations. This helps prevent escalations, improve customer retention, and enhance service quality. The Recommend risk signal solutions agentic workflow can be used to assess and offer solutions for both individual and multiple risks. It is triggered daily based on a predefined schedule and the results are displayed in the [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

For information on how risks are generated, see [Setup the engagement risk definition](https://www.servicenow.com/docs/access?context=account-lifecycle-setup-risk-defn&version=yokohama&pubname=yokohama-acct-lifecycle-events&ft:locale=en-US).

## Role masking

Required role: sn\_acct\_lc.customer\_success\_agent

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Configure the Recommend risk signal solutions agentic workflow

Before you use the agentic workflow, do the following:

-   Activate the Recommend risk signal solutions subflow to trigger the agentic workflow to run as a daily scheduled job. See [Activate a flow](https://www.servicenow.com/docs/access?context=flow-activate&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for details.
-   Configure the risk category and other conditions as required in the Engagement risk solutions decision table. See [Using decision tables](https://www.servicenow.com/docs/access?context=using-decision-builder&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).
-   Ensure that the solution subflows contain the following mandatory inputs:
    -   Risk system ID: Type is string and default name is risk\_system\_id.
    -   Solution table: Type is table.
    -   Solution ID: Type is sys\_id.

Optionally, you can define additional non-mandatory inputs. These can be used in subflow steps or to override default values.

**Note:** To enable the display of the Recommend risk signal solutions agentic workflow, you must activate the AI Agents for Customer Success Management plugin \(com.sn\_cust\_succ\_ai\_agent\).

## AI agents used in the Recommend risk signal solutions agentic workflow

The Recommend risk signal solutions agentic workflow uses specific AI agents to retrieve all unaddressed risks and recommend solutions.

|AI agent|AI agent role|
|--------|-------------|
|Success risk solution AI agent|Retrieves unaddressed risks for the current user, groups them, and provides solutions for each risk or group of risks.|

**Parent Topic:**[Customer success agentic workflows](now-assist-tmt-health-risk.md)

