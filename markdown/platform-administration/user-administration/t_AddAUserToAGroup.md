---
title: Add a user to a group
description: Add a user to a group so that the user inherits all the roles assigned to the group.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating groups, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Add a user to a group

Add a user to a group so that the user inherits all the roles assigned to the group.

## Before you begin

Role required: user\_admin

## About this task

If you’re a non-admin user, you can’t add a user to a group that contains the admin role. Likewise, if you don’t have a security\_admin role, you can’t add a user to a group that contains the security\_admin role.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Select a group **Name**.

3.  In the **Group Members** related list, select **Edit**.

4.  Select one or more names in the **Collection** list.

5.  Select **Add** and **Save**.

6.  Remove a user from a group when they change roles.

    1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

    2.  Select a group **Name**.

    3.  In the **Group Members** related list, select the check box next to each group member name you want to remove.

    4.  From the **Actions on selected rows** menu, select **Delete**.

        **Note:** Before selecting **Delete**, first make sure you have properly selected the rows containing the users you want to remove from the group.


**Parent Topic:**[Creating groups](../../roles/concept/ua-creating-groups.md)

