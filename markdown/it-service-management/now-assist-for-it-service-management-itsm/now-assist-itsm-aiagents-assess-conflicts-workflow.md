---
title: IT Service Management AI agent collection assess conflicts for a change request agentic workflow
description: Use the assess conflicts for a change request agentic workflow to run conflict detection for change requests and assess conflicts, and identify affected configuration items \(CIs\) and impacted services.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Change Management, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection assess conflicts for a change request agentic workflow

Use the assess conflicts for a change request agentic workflow to run conflict detection for change requests and assess conflicts, and identify affected configuration items \(CIs\) and impacted services.

## Assess conflicts for a change request agentic workflow overview

Using the assess conflicts for a change request agentic workflow, you can run conflict detection for change requests to view existing conflicts and the summary of conflict types, affected CIs, and impacted services.

The summary of each conflict type generated using the assess conflicts for a change request agentic workflow includes the following sections:

-   Affected CI
-   Conflicting change
-   Maintenance or blackout schedules

You can also use the workflow to rerun conflict detection.

**Note:** The assess conflicts for a change request agentic workflow doesn’t have a trigger and is invoked manually.

To modify the assess conflicts for a change request agentic workflow, duplicate it, and adjust the settings according to your requirements.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Assess conflicts for a change request

Autonomously assess conflicts for change requests.

**Note:** The workflow can be accessed by roles contained within the sn\_change\_write or itil roles.

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Assess change request conflicts**.

## AI agent used in the assess conflicts for a change request agentic workflow

The Change conflict assessor AI agent is used to identify conflict types and summarize the impacted schedules, CIs, and services related to the change request.

**Important:** The configuration item, planned start, and end date values must be available for the change request before running the conflict detection using the AI agent. If no information is available, the agent asks you to provide them.

## View conflicts using the assess conflicts for a change request agentic workflow

In the agentic workflow record:

1.  Review the information in the Describe and connect screen and in the Define trigger screen, make the necessary updates, and then select **Save and Continue**.
2.  In the select a UI display screen, turn on the **Display** option to add the icon for the Now Assist panel in the menu bar.
3.  Select **Save and test**.

The agent executes the request for the agentic workflow.

## Example of the assess conflicts for a change request agentic workflow output in the ServiceNow® AI Agent Studio

![Assess conflicts for a change request agentic workflow output in AI Agent Studio.](../image/now-assist-itsm-assess-conflicts-for-a-change-request-workflow.png)

Access and use assess conflicts for a Change request agentic workflow from the Now Assist panel.

You can add a query using the change request number to use the AI agent.

For the query instruction, follow the steps specified in the **List of steps** field of the Define key requirements screen of the agentic workflow record.

In the AI Agent Studio, the human agent gets notified as soon as a text message is generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

