---
title: Configure case and task roles and permissions
description: Assign roles to store associates, managers, and area managers to grant access to create, edit, and close cases and tasks in the quick case creation feature.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/t\_configure-instore-ops-roles.html
release: brazil
topic_type: task
last_updated: "2026-07-15"
reading_time_minutes: 1
keywords: [configure roles, assign roles, access control, ACL, in-store operations]
breadcrumb: [Configure, Retail]
---

# Configure case and task roles and permissions

Assign roles to store associates, managers, and area managers to grant access to create, edit, and close cases and tasks in the quick case creation feature.

## Before you begin

Role required: Administrator or System Security Administrator

## About this task

The quick case creation feature uses three primary roles that gate access to case and task operations. Area/Region Managers have restricted assignment capabilities.

## Procedure

1.  In the ServiceNow workspace, navigate to **System Security** &gt; **Users and Groups** &gt; **Users**.

2.  Select a user to configure.

3.  In the **Roles** section, add one or more of the following roles:

    |Role|Capabilities|
    |----|------------|
    |**`sn_rtl_instore_ops.associate`**|Create cases, create tasks, and work on assigned tasks. Cannot reassign or close cases/tasks. Store field is auto-populated and read-only.|
    |**`sn_rtl_instore_ops.manager`**|Create cases, create and close tasks, reassign cases and tasks, and view all cases in their store. Can close cases and tasks.|
    |**`sn_rtl_instore_ops.plan_author`**|Create cases and tasks originating from task plan templates. Used for workflow automation.|

4.  For Area/Region Managers, add the `sn_rtl_instore_ops.associate` role.

    **Note:** Area/Region Managers can create cases and be assigned to tasks, but they cannot be assigned to tasks via the task form. They also have required-field visibility for the Store field when reporting issues for multiple stores.

5.  Save the user record.

6.  Repeat for all users who need access to the quick case creation feature.


## Role assignment examples

-   **Store Associate:** Assign `sn_rtl_instore_ops.associate`
-   **Store Manager:** Assign `sn_rtl_instore_ops.manager` \(manager role includes associate capabilities\)
-   **Area Manager:** Assign `sn_rtl_instore_ops.associate` \(can create cases across multiple stores\)
-   **Automation User:** Assign `sn_rtl_instore_ops.plan_author` \(for template-originated cases\)

