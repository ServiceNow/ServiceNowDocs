---
title: Using AI agent workflows in Now Assist for WSD
description: Agentic workflows in Now Assist for WSD help complete workplace tasks autonomously.
locale: en-US
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-02-04"
reading_time_minutes: 4
breadcrumb: [Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Using AI agent workflows in Now Assist for WSD

Agentic workflows in Now Assist for WSD help complete workplace tasks autonomously.

<table id="table_gyx_brq_l2c"><thead><tr><th>

Agentic AI Workflow Name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Manage temporary space closures

</td><td>

This team of AI agents come together when there’s a meeting room maintenance case that must be looked at with priority.

 -   When the emergency maintenance request is submitted, maintenance work must be performed.
-   The emergency case is assigned to a user in the Workplace Event Planners assignment group.
-   The location is blocked by AI agents for maintenance.
-   If there are any existing reservations in the maintenance workspace, AI agents relocate or move the reservations to an available location.

 AI agents reduce repetitive tasks for Workplace event planners. They provide assistance and verify that employees have access to functional spaces within an organization during an outage or emergency maintenance. AI Agents handle the work for Workplace Event Planners so that they can focus on more important and complex tasks that require human intervention. For more information, see [Manage temporary space closures agentic workflow](maintenance-meeting-room-agent-ai.md).

</td><td>

-   Workplace case notes updater
-   Case Retriever
-   Reservation resolution processing AI agent

</td></tr><tr><td>

Help manage workplace reservations

</td><td>

This team of AI agents help Workplace Event Planners and autonomously reschedule events happening in the workplace. AI agents support Workplace Event Planners with all relevant information and preparation work when changes are occurring to a planned reservation. AI Agents gather relevant information and provide suggestions to the Workplace Event planners for the next best possible action. Event planners can review and optimize reservations as required by looking at the workplace case details.

 In order to finish the task, AI agents perform the following:

 -   Retrieve the change event edit workplace case details.
-   Analyze the reservation retrieved from the previous step.
-   Update Workplace case notes with all the actions taken.

 For more information, see [Help manage workplace reservations agentic workflow](manage-workplace-reservations-agent-ai.md).

</td><td>

-   Reservation updating AI agent
-   Case Retriever
-   Reservation analyzing AI agent
-   Workplace case notes updater

</td></tr><tr><td>

Optimize Cleaning activities

</td><td>

This team of AI agents get all open workplace maintenance management cases. The **Workplace Planned Maint Nightly Run** scheduled job runs on a daily or hourly basis to create maintenance cases. Each workplace maintenance case represents a cleaning or a maintenance case on a location for a certain time interval, also known as schedule \(on a daily or hourly basis\). The Optimize cleaning activities agentic AI workflow retrieves space utilization threshold for each workplace maintenance cases. Based on the space utilization threshold data, it creates new maintenance cases or deactivates underutilized maintenance cases. For more information, see [Optimize cleaning activities agentic workflow](optimize-cleaning-activities-agent.md).

</td><td>

-   Case aggregator AI agent
-   Utilization rate AI agent
-   Case optimizer AI agent

</td></tr><tr><td>

Automate map updates

</td><td>

The AI agent helps map admins configure the map during bulk updates to Indoor Mapping. The AI agent autonomously retrieves sources for the CAD file and resumes the import task. If the source isn't found, the AI agent moves the task to the `Waiting user input` state.

 For more information, see [Automate map updates agentic workflow](automate-map-updates-agent-ai.md).

</td><td>

Map Admin Agent

</td></tr><tr><td>

Workplace Advisor QnA

</td><td>

The Workplace Advisor QnA agentic AI workflow allows Reservation Managers to use the Now Assist panel to ask natural language questions about workplace reservations. For more information, see [Workplace advisor QnA agentic workflow](workplace-advisor-qna.md)

</td><td>

Workplace Reservation QnA Agent

</td></tr></tbody>
</table>**Important:** All use case and AI agent records are read only by default.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and complete the following steps:

-   Activate the use case.
-   Activate all agents within the use case.
-   Activate the trigger to invoke the use case automatically. If you prefer to invoke it manually, activating the trigger isn't necessary.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

