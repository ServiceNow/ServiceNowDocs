---
title: Set UiPath WebHook routing policies
description: Set the UiPath WebHook routing policies to enable the data to get populated in the ServiceNow tables, and then used by Automation Center.
locale: en-US
release: xanadu
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring UiPath with Automation Center, Configuring Automation Center, Automation Center, Creating integrations with applications]
---

# Set UiPath WebHook routing policies

Set the UiPath WebHook routing policies to enable the data to get populated in the ServiceNow tables, and then used by Automation Center.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **UiPath** &gt; **UiPath WebHook Routing Policies**.

2.  Turn the **Active** flag for the routing policy to **True**.

    When UiPath data comes to the ServiceNow instance, these routing policies take care of triggering the corresponding flows to store data in ServiceNow tables. By default, the flag is set to **False**.


**Parent Topic:**[Configuring UiPath with Automation Center](../concept/uipath-config.md)

