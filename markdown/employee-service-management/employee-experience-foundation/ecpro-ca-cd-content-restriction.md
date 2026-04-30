---
title: Assign ownership of content
description: Assign a user or group with the content manager \(sn\_cd.content\_manager\) role to a content item so only that user or group can edit and publish the content.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-10-06"
reading_time_minutes: 1
breadcrumb: [Content Ownership, Setup employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Assign ownership of content

Assign a user or group with the content manager \(sn\_cd.content\_manager\) role to a content item so only that user or group can edit and publish the content.

## Before you begin

Role required: sn\_cd.content\_admin

Ensure **Yes** is checked under **Allow Ownership for Content Items** under Content Publishing or Content Experiences properties. For more information, see [Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md) and [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

## About this task

Provide a content manager or group of managers with exclusive access to sensitive content, such as a notice of an upcoming merger or reduction of workforce.

Alternatively, use a content item as a template that can be repeatedly cloned and assigned to content owners for customization.

## Procedure

1.  Navigate to **All** &gt; **Content Publishing** &gt; **Content Library** &gt; **View All**.

2.  Select content.

3.  From the top-left menu \(![Menu icon](../../../reuse/icons/product-icons/menu-outline-24.svg)\), select **View content record**.

    -   To assign ownership to a user, select the **Restrict content by user** tab.
    -   To assign ownership to a group, select the **Restrict content by group** tab.
4.  Click **New**.

5.  From the **User** or **Group** field, click the **Lookup using list** \(![Lookup using list icon](../../human-resources/image/magnify-glass-outline-icon.png)\) icon and select a user or group.

    **Note:** Only groups that have the content admin \(sn\_cd.content\_admin\) or content manager \(sn\_cd.content\_manager\) roles appear. If the members of the group have these roles, but the group does not, the group does not appear.

6.  Select **Submit**.

    After a user or group is associated with content, only that user or group can access the content when scheduling content or when adding content to a campaign. Removing the user or group makes the content accessible by all content managers.


