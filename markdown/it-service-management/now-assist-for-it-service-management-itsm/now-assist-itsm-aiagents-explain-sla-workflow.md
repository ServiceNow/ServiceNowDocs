---
title: IT Service Management AI agent collection explain SLA agentic workflow
description: Use the explain SLA agentic workflow to analyze a Service Level Agreement \(SLA\) and gain insight into the SLA assignment, task ownership, and pause and resume events in the SLA duration for a task, such as an incident, problem, case, or change request.
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

# IT Service Management AI agent collection explain SLA agentic workflow

Use the explain SLA agentic workflow to analyze a Service Level Agreement \(SLA\) and gain insight into the SLA assignment, task ownership, and pause and resume events in the SLA duration for a task, such as an incident, problem, case, or change request.

## Explain SLA agentic workflow overview

The explain SLA agentic workflow begins with identifying the most important SLA associated with a task. By default, the matched SLA is the SLA that would be breached first. However, a different SLA can also be identified based on your SLA timer configuration. The workflow then suggests a few standard questions about the identified SLA. Based on the questions asked, the workflow explains the SLA breakdown by assignment, SLA duration, and provides insight into the task ownership, reassignment, and causes for the SLA breach.

The explain SLA agentic workflow can be used in the following scenarios:

-   Before an SLA is breached, assigned users can gain an insight into the time elapsed and potential for the SLA breach. The assigned user can track gaps with previous assignments and SLA ownership if the SLA breakdown shows multiple reassignments across teams and repeated pauses in the SLA. Based on requirements, the user can ask the agent questions to plan the handling of the incident or task in adherence to the SLA timelines.
-   After an SLA is breached, users or groups can investigate the possible causes of the breach, reassignment patterns, and users who were assigned for the longest duration. The agent can also provide information on the factors contributing to the SLA breach. Based on the information, the SLA can be monitored and configured for better handling of tasks, and improved assignment plans can be created.

**Note:** The explain SLA agentic workflow doesn’t have a trigger and is invoked manually.

To modify the explain SLA agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## Explain SLA

Autonomously generate an explanation for the SLA breakdown.

**Note:** The workflow can be accessed by the sn\_uxc\_gen\_ai.sn\_aia\_sla\_explain role that is available as a part of the itil role.

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Explain SLA**.

## AI agent used in the explain SLA agentic workflow

The explain SLA AI agent provides a list of suggested questions that you can ask the agent to get a detailed explanation about the SLA. You can also add custom questions regarding the SLA.

The following SLA details can be traced by conversing with the agent:

-   Reason for choosing the SLA for the given task
-   SLA target and vendor values
-   If the SLA is likely to breach
-   Time elapsed for the SLA
-   Number of times the SLA has paused or resumed, and their details
-   User and group assignments for the SLA
-   SLA assignment and breach patterns

## Generating SLA information using the explain SLA agentic workflow

In the agentic workflow record:

1.  Review the information in the Describe and connect screen and in the Define trigger screen, make the necessary updates, and then select **Save and Continue**.
2.  In the Select a UI display screen, turn on the **Display** option to add the icon for the Now Assist panel in the menu bar.
3.  Select **Save and test**.

The AI agent executes the request for the agentic workflow.

## Example of the explain SLA agentic workflow output in the ServiceNow® AI Agent Studio

![Explain SLA agentic workflow output in AI Agent Studio.](../image/now-assist-itsm-aiagents-explain-sla-workflow.png)

Access and use the explain SLA agentic workflow from the Now Assist panel.

You can add a query using the change request number to use the AI agent. You can enter the number from the suggested questions, add keywords from the questions, or ask custom questions to the agent.

For the query instruction, follow the steps specified in the **List of steps** field of the Define key requirements screen of the agentic workflow record.

In the AI Agent Studio, the human agent gets notified as soon as a text message is generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

