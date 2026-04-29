---
title: Set system properties for Microsoft Outlook integration
description: Use system properties to enable integration between Career Conversations and Microsoft Outlook so you can simultaneously create and schedule conversations with the Career Conversations app.
locale: en-US
release: australia
product: Career Conversations
classification: career-conversations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up Microsoft Outlook integration in Career Conversations, Install and configure Career Conversations, Career Conversations, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Set system properties for Microsoft Outlook integration

Use system properties to enable integration between Career Conversations and Microsoft® Outlook® so you can simultaneously create and schedule conversations with the Career Conversations app.

## Before you begin

Role required: admin \[sn\_egd\_act.admin\]

## Procedure

1.  Navigate to the **All** menu, and enter `sys_properties.list` in the navigation filter.

    The System Properties \[sys\_properties\] table appears.

2.  In the **Search** field that appears underneath the Application column, enter `Career Conversations`.

    A list of system properties associated with the Career Conversations app appears.

3.  Select the following system properties and define the corresponding values.

    |System property|Value|
    |---------------|-----|
    |**sn\_egd\_act.calendar\_provider\_option**|exchangeOnline|
    |**sn\_egd\_act.ex\_online\_notification\_url**|&lt;Microsoft Exchange Online Notification URL to handle notifications&gt;|
    |**sn\_egd\_act.ex\_online\_service\_account\_id**|&lt;Outlook service account used to manage calendar events&gt;|
    |**sn\_egd\_act.portal\_suffix**|esc|

    **Important:** Select **Update** to save the values you defined for each of the previously mentioned system properties.


**Parent Topic:**[Set up Microsoft Outlook integration in Career Conversations](../concept/outlook-integration-cc.md)

