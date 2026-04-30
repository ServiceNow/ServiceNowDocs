---
title: Configure the add support users property
description: To enable support agents to add users to a Connect Support conversation, add the glide.connect.support.add\_members property.
locale: en-US
release: yokohama
product: Connect
classification: connect
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Connect Support administration, Connect Support, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the add support users property

To enable support agents to add users to a Connect Support conversation, add the **glide.connect.support.add\_members** property.

## Before you begin

Role required: admin

**Warning:** Enabling the **glide.connect.support.add\_members** property can negatively impact instance performance if there are large numbers of users logged in to the instance.

## About this task

When the **glide.connect.support.add\_members** property is added and enabled, support agents can add users to a support conversation. Any added user can also add other users. Only the assigned agent can create an incident from the chat. When non-support agents are added to a chat, the chat appears in their chat tab.

**Note:** Make sure you are in the Global scope when adding this property.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Verify that the property does not exist by searching for the property name.

    If the property does exist, update the property with the information in the following table.

3.  Select **New**.

4.  Complete the form.

    |Field|Value|
    |-----|-----|
    |**Name**|glide.connect.support.add\_members|
    |**Type**|true \| false|
    |**Value**|true|


