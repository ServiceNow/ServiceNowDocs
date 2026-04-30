---
title: Assign ownership to a portal page
description: Assign ownership of a portal page to give a user or group with the content manager \(sn\_cd.content\_manager\) role exclusive content publishing ability for the Content Publishing widgets in that page.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content Ownership, Setup employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Assign ownership to a portal page

Assign ownership of a portal page to give a user or group with the content manager \(sn\_cd.content\_manager\) role exclusive content publishing ability for the Content Publishing widgets in that page.

## Before you begin

Role required: sn\_cd.content\_admin

Ensure **Yes** is checked under **Allow Ownership for Portal Pages** under Content Publishing or Content Experiences properties. For more information, see [Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md) and [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Pages**.

2.  Select the **ID** of the page.

3.  Scroll down to the related list tabs.

    -   To assign ownership to a user, select the **Content Publishing Owner by User** tab.
    -   To assign ownership to a group, select the **Content Publishing Owner by Group** tab.
4.  Click **New**.

5.  From the **User** or **Group** field, click the **Lookup using list** \(![Lookup using list icon](../../human-resources/image/magnify-glass-outline-icon.png)\) icon and select a user or group.

    **Note:** Only groups that have the content admin \(sn\_cd.content\_admin\) or content manager \(sn\_cd.content\_manager\) roles appear. If the members of the group have these roles, but the group does not, the group does not appear.

6.  Select **Submit**.

    After a user or group is assigned to a page, only that user or group can publish content to that page. Remove the user or group to allow all content managers to publish content to that page.


