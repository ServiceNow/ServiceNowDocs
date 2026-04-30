---
title: Enable Virtual Agent notifications for IT Service Management
description: Configure system properties to enable Virtual Agent notifications in Microsoft Teams.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [IT Service Management integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Enable Virtual Agent notifications for IT Service Management

Configure system properties to enable Virtual Agent notifications in Microsoft Teams.

## Before you begin

Role required: admin

## About this task

**Note:** If your first installation of [IT Service Management for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/14eb9da8c3f310102986a81c8640dd08) is version 2.7.0, Virtual Agent notifications are enabled by default. The following scenario is only applicable if you upgrade from older versions of the plugin.

After upgrading to [IT Service Management for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/14eb9da8c3f310102986a81c8640dd08) version 2.7.0, you must configure system properties to enable Virtual Agent notifications.

The following tables are supported for Virtual Agent notifications in the base system.

-   Incident
-   Change
-   Requested Item

## Procedure

1.  In the **All** menu, enter `sys_properties.list`.

    The System Properties table appears.

2.  In the name column, search for `*sn_now_teams`.

3.  For the following properties, set the value to `true`.

    -   **sn\_now\_teams.enable\_va\_approval\_notification**: This property enables Virtual Agent notifications for approvals.
    -   **sn\_now\_teams\_it.enable\_va\_comment\_notification**: This property enables Virtual Agent notifications for comments.
    The default value of these properties is **true**. If you've upgraded from an earlier version of [IT Service Management for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/14eb9da8c3f310102986a81c8640dd08), the value is **false**.


## What to do next

You can customize the fields displayed in approval notifications. For more information, see [Customizing approval notification fields](../concept/customizing-approval-notifications.md).

To configure LLM actionable provider notifications, refer to [Configure LLM based provider notifications for ITSM](configure-llm-based-actional-notifications-for-itsm.md).

**Parent Topic:**[Configure IT Service Management integration with Microsoft Teams](../concept/sn-ms-teams-config-it.md)

