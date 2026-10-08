---
title: Configure case and task roles and permissions
description: Assign roles to store associates, managers, and area managers to grant access to create, edit, and close cases and tasks in the quick case creation feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/t\_configure-instore-ops-roles.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 1
keywords: [configure roles, assign roles, access control, ACL, in-store operations]
breadcrumb: [Configure, Retail]
---

# Configure case and task roles and permissions

Assign roles to store associates, managers, and area managers to grant access to create, edit, and close cases and tasks in the quick case creation feature.

## Before you begin

Role required: Administrator or System Security Administrator

## About this task

Quick case and task creation uses three roles, one for each persona: store associate, store manager, and area or region manager. Users also need to be mapped to the stores they work with.

## Procedure

1.  In the ServiceNow workspace, navigate to **System Security** &gt; **Users and Groups** &gt; **Users**.

2.  Select a user to configure.

3.  In the **Roles** section, add one or more of the following roles:

    |Role|Capabilities|
    |----|------------|
    |**`sn_rtl_instore_ops.associate`**|Store associate. Create cases, add tasks, assign and reassign cases and tasks, use **Assign to me**, and edit and close cases and tasks for their store. The store is set automatically on new cases.|
    |**`sn_rtl_instore_ops.manager`**|Store manager. Contains the `sn_rtl_instore_ops.associate` role, so store managers can do everything store associates can.|
    |**`sn_rtl_instore_ops.manager_contributor`**|Area or region manager. Create cases for any store they're mapped to, add tasks, and edit and close cases and tasks across those stores. Can't assign cases or tasks or use **Assign to me**.|

4.  For area and region managers, add the `sn_rtl_instore_ops.manager_contributor` role.

    Users who already have the `sn_retail.manager_contributor` role get `sn_rtl_instore_ops.manager_contributor` automatically, because the retail role contains it.

5.  Save the user record.

6.  Repeat for all users who need access to the quick case creation feature.


## Role assignment examples

-   **Store Associate:** Assign `sn_rtl_instore_ops.associate`
-   **Store Manager:** Assign `sn_rtl_instore_ops.manager` \(manager role includes associate capabilities\)
-   Area or region manager: Assign `sn_rtl_instore_ops.manager_contributor` \(can create and monitor cases across multiple stores\)

