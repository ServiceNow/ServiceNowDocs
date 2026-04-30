---
title: User hierarchy access control for issue and remediation task records
description: If a user is assigned to an issue or a remediation task, then the manager of the user and the manager above in the hierarchy also get access to the issue or remediation task record.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manually create GRC issues, Manage issues in Policy and Compliance Management, Use the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# User hierarchy access control for issue and remediation task records

If a user is assigned to an issue or a remediation task, then the manager of the user and the manager above in the hierarchy also get access to the issue or remediation task record.

The user reference in the **Assigned to** field, **Opened by** field, or **Owner** field are configurable in the User hierarchy configurations \[sn\_grc\_user\_hierarchy\_configuration\] table. Therefore, you can configure the fields in the table and enter the user reference, for example **Assigned to** or **Issue Manager** as User reference field 1 or User reference field 2. However, you can configure only two fields in a table.

The manager of the user in the user reference field and the manager above in the hierarchy can be configured as User hierarchy field 1 and User hierarchy field 2, respectively. If one of them is no longer the manager of the user in the user reference field, then that user in the hierarchy loses access to the record. You can view the hierarchy of users in the User Hierarchy \[sn\_grc\_user\_hierarchy\] table.

The prerequisites to enable user hierarchy access control are:

-   Users in the hierarchy must have at least the GRC business user \(sn\_grc.business\_user\) role.
-   The **sn\_grc.enable\_user\_hierarchy\_access\_control** system property must be set as **true**.

The concept of user hierarchy is helpful as it provides more visibility to the users in the hierarchy in tracking its completion when it is assigned to a user in a team. User hierarchy fields are not visible in the Issue or Remediation task form, however internally this feature enables you to restrict access to records based on those users in the hierarchy who can access them.

**Parent Topic:**[Manually create GRC issues](../../grc-common/task/t_CreateAnIssue.md)

