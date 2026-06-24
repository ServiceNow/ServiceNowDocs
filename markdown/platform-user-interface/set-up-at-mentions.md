---
title: Set up suggestions for mentions based on record access
description: Set up @mentions that display suggestions based on recipients with access to view the record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-user-interface/set-up-at-mentions.html
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering forms for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Set up suggestions for mentions based on record access

Set up @mentions that display suggestions based on recipients with access to view the record.

## Before you begin

Role required: admin

## About this task

An @mention is any posted update that contains @username anywhere in the body of the message.

When you use @mentions, context-based suggestions display a list of recipients with access to view the record.

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Add a system property named **glide.ui.mentions.check\_record\_visibility**.

    For more information on adding system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

3.  Set the Value to **true**.

4.  Select **Submit**.


