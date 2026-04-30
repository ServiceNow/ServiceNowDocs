---
title: Configure an owning group for a lifecycle event
description: Create or modify an owning group to define the user group that owns a lifecycle event activity. Each owning group is responsible for overseeing the activities that fall under their purview.
locale: en-US
release: yokohama
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the supporting components for a lifecycle event, Building a lifecycle event, Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure an owning group for a lifecycle event

Create or modify an owning group to define the user group that owns a lifecycle event activity. Each owning group is responsible for overseeing the activities that fall under their purview.

## Before you begin

Role required: sn\_hr\_le.admin

To create, update, or delete an activity, you must be both a member of the associated owning group and have the sn\_hr\_le.activity\_writer role. For example, only members of the IT activity writers owning group with the sn\_hr\_le.activity\_writer role can configure an IT activity.

## Procedure

1.  Navigate to **All** &gt; **LIfecycle Events** &gt; **Administration** &gt; **Manage Owner Groups**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the owning group.|
    |Manager|Manager of the owning group.|
    |Description|Description of the owning group.|
    |Group email|Email address to associate with the owning group. This email acts as a group notification that sends an email to every member of the group.|
    |Parent|Parent group to associate with the owning group.|

4.  Click **Save**.

5.  In the **Roles**, **Group members**, **Groups**, and **Skills** related lists, assign the appropriate roles, users, groups, or HR skills to the owning group.

<table id="table_n1n_xqy_xgb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roles

</td><td>

Roles assigned to the owning group.**Note:** Any roles assigned to the parent group are automatically assigned to the owning group.

</td></tr><tr><td>

Group members

</td><td>

Users assigned to the owning group.

</td></tr><tr><td>

Groups

</td><td>

Groups assigned to the owning group.**Note:** Any groups assigned to the parent group are automatically assigned to the owning group.

</td></tr><tr><td>

Skills

</td><td>

HR skills assigned to the owning group.**Note:** Any HR skills assigned to the parent group are automatically assigned to the owning group.

</td></tr></tbody>
</table>6.  Click **Update**.


**Parent Topic:**[Configure the supporting components for a lifecycle event](../concept/configure-supporting-components-for-lifecycle-event.md)

