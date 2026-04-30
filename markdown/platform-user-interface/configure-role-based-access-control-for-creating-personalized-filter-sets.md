---
title: Restrict access to creating filter sets in the Activity stream
description: Restrict specified agents from creating filter sets in the Activity stream.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administering Activity stream for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Restrict access to creating filter sets in the Activity stream

Restrict specified agents from creating filter sets in the Activity stream.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_user.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Select a user.

3.  Within the **Roles** tab, select **Edit**.

4.  Add **workspace.activity\_stream\_restrict\_create\_filter\_set** to the Roles List.

5.  Select **Save**.


## Result

The restricted user profile can no longer create filter sets in the Activity stream.

