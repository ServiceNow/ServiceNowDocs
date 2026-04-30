---
title: ITSM Enhanced Security Features for Change Management
description: Help prevent unauthorized access to change-related tables using deny-unless ACLs. A deny-unless authentication ACL restricts access for a non-authenticated user.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference section for Change Management, Change Management, IT Service Management]
---

# ITSM Enhanced Security Features for Change Management

Help prevent unauthorized access to change-related tables using deny-unless ACLs. A deny-unless authentication ACL restricts access for a non-authenticated user.

The enhanced security model implements deny-unless ACLs to restrict access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on change-related tables, including reading, writing, deleting, or creating. This ensures that only authorized or approved user roles can access the change tables. For more information on deny-unless ACLs, see [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

This model is applicable on the following change-related tables after installing the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin:

<table id="table_frx_qsj_c2c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Change request\[change\_request\]

</td><td>

The change request table is extended from the Task \[task\] table. It inherits all the fields, rules, and policies from the Task table.

</td></tr><tr><td>

Change task\[change\_task\]

</td><td>

The change task table is a child of the task \[task\] table and inherits all the change request task details.

</td></tr></tbody>
</table>**Note:** For new or zboot instances, the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin is automatically installed.

The ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin can be installed and activated by an admin via a support request. Existing or upgrade users must test and evaluate the results in their non-production instance and then install the plugin and implement the security change in their production instance. For more information, see [Activate ITSM Enhanced Security Features for Change Management](../task/activate-itsm-enhanced-security-change.md).

-   **[Activate ITSM Enhanced Security Features for Change Management](../task/activate-itsm-enhanced-security-change.md)**  
Prevent unauthorized access to change-related tables using deny-unless ACLs by activating the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin.

**Parent Topic:**[Reference section for Change Management](../concept/reference-change-management.md)

