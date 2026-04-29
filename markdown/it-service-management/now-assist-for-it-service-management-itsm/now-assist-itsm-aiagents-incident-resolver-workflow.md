---
title: IT Service Management AI agent collection Investigate and resolve ITSM incidents agentic workflow
description: Use the Investigate and resolve ITSM incidents AI agent team to get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [ITSM, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Investigate and resolve ITSM incidents agentic workflow

Use the Investigate and resolve ITSM incidents AI agent team to get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.

## Investigate and resolve ITSM incidents agentic workflow overview

Using the Investigate and resolve ITSM incidents agentic workflow:

1.  Check for related catalog items and select the most relevant item.
2.  Check for Knowledge articles and similar incidents.
3.  Get recommended steps for incident resolution.

To modify the Investigate and resolve ITSM incidents agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Important:** When you modify an agentic workflow, AI agent, or a tool, make sure that you update all instructions accordingly.

## Link catalog items and Knowledge articles to incidents

When you make a query or a request in the Now Assist panel, you can get recommendations for relevant catalog items. The recommendations get automatically added to the incident's **Additional comments** section. The workflow uses relevant Knowledge articles and similar incidents to get the recommended steps for incident resolution that gets added to the incident's **Work notes** section.

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

ITSM incident resolution plan investigation AI agent

</td><td>

1.  Recommends catalog items related to the selected incident.
2.  Looks up similar incidents and provides an incident resolution. The resolution can also include information from knowledge articles.

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


![Investigate and resolve ITSM incidents agentic workflow output.](../image/now-assist-itsm-aiagents-inv-resolve-inc.png)

In the AI Agent Studio, the human agent gets notified as soon as the recommendations to resolve incidents get generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

## Generating the incident resolution steps in the Now Assist panel

As a user, do the following in the Now Assist panel:

1.  Open the Now Assist panel and enter the incident number for which you want to generate the incident resolution steps.

    The Investigate and Resolve ITSM incidents workflow gets triggered and the ITSM Incident Resolution Plan Investigation AI agent takes over the issue resolution.

2.  Using AI search, the AI agent retrieves the top 10 most relevant catalog items related to the incident.

    The URLs to these catalog items are added to the **Additional Comments** section in the incident.![Now Assist for ITSM Investigate and Resolve ITSM incidents workflow catalog comments](../image/now-assist-itsm-inv-resol-nap-cat-comment.png)

3.  The AI agent gathers all relevant information required for the investigation.

    The retrieved data includes similar resolved incidents, relevant knowledge base articles, and other contextual information. The AI agent generates a resolution plan based on this information.

4.  The resolution plan is added to the incident's work notes.

    If the AI agent was unable to create a resolution plan, then it displays a message indicating the failure.

    ![Now Assist for ITSM Investigate and Resolve ITSM incidents workflow plan comments](../image/now-assist-itsm-inv-resol-nap-plan-comment.png)


