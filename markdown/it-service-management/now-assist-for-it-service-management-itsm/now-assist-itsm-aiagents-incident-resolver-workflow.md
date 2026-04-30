---
title: IT Service Management AI agent collection Investigate and resolve ITSM incidents agentic workflow
description: Use the Investigate and resolve ITSM incidents AI agent team to get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.
locale: en-US
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-03-28"
reading_time_minutes: 3
keywords: [Now Assist, Agentic AI]
breadcrumb: [Use agentic workflows in ITSM, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Investigate and resolve ITSM incidents agentic workflow

Use the Investigate and resolve ITSM incidents AI agent team to get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.

## Investigate and resolve ITSM incidents agentic workflow overview

Using the Investigate and resolve ITSM incidents agentic workflow:

1.  Check for related catalog items and select the most relevant item.
2.  Check for Knowledge articles and similar incidents.
3.  Get recommended steps for incident resolution.

To modify the Investigate and resolve ITSM incidents agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Important:** When you modify an agentic workflow, AI agent, or a tool, make sure that you update all instructions accordingly.

## Link catalog items and Knowledge articles to incidents

When you make a query or a request in the Now Assist panel, you can get recommendations for relevant catalog items. After you select a catalog item, the workflow uses relevant Knowledge articles and similar incidents to get recommended steps for incident resolution.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Investigate and resolve ITSM incidents**.

## Setting manual triggers for the agentic workflow

The Investigate and resolve ITSM incidents agentic workflow is triggered manually based on the following conditions:

**Note:** In the **Define trigger** screen, the value in the **Run as** field must be set to **Assigned to**.

-   **State** is updated to **In progress**
-   **Assigned to** isn’t empty

## AI agents used in the Investigate and resolve ITSM incidents agentic workflow

In the Investigate and resolve ITSM incidents agentic workflow, use specific AI agents for each type of resolution to generate the desired recommendations.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

<table id="table_abj_5lk_j2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Find catalog item AI agent

</td><td>

Recommends catalog items related to the selected incident.

</td></tr><tr><td>

ITSM incident resolution investigation AI Agent

</td><td>

1.  Looks up similar incidents and provides an incident resolution.
2.  Looks for Knowledge articles and adds relevant Knowledge articles to the incident.

</td></tr></tbody>
</table>## Generating a recommendation using the Investigate and resolve ITSM incidents agentic workflow

In the agentic workflow record:

1.  Review the information in the Describe and connect screen and in the Define trigger screen, make any necessary updates, and then select **Save and Continue**.
2.  In the Select display screen:

    1.  Choose where you want the agentic workflow output to be displayed.
    2.  Use the arrow next to it to add roles that can access the agentic workflow.

        **Note:** The itil role is added by default.

    3.  Select **Save and test**.

        The agent executes the request for the agentic workflow.

    **Example of Investigate and resolve ITSM incidents agentic workflow output in the ServiceNow AI Agent Studio**


![Investigate and resolve ITSM incidents agentic workflow output.](../image/now-assist-itsm-aiagents-incident-resolution-workflow.png)

In the AI Agent Studio, the human agent gets notified as soon as the recommendations to resolve incidents get generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

**Parent Topic:**[Using agentic workflows in Now Assist for ITSM](now-assist-itsm-ai-agents-use-cases.md)

