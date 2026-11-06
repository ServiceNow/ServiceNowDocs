---
title: Enhanced security model features for incident tables
description: Help prevent unauthorized access to incident-related tables using Deny-Unless access control lists \(ACLs\). A Deny-Unless authentication ACL restricts access for a non-authenticated user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/comp-instal-itsm-enhanced-sec-features.html
release: australia
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Enhanced security model features for incident tables]
breadcrumb: [Reference, Incident Management, IT Service Management]
---

# Enhanced security model features for incident tables

Help prevent unauthorized access to incident-related tables using Deny-Unless access control lists \(ACLs\). A Deny-Unless authentication ACL restricts access for a non-authenticated user.

The enhanced security model implements Deny-Unless ACLs to restrict access for a non-authenticated user, such as a public role user. Without access, the user can't perform any actions on incident-related tables, including reading, writing, deleting, creating, or accessing the report view. This model helps restrict access to the incident tables to authorized or approved user roles. For more information on Deny-Unless ACLs, see [Deny-Unless ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/acl-denial-behavior.md).

This model is activated by default and applies to the following incident-related tables.

<table id="table_uzx_dfs_ydc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incident KCS Article\[kb\_template\_incident\_kcs\_article\]

</td><td>

Stores knowledge articles created from the Incident KCS template.

</td></tr><tr><td>

Incident KCS Template\[kb\_template\_incident\_kcs\_template\]

</td><td>

Stores knowledge templates created from the Incident KCS template.

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

The Incident task \[incident\_task\] table is a child of the Task \[task\] table and inherits all the incident task details.

</td></tr><tr><td>

Task CI\[task\_ci\]

</td><td>

The Task CI \[task\_ci\] table is extended from the Task \[task\] table and contains all the affected CI details.

</td></tr><tr><td>

Task outage\[task\_outage\]

</td><td>

The Task outage \[task\_outage\] table maintains the mapping between the Task \[task\] table and the Outage \[cmdb\_ci\_outage\] table.

</td></tr></tbody>
</table>**Note:** For new or zBoot instances, the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin is installed automatically.

The ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin can be installed and activated by an administrator through a support request. Existing or upgrade users must test and evaluate the results in their non-production instance and then install the plugin and implement the security change in their production instance. For more information, see [Activate ITSM Enhanced Security Features for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/activate-itsm-enhanced-security-inci-mangmnt.md).

-   **[Activate ITSM Enhanced Security Features for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/activate-itsm-enhanced-security-inci-mangmnt.md)**  
Help prevent unauthorized access to incident-related tables by activating the ITSM Enhanced Security Features plugin \(com.snc.itsm.enhanced\_security\), which uses deny unless authenticated access control lists \(ACLs\).

**Parent Topic:**[Incident Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/reference-section-for-incident-management.md)

