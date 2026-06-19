---
title: Alert group automations
description: Configure grouping rules to automatically consolidate related alerts into single actionable items for more efficient incident management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/group-alerts.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [Event Management, alert grouping, noise reduction]
breadcrumb: [Configure Event Management using Setup Hub, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert group automations

Configure grouping rules to automatically consolidate related alerts into single actionable items for more efficient incident management.

## Before you begin

Verify that you have installed the ITOM AIOps and Now Assist for IT Operations Management \(ITOM\) plugins.

Ensure you're in the Configure IT Operations Management page.

Role required: evt\_mgmt\_admin or evt\_team\_operator

## About this task

Alert grouping rules automatically combine related alerts that represent the same underlying issue or event. This reduces alert volume and helps operations teams focus on resolving the root cause rather than managing multiple individual alerts for the same problem.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Reduce Noise**.

2.  Expand **Reduce Noise**.

3.  Select **Group alerts**.

    A list of group alert automations appears.

4.  Select **Create automation**.

    The Group alerts page opens.

    \[Omitted image "ai-specialist-group-alerts-console.png"\] Alt text: Alerts grouping page where you can create a grouping automation.

    You can use the suggested grouping automations to create your grouping automation. If you have the Now Assist for IT Operations Management \(ITOM\) plugin installed, select **Configure with Now Assist** from the top-right of the page and ask the Now Assist chatbot to create an automation. The created automation appears in the list of automations.

    \[Omitted image "ai-specialist-group-now-assist-chatbot.png"\] Alt text: Now Assist chatbot to help you automatically create a group automation.

    For more information on group automation, see [Create Group automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/group-alert-sow-itom.md).

5.  To complete the setup, select **Mark as configured**.


