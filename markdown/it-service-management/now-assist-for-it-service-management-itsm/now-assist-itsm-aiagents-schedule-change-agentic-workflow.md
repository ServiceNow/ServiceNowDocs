---
title: IT Service Management AI agent collection schedule a change agentic workflow
description: Use the schedule a change agentic workflow to schedule change requests by identifying the available schedule slots.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Change Management, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection schedule a change agentic workflow

Use the schedule a change agentic workflow to schedule change requests by identifying the available schedule slots.

## Schedule a change agentic workflow overview

Use the schedule a change agentic workflow to schedule change requests in the slots available. If the planned start and end dates are provided, the workflow helps schedule the change request on or after the planned start date, at the earliest time slot available. The workflow helps align slots in the future dates by monitoring possible conflicts and upcoming blackout or maintenance schedules.

**Note:** The schedule a change agentic workflow doesn’t have a trigger and is invoked manually.

To modify the schedule a change agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Schedule a change request

Autonomously schedule change requests by identifying the available slots.

**Note:** The workflow can be accessed by the sn\_itsm\_aia.sn\_aia\_chg\_schedule role that is available as a part of the itil role.

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Schedule a change request**.

## AI agent used in the schedule a change agentic workflow

The Schedule Change Request AI agent can help you schedule a change request in the following scenarios:

-   If the duration provided is not sufficient for managing the change request, the agent suggests updating the schedule accordingly.
-   If there are scheduled CIs in the existing change, the agent suggests an alternate schedule within the next 90 days while also adhering to existing blackout and maintenance schedules.

## Schedule slots using the schedule a change agentic workflow

In the agentic workflow record:

1.  Review the information in the Describe and connect screen and in the Define trigger screen, make the necessary updates, and then select **Save and Continue**.
2.  In the Select a UI display screen, turn on the **Display** option to add the icon for the Now Assist panel in the menu bar.
3.  Select **Save and test**.

The AI agent executes the request for the agentic workflow.

## Example of the schedule a change agentic workflow output in the ServiceNow® AI Agent Studio

![Schedule a change agentic workflow output in AI Agent Studio.](../image/now-assist-itsm-schedule-a-change-workflow.png)

Access and use the schedule a change agentic workflow from the Now Assist panel.

You can add a query using the change request number to use the AI agent.

For the query instruction, follow the steps specified in the **List of steps** field of the Define key requirements screen in the agentic workflow record.

In the AI Agent Studio, the human agent gets notified as soon as a text message is generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

