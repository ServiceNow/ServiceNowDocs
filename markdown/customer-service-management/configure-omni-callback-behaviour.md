---
title: Configure the callback behavior for Omnichannel Callback for Customer Service Management
description: such as enabling agent-scheduled callbacks, setting the maximum number of retry attempts or defining the expiration time, in Omnichannel Callback for Customer Service Management.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Omnichannel Callback, Enable communication channels, Configure, Customer Service Management]
---

# Configure the callback behavior for Omnichannel Callback for Customer Service Management

such as enabling agent-scheduled callbacks, setting the maximum number of retry attempts or defining the expiration time, in Omnichannel Callback for Customer Service Management.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** search field, enter `sn_callback`.

3.  Configure any of the properties listed in the following table.

    |Property|Default value|Description|
    |--------|-------------|-----------|
    |sn\_callback.callback\_expire\_time|60|Callback timeout in minutes after which the callback task is closed.|
    |sn\_callback.callback\_max\_retry\_attempts|5|Maximum retry attempts after which the callback task is closed.|
    |sn\_callback.enable\_scheduled\_callback|true|Option to enable scheduled callbacks by enabling customers to select a time slot for callback.|
    |sn\_callback.enable\_agent\_scheduled\_callback|Boolean|Enable the agent-scheduled callback feature. When enabled, agents can schedule callbacks on behalf of customers from CSM/FSM Configurable Workspace.|


