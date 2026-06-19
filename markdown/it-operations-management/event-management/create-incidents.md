---
title: Create incidents
description: Configure automation rules to automatically create incidents from alerts that require immediate attention and resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/create-incidents.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [Event Management, incident creation, automation rules]
breadcrumb: [ITOM Configuration console for Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create incidents

Configure automation rules to automatically create incidents from alerts that require immediate attention and resolution.

## Before you begin

Verify that you have installed the ITOM AIOps and Now Assist for IT Operations Management \(ITOM\) plugins.

Ensure you are in the Configure IT Operations Management page.

Role required: evt\_mgmt\_admin or evt\_team\_operator

## About this task

Incident creation rules automatically generate incident records from alerts that meet specific criteria. This automation ensures that critical issues are promptly escalated to the appropriate teams for resolution while reducing manual effort in the incident management process.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Event Management** &gt; **Alert response**.

2.  Expand **Alert response**.

3.  Select **Create incidents**.

    A list of respond alert automations appears.

4.  Select **Create automation**.

    The Respond to alert page opens.

5.  Follow the steps in [Create Respond automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/respond-alert-sow-itom.md).

6.  To complete the setup, select **Mark as configured**.


