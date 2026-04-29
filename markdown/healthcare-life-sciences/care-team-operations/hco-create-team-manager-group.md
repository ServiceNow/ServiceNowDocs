---
title: Create a group for all care team managers in Healthcare Operations Core
description: Create a group for care team managers with the sn\_hco.care\_team\_manager role assigned so that users added to this group inherits the collection of roles for Healthcare Operations Core.
locale: en-US
release: australia
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Create a group for all care team managers in Healthcare Operations Core

Create a group for care team managers with the sn\_hco.care\_team\_manager role assigned so that users added to this group inherits the collection of roles for Healthcare Operations Core.

## Before you begin

Role required: admin

## About this task

**Note:** The sn\_hco.care\_team\_manager role inherits the sn\_hco.care\_team\_member role, so users assigned to your team manager group don’t need to be assigned to your team member group.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Select **New**.

3.  In the name field, enter a name for your team member group.

4.  Fill in the other fields as needed.

5.  Navigate to the roles related list.

6.  Select **Edit**.

7.  Add the sn\_hco.care\_team\_manager role into the Roles List.

8.  Select **Save**.


## Result

A user group has been created that you can assign care team managers to when doing automated user imports.

