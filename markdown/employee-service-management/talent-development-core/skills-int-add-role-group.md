---
title: Adding role groups and role levels for skills administration
description: Create additional role groups and role levels based on the various roles in your organization and create a comprehensive role-based structure to accommodate various employee roles in your organization.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Skills Foundation, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Adding role groups and role levels for skills administration

Create additional role groups and role levels based on the various roles in your organization and create a comprehensive role-based structure to accommodate various employee roles in your organization.

## About this task

You can add role groups and role levels by importing them through the job architecture data import. For more information, see [Load job architecture data into your ServiceNow instance](load-data-skills-tables.md).

This procedure describes how to add role groups and role levels to the Role Groups \[sn\_skills\_int\_role\_group\] and Role Levels \[sn\_skills\_int\_role\_level\] tables manually after the job architecture data is imported.

## Before you begin

Role required: sn\_skills\_int.job\_arch\_admin

## Procedure

1.  Navigate to **All** &gt; **Job Architecture** &gt; **Role Groups**.

2.  Create a role group.

    1.  Select **New**.

    2.  Enter a name and description for the role group.

    3.  In the **Job family** field, select a relevant job family for the role group.

    4.  Indicate that this role group is an addition to the existing role group by selecting **Is supplemental**.

    5.  Select **Submit**.

3.  Create new role levels for the role group.

    1.  Select the newly created role group.

    2.  Select the **Role Levels** tab.

    3.  Select **New**.

    4.  Enter a title and description for the role level.

    5.  The **Role group** field is already preselected with the newly created role group.

        **Note:** You can also choose a different role group for the role level. When changing the role group of the existing role level, the skills that belong to the previous role group will be removed. However, any skills explicitly added to the role level will be retained.

    6.  Select a **Job profile** the role level should belong to.

    7.  Make the role level active by selecting **Active**.

    8.  Select **Submit**.

4.  Add skills to the role groups and role levels.

    **Note:**

    -   If a skill is marked as required at the role group level, the setting will be applied to that skill in all the role levels of that role group. You cannot edit the field on the role level.
    -   The setting for a skill relevance as High, Medium, or Low at the role group level will also be applied to that skill in all the role levels of that role group. You cannot change the relevance on the role level.
    -   The skills in role groups are automatically attached to the role levels.

## What to do next

Create transitions using the **From Role Groups** and **To Role Groups** related lists. Related role groups have similar skill sets and can be used in suggesting the next possible lateral roles for an employee in other role groups. Adding a role group to the To Role Groups list will update the From Role Groups list of other role groups.

