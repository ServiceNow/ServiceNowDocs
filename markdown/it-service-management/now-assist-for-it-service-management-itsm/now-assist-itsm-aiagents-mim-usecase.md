---
title: IT Service Management AI agent collection Generate post incident reviews agentic workflow
description: Use the Post-incident review AI agent to generate a review report after a major incident is closed. You can review and revise this report if necessary.
locale: en-US
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 3
keywords: [Now Assist, Agentic AI]
breadcrumb: [Use agentic workflows in ITSM, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Generate post incident reviews agentic workflow

Use the Post-incident review AI agent to generate a review report after a major incident is closed. You can review and revise this report if necessary.

## Generate post incident reviews agentic workflow overview

Using the Generate post incident reviews agentic workflow, generate reports after an incident is closed. The report includes the following sections:

-   Executive Summary
-   Customer/Service Impact
-   Detailed Technical Summary
-   Action Items &amp; Prevention

The time taken to resolve incidents may be reduced, and the business impact may be minimized when responses to major incidents are both effective and efficient. For information on how major incidents are created, see [Major Incident Management process](../../incident-management/concept/major-incident-management-process.md).

To modify the Generate post incident reviews agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Important:** When you modify a use case, AI agent, or tool, make sure that you update all instructions accordingly.

## Generate post incident reviews agentic workflow

Autonomously generate a report for the fulfiller once a major incident has been closed.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Post-incident reporting**.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

**Important:** To enable the display of the Generate post incident reviews agentic workflow, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](../../incident-management/task/activate-major-incident-management-plugin.md).

## AI agents used in the Generate post incident reviews agentic workflow

The Post-incident review AI agent is used to fetch incident details, related records, and the post incident summary.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

## Generating the report

In the agentic workflow record:

1.  Review the information in the Describe and connect screen and in the Define trigger screen, make the necessary updates, and then select **Save and Continue**.
2.  In the Select display screen:

    1.  Choose where you want the agentic workflow output to be displayed.
    2.  Use the arrow next to it to add roles that can access the agentic workflow.

        **Note:** The itil role is added by default.

    3.  Select **Save and test**.

        The agent executes the request for the agentic workflow.

    **Example of a Generate post incident reviews agentic workflow report in the ServiceNow AI Agent Studio** ![Generate post incident reviews agentic workflow output.](../image/now-assist-itsm-aiagents-mim-nap.png)


In the AI Agent Studio, the fulfiller receives a notification as soon as the report is generated, enabling them to follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

**Parent Topic:**[Using agentic workflows in Now Assist for ITSM](now-assist-itsm-ai-agents-use-cases.md)

