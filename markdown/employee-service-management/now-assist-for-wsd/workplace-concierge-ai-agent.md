---
title: Workplace Concierge agentic workflow
description: Use the Workplace Concierge agentic workflow to register visitors from existing communication tools like emails, calendars, or the Virtual Agent.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-03-18"
reading_time_minutes: 3
breadcrumb: [Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Workplace Concierge agentic workflow

Use the Workplace Concierge agentic workflow to register visitors from existing communication tools like emails, calendars, or the Virtual Agent.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Workplace Concierge workflow overview

Workplace Concierge is an agentic workflow that operates directly from communication tools like email, calendar, and Now Assist in Virtual Agent. When you add the Workplace Concierge to a conversation, it identifies the intent to schedule a meeting, gathers and validates the necessary visit details, confirms the information with the host, and then creates the visit and visitor invitations. If any mandatory detail is absent or ambiguous, Workplace Concierge pauses and communicates with the host before proceeding.

Workplace Concierge supports the following communication channels:

-   Calendar invite: Workplace Concierge can be added as a guest to a calendar invite
-   Email thread: Workplace Concierge can be added in the CC field of the email thread
-   Now Assist in Virtual Agent: Workplace Concierge can be invoked in the chat by entering keywords like `invite a visitor`

After a visit is created, the Workplace Concierge sends invitation emails with a link to the visitor portal. Workplace Concierge also monitors replies and updates the visitor records. Visitors can respond to the email or use the portal link based on their preference. Hosts can use simple commands to send reminders or cancel specific visits, and they receive progress notifications like how many visitors have completed the pre-check tasks.

## Workplace Concierge workflow

To access the Workplace Concierge workflow, follow these steps:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Automate map updates**.
3.  Select **Define trigger** to review the trigger factors for this agentic workflow.
4.  The **Display** option enables the Now Assist panel. For more information, see [Select display](workplace-concierge-ai-agent.md#section_bc5_ykn_x2c).

## AI agents used in the Workplace Concierge workflow

The **Connect AI agents** section in the Describe and Connect workflow displays the AI Agents that are working on the Automate map updates workflow.

The following agents are used in the Automate map updates workflow:

|AI agent Name|Description|
|-------------|-----------|
|Chat Visit Agent|This agent assists hosts in managing workplace visits, adding visitors and checking visit requirements from Now Assist in Virtual Agent.|
|Email Visit creation agent|This agent assists hosts in managing workplace visits from emails and calendar invites.|
|Email Visitor Intake agent|This agent collects and processes visitor information through email replies sent by visitors. The agent communicates directly with visitors via email and updates visitor records based on email responses.|

## Select display

In the Select a UI display section, select **Display** to display the Now Assist panel. Workplace users with the now\_assist\_panel\_role receive notifications for the triggered use case output. When the Now Assist panel option is enabled, the AI agent output or notifications are displayed in the Now Assist panel.

**Note:** To view the output from a triggered use case, you should have the now\_assist\_panel\_role.

Select this option to receive and review notifications sent by AI agents in the Now Assist panel. AI agents send notifications to Map Admins in the Now Assist panel about updates to the import tasks.

-   **[Use Workplace Concierge with Now Assist in Virtual Agent](../task/use-concierge-virtual-agent.md)**  
Invoke Workplace Concierge from Now Assist in Virtual Agent to invite visitors to your organization.
-   **[Use Workplace Concierge with email or calendar invite](../task/use-concierge-email.md)**  
Add the Workplace Concierge to an email thread or a calendar invite.

**Parent Topic:**[Using AI agent workflows in Now Assist for WSD](now-assist-wsd-using-agentic-use-cases.md)

**Related topics**  


[Manage temporary space closures agentic workflow](maintenance-meeting-room-agent-ai.md)

[Help manage workplace reservations agentic workflow](manage-workplace-reservations-agent-ai.md)

[Optimize cleaning activities agent overview](optimise-cleaning-agent-overview.md)

[Automate map updates agentic workflow](automate-map-updates-agent-ai.md)

[Workplace Advisor Overview](workplace-advisor-overview.md)

[implement-autonomous-l1-agent-for-workplace.md](implement-autonomous-l1-agent-for-workplace.md)

[Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

