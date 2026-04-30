---
title: Example - Create a group for all team members in Healthcare Operations Core
description: Explore how a group is created for users that care team members can later be added to to inherit the correct permissions.
locale: en-US
release: zurich
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 1
breadcrumb: [Create a group for team members, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Example - Create a group for all team members in Healthcare Operations Core

Explore how a group is created for users that care team members can later be added to to inherit the correct permissions.

## Before you begin

Role required: admin

## About this task

Scenario: As a ServiceNow administrator for a hospital, Armand faces the challenge of configuring over a thousand users for Healthcare Operations care teams. Manually creating each user account and assigning individual role permissions would be extremely time-consuming. To streamline this process, Armand creates a group in ServiceNow with the appropriate role permissions for care team members, allowing him to efficiently assign the correct permissions to many users during automated imports by linking them to this group.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Select **New**.

3.  In the name field, enter **HCO Team Members**.

4.  In the Description field, enter **Any user who will be a member of a Healthcare Organization.**

5.  Fill in other fields as needed.

6.  Navigate to the roles related list.

7.  Click **Edit**.

8.  Add the **sn\_hco.care\_team\_member** role into the Roles List.

9.  Click **Save**.


## Result

A group for all team members has been created. Armand can assign care team members to this group when doing automated imports.

