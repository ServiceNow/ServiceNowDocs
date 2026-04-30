---
title: Disable email responses from the case activity stream
description: By default, customer service agents can respond to cases using options within a customer email thread instead of having to use another email client. As an admin, you can disable this option for a business manager who does not want agents to interact with customers directly.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Disable email responses from the case activity stream

By default, customer service agents can respond to cases using options within a customer email thread instead of having to use another email client. As an admin, you can disable this option for a business manager who does not want agents to interact with customers directly.

## Before you begin

Role required: admin

## About this task

Agents can use the **Reply**, **Reply All**, and **Forward**

buttons in the case activity stream to respond to customer emails. This feature is enabled by default. Users with the system administrator role can disable this feature and hide these buttons if needed from the Agent Workspace or Configurable Workspace application.

## Procedure

1.  Navigate to **All** and enter **sys\_properties.list**.

    The System Properties page opens.

2.  Click **New**.

3.  Create a new system property with the name **sn\_agent\_workspace.activity\_email\_options\_enabled**.

4.  Set the value to false and click **Submit**.

    Users with the role **sn\_customerservice\_agent** are now unable to reply to or forward emails.


