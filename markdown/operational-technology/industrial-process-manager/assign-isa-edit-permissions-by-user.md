---
title: Assign ISA Access edit permissions by user
description: Configure access permissions to grant users edit access to Equipment Model entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/assign-isa-edit-permissions-by-user.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 1
keywords: [user access, Equipment Model, granular access control, ISA, permissions]
breadcrumb: [ISA Access by User, Equipment Model entity access control tables, Configure the Industrial Process Manager, Industrial Process Manager, Operational Technology]
---

# Assign ISA Access edit permissions by user

Configure access permissions to grant users edit access to Equipment Model entities.

## Before you begin

Role required: cmdb\_ot\_isa\_admin or admin

## About this task

The Equipment Model entity access control interface lets you manage which users or groups can access specific Equipment Model entities and what actions they can perform. By default, users and groups have read-only access.

## Procedure

1.  Navigate to **All** &gt; **Equipment Model - ISA** &gt; **ISA Access - by User**.

    The Equipment Model Entity User Access page opens, showing a list of users with current access assignments.\[Omitted image "access-level-list.png"\] Alt text: List of access type for users, site, and equipment model entity

2.  On this page, select **New**.

    The new record form opens.

3.  In the **User** field, enter a new user name or select the search icon and select a user from the drop down list.

    \[Omitted image "eme-new-record-user.png"\] Alt text: Select a User

4.  In the **Site** field, select the site for this user's access.

    The a Site selection is required.

5.  When you select a **Site**, the **Equipment model entity** field is displayed.

6.  In the **Equipment model entity** field, select the Search icon.

    The Equipment Model Entities list for the chosen site opens.

7.  Select an entity that is available in the Site.

8.  From the **Access Type** field, select **Edit** from the menu.

    \[Omitted image "can-edit-selection-group-eme.png"\] Alt text: Access type: Edit

9.  Select **Submit**.

    The new record is added to the Equipment Model Entity User Access list and the user now has edit permissions.

10. To modify access for an existing user, select the user from the Equipment Model Entity Group Access list, update the Access Type setting, and select Update.


## Result

The user can now access the Equipment model entity at both the read and edit levels. The user's access is scoped to the selected site and is effective immediately.

**Parent Topic:**[ISA Access by User](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/c-isa-access-by-user.md)

