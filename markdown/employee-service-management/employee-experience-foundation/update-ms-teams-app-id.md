---
title: Update the Microsoft Teams application ID
description: Update the Microsoft Teams application ID in your ServiceNow instance to navigate to your custom ServiceNow for Microsoft Teams app.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Employee Center for Microsoft Viva Connections, Employee Center for Microsoft Viva Connections, Employee Center Integrations, Unified Employee Experience, Employee Service Management]
---

# Update the Microsoft Teams application ID

Update the Microsoft Teams application ID in your ServiceNow instance to navigate to your custom ServiceNow for Microsoft Teams app.

## Before you begin

Ensure you have created and uploaded the ServiceNow for Microsoft Teams manifest file. For more information, see [Create and download manifest file for Employee Center and Microsoft 365 integration](../../sn-teams/task/download-manifest-ms365.md).

Role required:

-   Microsoft: Microsoft Teams administrator
-   ServiceNow instance: external\_app\_install\_admin

## Procedure

1.  Copy the App ID.

    1.  Log in to the Microsoft Teams admin center.

    2.  Navigate to **Teams apps** &gt; **Manage apps**.

    3.  Select the ServiceNow for Microsoft 365 app.

    4.  Copy the App ID.

2.  Update the App ID.

    1.  Log in to your ServiceNow instance.

    2.  In the filter navigator, enter `sys_properties.list`.

    3.  In the **Name** field, search for `sn_now_ms_viva.service_now_for_teams_app_id`.

    4.  Select the property to view the property details.

    5.  Update the **App ID** in the **Value** field.

    6.  Select **Update**.


**Parent Topic:**[Configuring Employee Center for Microsoft Viva Connections](../concept/configure-viva.md)

