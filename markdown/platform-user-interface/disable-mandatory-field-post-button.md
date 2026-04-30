---
title: Disable the Post button from disappearing in Activity stream
description: Disable the Post button from disappearing in Activity stream when mandatory fields aren't filled in. The Post button is functional even when mandatory fields aren't filled in.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering Activity stream for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Disable the Post button from disappearing in Activity stream

Disable the Post button from disappearing in Activity stream when mandatory fields aren't filled in. The Post button is functional even when mandatory fields aren't filled in.

## Before you begin

The **Post** button disappears by default when the Comments or Work Notes fields are made mandatory by a UI Policy on the incident\_task table. This task enables you to disable that functionality so that the button is visible and useable even when mandatory fields aren't filled in.

Role required: admin

## Procedure

1.  Enter `sys_properties.list` in the **Filter navigator**.

2.  Select **glide.activity.compose.can\_post\_mandatory\_fields** from the list.

3.  In the **Value** field, set the value to **true**.


