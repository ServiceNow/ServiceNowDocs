---
title: Alert ignore automations
description: Configure ignore rules to automatically suppress alerts that are not actionable or relevant to your operations team.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/ignore-alerts.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [Event Management, ignore alerts, noise reduction]
breadcrumb: [Configure Event Management using Setup Hub, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert ignore automations

Configure ignore rules to automatically suppress alerts that are not actionable or relevant to your operations team.

## Before you begin

Verify that you have installed the ITOM AIOps and Now Assist for IT Operations Management \(ITOM\) plugins.

Ensure you are in the Configure IT Operations Management page.

Role required: evt\_mgmt\_admin or evt\_team\_operator

## About this task

Ignore rules help reduce alert noise by automatically suppressing alerts that match specific criteria. This allows operations teams to focus on actionable alerts while filtering out known non-critical events, maintenance notifications, or false positives.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Reduce Noise**.

2.  Expand **Reduce Noise**.

3.  Select **Ignore alerts**.

    A list of ignore alert automations appears.

4.  Select **Create automation**.

    The Ignore alerts page opens.

5.  Follow the steps in [Create Ignore automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/create-ignore-automation-sow-itom.md).

6.  To complete the setup, select **Mark as configured**.


