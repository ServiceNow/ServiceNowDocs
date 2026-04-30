---
title: Enable Virtual Agent notifications for HR Service Delivery
description: Configure system properties to enable Virtual Agent notifications in Microsoft Teams.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-05"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Enable Virtual Agent notifications for HR Service Delivery

Configure system properties to enable Virtual Agent notifications in Microsoft Teams.

## Before you begin

Role required: admin

## About this task

**Note:** If your first installation of [HR Service Delivery for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/23364660c3b31010aab55b79c840ddc2) is version 3.4.0, Virtual Agent notifications are enabled by default. The following scenario is only applicable if you upgrade from older versions of the plugin.

After upgrading to [HR Service Delivery for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/23364660c3b31010aab55b79c840ddc2) version 3.4.0, you must configure a system property to enable Virtual Agent notifications.

## Procedure

1.  In the **All** menu, enter `sys_properties.list`.

    The System Properties table appears.

2.  In the name column, enter `*sn_now_teams`.

3.  For the **sn\_now\_teams\_hr.enable\_va\_comment\_notification** property, set the value to `true`.

    The default value of the property is **true**. If you've upgraded from an earlier version of [HR Service Delivery for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/23364660c3b31010aab55b79c840ddc2), the value is **false**.

    The comment notifications for all HR Core and HR Task tables are enabled.


## What to do next

To configure LLM actionable provider notifications, refer to [Configure LLM based provider notifications for HR](configure-llm-based-provider-notifications-for-hr.md).

**Parent Topic:**[Configure HR Service Delivery integration with Microsoft Teams](../concept/sn-ms-teams-config-hr.md)

