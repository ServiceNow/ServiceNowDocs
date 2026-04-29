---
title: Using agentic workflows in IRM
description: Use the Integrated Risk Management AI agent collection to help complete tasks autonomously.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Use agentic AI, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Using agentic workflows in IRM

Use the Integrated Risk Management AI agent collection to help complete tasks autonomously.

<table id="table_ug2_22t_z2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Optimize GRC issue resolution

</td><td>

Enables issue managers to auto-generate action plans and remediation tasks for faster issue resolution.

</td><td>

-   Issue action plan AI agent
-   Remediation tasks AI agent

</td></tr><tr><td>

Get regulatory insights

</td><td>

Assists regulatory change management professionals by analyzing regulatory alerts, enriches context using web search, and recommends potential impacts to citations, policies, control objectives, and more.

</td><td>

-   Regulatory alert recommendation agent
-   Regulatory alert enrichment agent

</td></tr><tr><td>

Generate regulatory action plans

</td><td>

Supports regulatory change management professionals in implementing change and action tasks by analyzing impacted areas and referencing similar past alerts.

</td><td>

Regulatory change task planning agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-ai-agents/task/clone-aia-usecase.html), and then proceed with the following steps:

-   Activate the workflow.
-   Activate all agents within the workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn't necessary.

There may be AI agents installed with the Now Assist application that aren’t used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

