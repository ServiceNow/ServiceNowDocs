---
title: Use the Analyze alert impact agentic workflow
description: Learn how to use the Analyze alert impact agentic workflow in the Now Assist panel. The agentic workflow helps you investigate an alert and get the context that you need to respond efficiently.
locale: en-US
release: xanadu
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Analyze alert impact agentic workflow, Using agentic workflows in Now Assist for IT Operations Management \(ITOM\), Now Assist for IT Operations Management \(ITOM\), IT Operations Management]
---

# Use the Analyze alert impact agentic workflow

Learn how to use the Analyze alert impact agentic workflow in the Now Assist panel. The agentic workflow helps you investigate an alert and get the context that you need to respond efficiently.

## Before you begin

Before using the Analyze alert impact agentic workflow, you must have Now Assist for IT Operations Management \(ITOM\) installed on your instance. For more information about installing Now Assist plugins, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

You must also do the following:

-   Turn on the Analyze alert impact agentic workflow in the Now Assist panel. See [Analyze alert impact agentic workflow](../concept/now-assist-itom-agentic-aia.md) for more information.
-   Configure and activate AI agents for the observability tools that you have integrated with Event Management, such as Dynatrace, Kentik, or New Relic. For more information, see [Configuring AI agents for Now Assist for ITOM](../concept/itom-ai-agent-configuration.md).

**Note:** The following procedure shows how to use the Now Assist panel for the Analyze alert impact agentic workflow. For general guidance on using the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon: ![Express list icon](../../event-management/image/express-list1.png).

3.  Select an alert.

4.  Open the panel by selecting the Now Assist icon \(![Now Assist icon.](../image/wwna-icon.png)\).

5.  Ask Now Assist a question about the alert.

<table id="choicetable_hl1_xpf_3gc"><thead><tr><th align="left" id="d184838e187">

Option

</th><th align="left" id="d184838e190">

Description

</th></tr></thead><tbody><tr><td id="d184838e196">

**Ask about impact**

</td><td>

Get a summary of affected services and users. Include the word `impact` in your question. For example, `What is the impact of this alert?` or `What is the impact level of this alert?`.If the alert source is an observability tool, such as Kentik, Now Assist also includes relevant information from that tool in the response.

</td></tr><tr><td id="d184838e222">

**Ask a tool-specific question**

</td><td>

Get detailed insights about the alert from the relevant observability tool. For example, for New Relic alerts, you can ask `Have there been recent deployments for this alert?`.See [Questions for the Analyze alert impact agentic workflow](../reference/questions-now-assist-workflows.md) for the list of available questions.

</td></tr></tbody>
</table>    Now Assist uses the relevant AI agents to analyze your question and respond with a summary or insight. The first response for an alert might take several seconds to appear.


## What to do next

Use the information that you received to understand the alert impact and respond accordingly. You can also ask more questions about the alert.

**Note:** Your conversation in the Now Assist panel is specific to the alert that you selected in Step 2. To ask about a different alert, open that alert and select the Now Assist icon \(![Now Assist icon.](../image/wwna-icon.png)\) to start a new conversation.

**Parent Topic:**[Analyze alert impact agentic workflow](../concept/now-assist-itom-agentic-aia.md)

