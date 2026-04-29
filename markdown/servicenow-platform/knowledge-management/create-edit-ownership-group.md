---
title: Manage ownership groups
description: Create ownership groups and associate them to knowledge articles. Knowledge group managers or knowledge administrators can edit ownership groups.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Manage ownership groups

Create ownership groups and associate them to knowledge articles. Knowledge group managers or knowledge administrators can edit ownership groups.

## Before you begin

The Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) must be activated.

Role required: Users with the knowledge\_domain\_expert or knowledge\_admin roles can create ownership groups.

Users with the knowledge\_group\_manager or knowledge\_admin roles can edit ownership groups.

## About this task

Create an ownership group by adding members and a manager. Knowledge administrators approve ownership groups.

When knowledge articles are created, ownership groups can be associated to them. Ownership groups manage article approvals and feedback and can edit and retire knowledge articles that they are associated with.

Knowledge group managers can edit ownership groups managed by them by adding or removing members without the need for approval. They cannot change the manager assigned in their groups. Only knowledge administrators can reassign managers.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Ownership Groups** &gt; **Manage Group**.

2.  To create an ownership group, from the Request Type list, select **Create Ownership Group**.

    **Note:** To edit an existing ownership group, from the Request Type list, select **Edit Ownership Group**.

3.  Fill in the fields on the form.

<table id="table_ysd_btl_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the ownership group.

</td></tr><tr><td>

Group email

</td><td>

An email address for the ownership group. Emails are sent to group members in these cases.-   Activity on articles they are associated with, for example, comments.
-   Article quality checks \(AQI\) performed on articles they are associated with.

If no group email is defined, emails are sent to individual group member emails.

</td></tr><tr><td>

Description

</td><td>

Description that defines the ownership group.

</td></tr><tr><td>

Manager

</td><td>

Manager for the ownership group.

</td></tr><tr><td>

Group members

</td><td>

Members of the ownership group.

</td></tr></tbody>
</table>4.  Click **Order Now**.

    The ownership group is sent to the knowledge administrator for approval. Once approved, the ownership group is ready to use and associate to a knowledge article.

    **Note:** You can also create an ownership group from an existing group.

    1.  Navigate to **System Security** &gt; **Users and Groups** &gt; **Groups**.
    2.  Click a group.
    3.  In the **Type** field, enter `Knowledge`.

        **Note:** If the **Type** field does not appear on the form, configure the form layout to add it.

    4.  In the **Manager** field, enter a manager and add the role knowledge\_group\_manager.
    5.  In the Roles related list, click **Edit** and add the role knowledge\_group\_member to the group.

**Parent Topic:**[Using Knowledge Management](../concept/using-knowledge-management.md)

