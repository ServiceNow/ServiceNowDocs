---
title: Configure mention suggestions
description: Configure @mentions that display suggestions based on recipients with access to view the record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure mention suggestions

Configure @mentions that display suggestions based on recipients with access to view the record.

## Before you begin

Role required: admin

## About this task

An @mention is any posted update that contains @username anywhere in the body of the message.

When you use @mentions, context-based suggestions display a list of recipients with access to view the record.

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Add a system property named **glide.ui.mentions.check\_record\_visibility**.

    For more information on adding system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

3.  Set the Value to **true**.

4.  Select **Submit**.


