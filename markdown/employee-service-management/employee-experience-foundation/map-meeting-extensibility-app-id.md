---
title: Add the Meeting Extensions tab in Microsoft Teams
description: Map the ServiceNow Meeting Extensions app ID in your ServiceNow instance to automatically add the meeting extensions tab in Microsoft Teams for a conference call.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate Meeting Extensions self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Add the Meeting Extensions tab in Microsoft Teams

Map the ServiceNow® Meeting Extensions app ID in your ServiceNow instance to automatically add the meeting extensions tab in Microsoft Teams for a conference call.

## Before you begin

Role required: sn\_notify\_msteams.admin

## Procedure

1.  Log in to the ServiceNow instance.

2.  Navigate to **Notify** &gt; **Microsoft Teams** &gt; **Properties**.

3.  Paste the copied App ID value in **Application ID of Meeting Extensibility teams app \(The App ID can be found from "Manage apps" page in Teams Admin portal\)** and select **Save**.

    **Note:** Log in to the [Microsoft Teams portal](https://teams.microsoft.com/), search for and open **Notify Connector for Microsoft Teams** app at least once for the Meeting Extensions app to work.

    Meeting Extensions app is set up.


**Parent Topic:**[Integrate Meeting Extensions self-configured app with Microsoft Teams](../concept/setup-meeting-extensibility-single-tenant.md)

