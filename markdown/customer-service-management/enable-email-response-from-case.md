---
title: Disable email responses from the case activity stream
description: Disable email responses from the case activity stream. Stop agents from interacting with customers directly.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Email to case, Email channel, Configure, Enable communication channels, Configure, Customer Service Management]
---

# Disable email responses from the case activity stream

Disable email responses from the case activity stream. Stop agents from interacting with customers directly.

## Before you begin

Role required: admin

## About this task

By default, customer service agents can respond to cases using options within a customer email thread instead of having to use another email client. Agents can use the **Reply**, **Reply All**, and **Forward** buttons in the case activity stream to respond to customer emails.

You can disable this feature and hide these buttons from the Agent Workspace or Configurable Workspace application.

## Procedure

1.  Navigate to **All** and enter `sys_properties.list`.

    The System Properties page opens.

2.  Select **New**.

3.  Create a system property with the name **sn\_agent\_workspace.activity\_email\_options\_enabled**.

4.  Set the value to false.

5.  Select **Submit**.


## Result

Users with the role sn\_customerservice\_agent are now unable to reply to or forward emails.

