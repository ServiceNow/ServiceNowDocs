---
title: Assign ownership to a topic
description: Assign ownership of a taxonomy topic to give a user or group with the content manager \(sn\_cd.content\_manager\) role exclusive content publishing ability for the Content Publishing widgets in that topic.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Content Ownership, Setup employee communications, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Assign ownership to a topic

Assign ownership of a taxonomy topic to give a user or group with the content manager \(sn\_cd.content\_manager\) role exclusive content publishing ability for the Content Publishing widgets in that topic.

## Before you begin

Role required: sn\_cd.content\_admin

Ensure **Yes** is checked under **Allow Ownership for Topics** under Content Publishing or Content Experiences properties. For more information, see [Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md) and [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

## About this task

The Unified Taxonomy is a collection of hierarchical topics that brings together different content types, such as requests, articles, quick links, learning content, and employee communications. For more information, see [Unified Taxonomy for Employee Center](../concept/config-taxonomy.md).

## Procedure

1.  Navigate to **All** &gt; **Content Taxonomy** &gt; **Topics**.

2.  Select a topic.

    -   To assign ownership to a user, select the **Content Publishing Owner by user** tab.
    -   To assign ownership to a group, select the **Content Publishing Owner by group** tab.
3.  Click **New**.

4.  From the **User** or **Group** field, click the **Lookup using list** \(![Lookup using list icon](../../human-resources/image/magnify-glass-outline-icon.png)\) icon and select a user or group.

    **Note:** Only groups that have the content admin \(sn\_cd.content\_admin\) or content manager \(sn\_cd.content\_manager\) roles appear. If the members of the group have these roles, but the group does not, the group does not appear.

5.  Select **Submit**.

    After a user or group is assigned to a topic, only that user or group can publish content to that topic. Removing the user or group allows all content managers to publish content to that topic.


