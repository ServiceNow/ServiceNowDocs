---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection analyze risks and recommend solutions agentic workflow
description: Use the Analyze risk and recommend solutions agentic workflow to monitor and mitigate risks in customer engagements with minimal user intervention.
locale: en-US
release: xanadu
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2025-04-23"
reading_time_minutes: 1
breadcrumb: [Customer success agentic workflows, Using agentic workflows in Now Assist for Telecommunications, Media and Technology \(TMT\), Now Assist for Telecommunications, Media and Technology \(TMT\), Telecommunications, Media, and Technology]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection analyze risks and recommend solutions agentic workflow

Use the Analyze risk and recommend solutions agentic workflow to monitor and mitigate risks in customer engagements with minimal user intervention.

## Analyze risks and recommend solutions agentic workflow overview

Use the Analyze risks and recommend solutions agentic workflow to:

-   Monitor engagements and retrieve all applicable risks.
-   Provide real-time risk analysis and generate detailed reports.
-   Identify common solutions and provide proactive recommendations.

Customer success managers can collaborate with customer success squad members to monitor risks, perform real-time risk analysis, generate detailed reports with proactive recommendations. This helps prevent escalations, improve customer retention, and enhance service quality. The Analyze risks and recommend solutions agentic workflow can be used to assess and offer solutions for both individual and multiple risks. It is triggered daily based on a predefined schedule and the results are displayed in the [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Configure the Analyze risks and recommend solutions agentic workflow

Before you use the agentic workflow, do the following:

-   Activate the Analyze risks and recommend solutions subflow to trigger the agentic workflow to run as a daily scheduled job. See [Activate a flow](https://www.servicenow.com/docs/access?context=flow-activate&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) for details.
-   Configure the risk category and other conditions as required in the Engagement risk solutions decision table. See [Using decision tables](https://www.servicenow.com/docs/access?context=using-decision-builder&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Ensure that the solution subflows contain the following mandatory inputs:
    -   Risk system ID: Type is string and default name is risk\_system\_id.
    -   Solution table: Type is table.
    -   Solution ID: Type is sys\_id.

Optionally, you can define additional non-mandatory inputs. These can be used in subflow steps or to override default values.

**Note:** To enable the display of the Analyze risk and recommend solutions agentic workflow, you must activate the AI Agents for Customer Success Management plugin \(com.sn\_cust\_succ\_ai\_agent\).

## AI agents used in the Analyze risks and recommend solutions agentic workflow

The Analyze risks and recommend solutions agentic workflow uses specific AI agents to retrieve all unaddressed risks and recommend solutions.

|AI agent|AI agent role|
|--------|-------------|
|Success risk manager AI agent|Retrieves unaddressed risks for the current user, groups them, and provides solutions for each risk or group of risks.|

