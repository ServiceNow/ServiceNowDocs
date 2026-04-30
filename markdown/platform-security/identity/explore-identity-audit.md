---
title: Explore Identity and Access Audit
description: Use the Identity and Access Audit to understand changes made for users, groups, roles, and ACLs.
locale: en-US
release: zurich
product: Identity
classification: identity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Identity and Access Audit, Identity]
---

# Explore Identity and Access Audit

Use the Identity and Access Audit to understand changes made for users, groups, roles, and ACLs.

Identity and Access Audit helps to understand the critical information about who has modified what, where and when in user accounts, groups and roles.

Helps to detect malicious users and track unusual activity in the ServiceNow® instance and adhere with compliance standards of being able to track access changes.

Identity and Access Audit \(Identity Security Audit\) is a plugin \(`com.glide.security.audit`\), which is auto-installed.

Auditing feature can be turned on or off by toggling the`glide.identity.security.audit.enabled` system property. By default, the property is set `true`.

Identity and Access Audit enables you to:

-   View the changes made in the last 30 days to users, groups, role ACL attributes, role memberships, group memberships, and ACL roles.​
-   Track the changes in your ServiceNow instance.
-   Help mitigate potential security and regulatory risks.
-   Demonstrate compliance with auditors for different groups within the organization.
-   Demonstrate that the organization isn’t vulnerable to threats related to a lack of visibility in the user group and role changes.

## User personas in Identity Access and Audit

Following are the different user personas in Identity and Access Audit:

-   **Admin**​: View the audit records and the configuration.​
-   **Security Admin**: View these audit trails. Modify the configuration to enable or disable auditing for a certain table or modify the fields that are being audited.

## Audit Tables

The following tables can be audited using Identity and Access Audit​:

-   Group \[sys\_user\_group\]​
-   Role \[sys\_user\_role\]​
-   Access Control \[sys\_security\_acl\]​
-   User \[sys\_user\]​
-   Group Role \[sys\_group\_has\_role\]​
-   User Role \[sys\_user\_has\_role\]​
-   Access Roles \[sys\_security\_acl\_role\]​
-   Contained Role \[sys\_user\_role\_contains\]​
-   Group Member \[sys\_user\_grmember\]​

## Modules in Identity and Access Audit

Identity and Access Audit has the following modules on the ServiceNow instance:

|Module|Description|
|------|-----------|
|Audit Results|Displays the audits that occurred in the ServiceNow instance.|
|Configure Table &amp; Fields|Configure the system tables and fields with the available fields from the Identity and Access Audit.|
|Configure Retention Period|Configure the retention period of the audited data. The maximum period that can be set is 30 days.|
|User Trails|Displays audits of users.|
|Group Trails|Displays audits of groups.|
|Role Trails|Displays audits of roles.|
|ACL Trails|Displays audits of ACLs.|

