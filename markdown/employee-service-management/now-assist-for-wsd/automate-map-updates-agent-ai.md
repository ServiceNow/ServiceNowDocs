---
title: Automate map updates agentic workflow
description: This AI agent helps map admins configure the map during bulk updates to Indoor Mapping.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Automate map updates agentic workflow

This AI agent helps map admins configure the map during bulk updates to Indoor Mapping.

## Automate map updates workflow overview

The AI agent autonomously retrieves sources for the CAD file and resumes the import task. If the source isn't found, the AI agent moves the task to the `Waiting user input` state. For more information about import tasks, see [Work on an import task](../../wsd-indoor-mapping/task/work-import-task.md).

The AI agent autonomously performs the following:

-   Retrieves all the sources for the uploaded CAD.
-   Sets the CAD source on the Import Task and resumes the task.
-   Moves the task to the `Waiting user input` state if the source isn't found.

## Automate map updates workflow

To access the Automate map updates workflow, follow these steps:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Automate map updates**.
3.  Select **Define trigger** to review the trigger factors for this agentic workflow.
4.  The **Display** option enables the Now Assist panel. For more information, see [Select display](automate-map-updates-agent-ai.md#section_bc5_ykn_x2c).

## AI agents used in the Automate map updates workflow

The **Connect AI agents** section in the Describe and Connect workflow displays the AI Agents that are working on the Automate map updates workflow.

The following agents are used in the Automate map updates workflow:

|AI agent Name|Description|
|-------------|-----------|
|Map Admin Agent|This agent handles anything related to Indoor Mapping configuration.|

## Select display

In the Select a UI display section, select **Display** to display the Now Assist panel. Workplace users with the now\_assist\_panel\_role receive notifications for the triggered use case output. When the Now Assist panel option is enabled, the AI agent output or notifications are displayed in the Now Assist panel.

**Note:** To view the output from a triggered use case, you should have the now\_assist\_panel\_role.

Select this option to receive and review notifications sent by AI agents in the Now Assist panel. AI agents send notifications to Map Admins in the Now Assist panel about updates to the import tasks.

**Parent Topic:**[Using AI agent workflows in Now Assist for WSD](now-assist-wsd-using-agentic-use-cases.md)

**Related topics**  


[Manage temporary space closures agentic workflow](maintenance-meeting-room-agent-ai.md)

[Help manage workplace reservations agentic workflow](manage-workplace-reservations-agent-ai.md)

[Optimize cleaning activities agent overview](optimise-cleaning-agent-overview.md)

[Workplace Advisor Overview](workplace-advisor-overview.md)

[Workplace Concierge agentic workflow](workplace-concierge-ai-agent.md)

[implement-autonomous-l1-agent-for-workplace.md](implement-autonomous-l1-agent-for-workplace.md)

[Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

