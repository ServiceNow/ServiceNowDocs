---
title: Exploring Identity and Access Audit
description: Use Identity and Access Audit to understand changes made to users, groups, roles, and ACLs.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Identity and Access Audit, Identity]
---

# Exploring Identity and Access Audit

Use Identity and Access Audit to understand changes made to users, groups, roles, and ACLs.

Identity and Access Audit helps to understand the critical information about who has modified what, where and when in user accounts, groups and roles.

This feature helps identify malicious users, monitor unusual activity within your ServiceNow instance, and maintain compliance by tracking changes to access permissions.

Identity and Access Audit \(Identity Security Audit\) is a plugin \(`com.glide.security.audit`\), which is auto-installed.

It can be turned on or off by toggling the `glide.identity.security.audit.enabled` system property. By default, the property is set `true`.

Identity and Access Audit enables you to:

-   View the changes made in the last 30 days to users, groups, role ACL attributes, role memberships, group memberships, and ACL roles.​
-   Track the changes in your ServiceNow instance.
-   Help mitigate potential security and regulatory risks.
-   Demonstrate compliance to auditors across different organizational groups.
-   Demonstrate that the organization is protected against threats caused by limited visibility into user group and role changes.

## User personas in Identity Access and Audit

There are two different user personas in Identity and Access Audit \(identity\_access\_audit\_viewer\):

-   **role\_viewer** and **group\_viewer​**: View audit records and configuration.​
-   **Security Admin**: View the audit trails. Enable or disable auditing for specific tables or fields.

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

## Identity and Access Audit Modules

Identity and Access Audit's modules include:

|Module|Description|
|------|-----------|
|Audit Results|Displays audits that occurred in the ServiceNow instance.|
|Configure Table &amp; Fields|Configure system tables and fields with available fields from Identity and Access Audit.|
|Configure Retention Period|Configure the retention period for audited data. The maximum period is 30 days.|
|User Trails|Displays audits of users.|
|Group Trails|Displays audits of groups.|
|Role Trails|Displays audits of roles.|
|ACL Trails|Displays audits of ACLs.|

