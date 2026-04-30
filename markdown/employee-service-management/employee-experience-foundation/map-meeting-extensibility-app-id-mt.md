---
title: Map ServiceNow Meeting Extensions app ID in ServiceNow
description: Map the ServiceNow Meeting Extensions app ID in your ServiceNow instance to automatically add the meeting extensions tab in Microsoft Teams for a conference call.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrate Meeting Extensions pre-published app with Microsoft Teams, Integration for Agent Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Map ServiceNow Meeting Extensions app ID in ServiceNow

Map the ServiceNow Meeting Extensions app ID in your ServiceNow instance to automatically add the meeting extensions tab in Microsoft Teams for a conference call.

## Before you begin

Role required: Microsoft Teams admin

## Procedure

1.  Copy the Meeting Extensions App ID.

    1.  Log in to [Microsoft Teams admin portal](https://admin.teams.microsoft.com/).

    2.  Navigate to **Teams apps** &gt; **Manage apps**.

    3.  Search and select **ServiceNow Meeting Bot**.

    4.  Select **ServiceNow Meeting Bot**.

    5.  Copy the App ID in a notepad.

        **Note:** Ensure that you are copying the value of the **App ID** and not the **External app ID**.

        This **App ID** must be updated in System Properties in ServiceNow instance.

2.  Paste the Meeting Extensions App ID.

    1.  Log in to the ServiceNow instance.

    2.  Navigate to **Notify** &gt; **Microsoft Teams** &gt; **Properties**.

    3.  Update the **Application ID of Meeting Extensibility teams app** field with the above App ID.

    4.  Click **Save**.

        **Note:** Log in to the [Microsoft Teams portal](https://teams.microsoft.com/), under **Apps**, search and open **ServiceNow Meetings Bot** app at least once for the Meeting Extensions app to work.

    Meeting Extensions app is set up.


## What to do next

After completing Meeting Extensions integration with Microsoft Teams, see the section [Meeting Extensions for Microsoft Teams](../concept/meeting-extensibility-ms-teams.md).

**Parent Topic:**[Integrate Meeting Extensions pre-published app with Microsoft Teams](../concept/setup-meeting-extensibility-multi-tenant.md)

