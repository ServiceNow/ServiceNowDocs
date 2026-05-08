---
title: Features of enhanced security model adoption for incident tables
description: Help prevent unauthorized access to incident-related tables using Deny-Unless ACLs. A Deny-Unless authentication ACL restricts access for a non-authenticated user.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference section for Incident Management, Incident Management, IT Service Management]
---

# Features of enhanced security model adoption for incident tables

Help prevent unauthorized access to incident-related tables using Deny-Unless ACLs. A Deny-Unless authentication ACL restricts access for a non-authenticated user.

The enhanced security model implements Deny-Unless ACLs to restrict access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on incident-related tables, including reading, writing, deleting, creating, or accessing the report view. This ensures that only authorized or approved user roles can access the incident tables. For more information on Deny-Unless ACLs, see Deny-Unless ACL.

This model is activated by default and applicable on the following incident-related tables:

<table id="table_uzx_dfs_ydc"><thead><tr><th>

Tables

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incident KCS Article\[kb\_template\_incident\_kcs\_article\]

</td><td>

The table is used to store knowledge articles created from the Incident KCS template.

</td></tr><tr><td>

Incident KCS Template\[kb\_template\_incident\_kcs\_template\]

</td><td>

The table is used to store knowledge templates created from the Incident KCS template.

</td></tr></tbody>
</table>This model is applicable on the following incident-related tables after installing the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin:

<table id="table_uly_yfs_ydc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incident\[incident\]

</td><td>

The Incident table is extended from the Task \[task\] table. It inherits all the fields, rules, and policies from the Task table.

</td></tr><tr><td>

Incident task\[incident\_task\]

</td><td>

The incident task \[incident\_task\] table is a child of the task \[task\] table and inherits all the incident task details.

</td></tr><tr><td>

Task CI\[task\_ci\]

</td><td>

The Task CI \[task\_ci\] table is extended from the Task \[task\] table and contains all the affected CI details.

</td></tr><tr><td>

Task outage\[task\_outage\]

</td><td>

The Task-Outage table \[task\_outage\] maintains the mapping between the Task \[task\] table and the Outage \[cmdb\_ci\_outage\] table.

</td></tr></tbody>
</table>**Note:** For new or zboot instances, the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin is auto installed.

The ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin can be installed and activated by an admin via a support request. Existing or upgrade users must test and evaluate the results in their non-production instance and then install the plugin and implement the security change in their production instance. For more information, see [Activate ITSM Enhanced Security Features for Incident Management](../task/activate-itsm-enhanced-security-inci-mangmnt.md).

-   **[Activate ITSM Enhanced Security Features for Incident Management](../task/activate-itsm-enhanced-security-inci-mangmnt.md)**  
Prevent unauthorized access to incident-related tables using deny unless authenticated ACLs by activating the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin.

**Parent Topic:**[Reference section for Incident Management](reference-section-for-incident-management.md)

