---
title: Assign ownership of an audience
description: Provide ownership of an audience to a user or group with the content manager \(sn\_cd.content\_manager\) role so only they can access and schedule content for the audience.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Content Ownership, Setup employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Assign ownership of an audience

Provide ownership of an audience to a user or group with the content manager \(sn\_cd.content\_manager\) role so only they can access and schedule content for the audience.

## Before you begin

Role required: sn\_cd.content\_admin

Ensure **Yes** is checked under **Allow Ownership for Audiences** under Content Publishing or Content Experiences properties. For more information, see [Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md) and [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

## About this task

An audience is a defined group of employees that will receive targeted content. For information on creating an audience, see [Create an audience](ec-audiences.md).

You can restrict an audience to a specific content manager or group of content managers, which specifies which audience the content managers can publish for, and prevents other content managers from publishing content to that audience. For example, assign a regional Human Resources manager the sole ability to create content for employees based in that country.

## Procedure

1.  Navigate to **All** &gt; **Content Publishing** &gt; **Re-usable Components** &gt; **Audiences**.

2.  Select an audience or create a new audience.

    -   To assign ownership to a user, select the **Restrict audience by user** tab.
    -   To assign ownership to a group, select the **Restrict audience by group** tab.
3.  Click **New**.

4.  From the **User** or **Group** field, click the **Lookup using list** \(![Lookup using list icon](../../human-resources/image/magnify-glass-outline-icon.png)\) icon and select a user or group.

    **Note:** Only groups that have the content admin \(sn\_cd.content\_admin\) or content manager \(sn\_cd.content\_manager\) roles appear. If the members of the group have these roles, but the group does not, the group does not appear.

5.  Select **Submit**.

    After a user or group is associated with an audience, only that user or group can access the audience. Remove the user or group to make the audience accessible to all content managers.


