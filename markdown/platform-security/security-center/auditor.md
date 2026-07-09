---
title: Security Center Scan Suites
description: Use the Auditor suite to SecureCheck to detect misconfiguration that can impact the security posture of your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/security-center/auditor.html
release: australia
product: Security Center
classification: security-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Scan suites, Security scanner, Security configuration console, Security Center, Platform Security]
---

# Security Center Scan Suites

Use the Auditor suite to SecureCheck to detect misconfiguration that can impact the security posture of your instance.

## Security Center Scan Suites

Security Center provides 4 scan suites that provide schedules to run checks at different cadences. The suites are:

-   Security Center- daily
-   Security Center- weekly
-   Security Center- monthly
-   Security Center- quarterly

You can add custom checks to these suites to automatically perform on the respective cadence.

## Check information

<table id="table_ez5_r21_qcc"><thead><tr><th>

Cadence

</th><th>

Check Name

</th><th>

Description

</th><th>

Scan finding type

</th></tr></thead><tbody><tr><td rowspan="8">

Daily

</td><td>

Review public knowledge base articles

</td><td>

Identifies knowledge bases and knowledge base Articles configured to enable access to unauthenticated users.

 Review and confirm that the current configuration aligns with your business needs.

</td><td>

Review and Decide

</td></tr><tr><td>

Review public knowledge bases

</td><td>

Identifies public Knowledge Bases to be reviewed for confirmation that the current configuration aligns with your business needs.

</td><td>

Review and Decide

</td></tr><tr><td>

Users with Direct Role Assignments \(Bypassing Groups\)

</td><td>

Identifies users with roles assigned directly instead of through group inheritance. Direct assignments reduce visibility and complicate access audits — group-based access is preferred for governance.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Inactive Users with Assigned Roles

</td><td>

Identifies user accounts that are inactive but still holds active role assignments. These should be reviewed and removed to prevent unauthorized access via dormant accounts.

</td><td>

Resolution Recommended

</td></tr><tr><td>

External users with access to classified data

</td><td>

External users are typically given limited access using the snc\_external role. This external user currently has access to one or more classified or sensitive data tables/fields. Such access is needs to be reviewed for external accounts and may result in unauthorized data exposure.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Access controls on Tables

</td><td>

Checks for tables without ACLs.

</td><td>

Tables should be secured with ACLs. Access to data stored in tables should be limited only to users that need it.

</td></tr><tr><td>

Access controls on UI pages

</td><td>

Checks for UI Pages that aren't secured by ACLs.

</td><td>

Without an ACL securing access to a UI Page, that UI Page is accessible to all logged-in internal users. Without any restrictions logged-in users can potentially make unauthorized changes.

</td></tr><tr><td>

Access Controls on Client callable Script Includes

</td><td>

Checks for client-callable script includes that aren't secured by ACLs.

</td><td>

All client callable script includes should be secured with an ACL using required roles.

</td></tr><tr><td rowspan="3">

Weekly

</td><td>

Review client callable script includes with no corresponding ACL

</td><td>

Identifies client callable script includes that don’t have a corresponding ACL. These scripts use the default \("\*"\) client callable script include ACL.

 For these scripts, create ACLs that defines the appropriate criteria for access to verify that only expected users can interact with the functionality provided.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Dormant user account

</td><td>

Identified active users with no activity in a certain time frame is considered a dormant user. Dormant accounts without proper review can lead to unmanaged, fragmented, or untracked access risks.This flagged user has not logged into the system for configured time frame.

</td><td>

Resolution Recommended

</td></tr><tr><td>

User Account shouldn't have both internal and external roles

</td><td>

Checks for user records with both internal and external roles assigned.

</td><td>

Internal user roles are intended for users within your company. External user roles are intended for external personnel, such as customers and partners.

</td></tr><tr><td rowspan="19">

Monthly

</td><td>

Review custom tables with record producers and no business rule

</td><td>

Identifies record producers that don’t have additional server-side validation. This check identifies custom tables with a Record Producer but without an associated business rule.

 These may enable users to submit unexpected data into the associated table.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Review fields with HTML Sanitization inactive

</td><td>

Identifies HTML fields where [HTML Sanitization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_HTMLSanitizer.md) is inactive.

 HTML sanitization removes or replaces potentially harmful elements and attributes within HTML code. Review HTML fields where sanitization is inactive to confirm whether this configuration is necessary.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Review inactive security feature plugins

</td><td>

Identifies plugins that aren’t activated that provide additional, configurable security controls. The findings produced by this check are provided for informational purposes.

 Before enabling one of the identified plugins, verify that the plugin meets your use cases or requirements. You can mute these findings if you don't have a use case for the identified.

</td><td>

Inform

</td></tr><tr><td>

Review large allowed IP address ranges

</td><td>

Identifies IP Address Access Control Ranges that contain many IP Addresses.

 **Note:**

If you’re seeing many false positives, consider adjusting the largestExpectedCIDRBlock variable for your specific business needs.

Classless Inter-Domain Routing \(CIDR\) blocks contain a larger amount of IP addresses as the number decreases. For example, the CIDR block size 8 is larger \(contains more IP addresses\) than the CIDR block size 16.

 Review and confirm that the current configuration aligns with your business needs.

</td><td>

Review and Decide

</td></tr><tr><td>

Review public GraphQL schemas

</td><td>

Identifies public GraphQL schemas in the GraphQL API \[sys\_graphql\_schema\] table.

 These schemas can be configured to be available without authentication. Depending on the endpoint's functionality, this may allow unauthenticated users to perform unexpected actions or interact with unexpected data.

</td><td>

Review and Decide

</td></tr><tr><td>

Identify out of date store apps

</td><td>

Identifies apps activated on your instance that have updated versions available.

 Verify you’re running to the most up-to-date versions of store applications, which can include fixes to potential security issues.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Insecure GlideRecord calls

</td><td>

Identifies scripts that are directly invokable by end users \(such as Client-Callable Script Includes, Widgets, Processors, REST Endpoints\)

 These scripts should respect ACLs and use GlideRecordSecure or GlideRecord with canRead, canWrite, canCreate, canDelete.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Review public REST API endpoints

</td><td>

Identifies Rest API Endpoints in the Scripted REST Resource \[sys\_ws\_operation\] table that are configured to be available without authentication.

 Depending on the endpoint's functionality, this may allow unauthenticated users to perform unexpected actions or interact with unexpected data.

</td><td>

Review and Decide

</td></tr><tr><td>

Review public Service Portal pages

</td><td>

Identifies Service Portal pages that are made public. Service Portal pages are made available to unauthenticated users by setting the "public" field to "true."

 Review and confirm that the current configuration aligns with your business needs.

</td><td>

Review and Decide

</td></tr><tr><td>

Review public UI Pages

</td><td>

Identifies UI Pages that are made public. UI Pages can be made available to unauthenticated users using the \[sys\_public\] page.

 Review and confirm that the current configuration aligns with your business needs.

</td><td>

Review and Decide

</td></tr><tr><td>

Review roles that contain the 'admin' role

</td><td>

Identifies any roles \(Roles \[sys\_user\_role\] table\) that contains the **admin** role.

 The **admin** role grants users administrative privileges and should be used only when necessary. Review and confirm that the current configuration aligns with your business needs. If this is an intentional configuration, this check can be muted.

</td><td>

Review and Decide

</td></tr><tr><td>

Review UI Pages without corresponding ACLs

</td><td>

Identifies UI Pages that don’t have an ACL for that UI Page.

 UI Pages that don’t have a specific ACL default to a generic UI Page ACL, which may grant access to unintended users.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Review users with valid local passwords

</td><td>

Identifies users with locally set passwords.

 Users with local passwords may interact with the instance via APIs using the local credentials, even if local logins are disallowed. This password configuration is needed for integration user accounts to function correctly.

 Review these user accounts to verify that only intended users \(such as integration accounts\) can authenticate with local authentication.

</td><td>

Review and Decide

</td></tr><tr><td>

Rotate passwords stored with outdated hashing algorithms

</td><td>

Identifies user accounts with passwords created in previous versions of the ServiceNow AI Platform, which may have used what is now considered a legacy or outdated hashing algorithm.

 Accounts created on old platform versions that haven’t rotated their passwords may still have passwords stored with a legacy hashing algorithm. Review the identified accounts created consider password resets.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Review public REST API endpoints

</td><td>

Identifies Rest API Endpoints in the Scripted REST Resource \[sys\_ws\_operation\] table that are configured to be available without authentication.

 Depending on the endpoint's functionality, this may allow unauthenticated users to perform unexpected actions or interact with unexpected data.

</td><td>

Review and Decide

</td></tr><tr><td>

UI action visibility

</td><td>

Identifies UI actions that can be accessed by a user with no roles who doesn’t have read access to the table.

 These users may be able to alter data on a table they don’t have access to via these UI actions. Verify that UI actions are only available to users with access to the table they affect.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Publicly accessible knowledge base and articles

</td><td>

Checks for publicly accessible knowledge bases and knowledge base articles

</td><td>

Publicly accessible knowledge bases and articles are visible to all users in the instance. Increase security by limiting knowledge bases and articles to the specific audience that needs them.

</td></tr><tr><td>

Can Contribute / Cannot Contribute user criteria to be defined on each knowledge

</td><td>

Checks for knowledge base records that don't have Can Contribute or Cannot Contribute user criteria defined.

</td><td>

Each knowledge base should have either Can Contribute or Cannot Contribute user criteria defined. Otherwise, any user can contribute content to a knowledge base with no Contribute criteria defined.

</td></tr><tr><td>

All Processors of type - SCRIPT must be protected with CSRF Token

</td><td>

Checks for Processors with the SCRIPT type that aren't protected with a CSRF token.

</td><td>

All Processors with the SCRIPT type should be protected with a Cross-site Request Forgery \(CSRF\) token. These processors should have the CSRF option checked, which prohibits the processor from running unless the instance uses a CSRF token.

</td></tr><tr><td rowspan="3">

Quarterly

</td><td>

Review allowed JavaScript libraries

</td><td>

Identifies scripts where JavaScript Content Access Control is used to allow or deny specific third-party JavaScript libraries.

 Review instance customizations to verify that libraries aren’t in use before blocking access. The JavaScript Content provider Access Tracking \[sys\_js\_content\_provider\_access\_tracking\] table can be reviewed to see the last date that the library was accessed.

 **Note:** This check can be ignored in instances initially provisioned on Tokyo or later. Records on the associated table have deny rules set by default. In instances initially provisioned before Tokyo, there may be allow rules in the JavaScript Access Control tables.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Securing record producers

</td><td>

Identifies insecure record producers.

 If not assigned to appropriate roles unauthorized users can access them, potentially revealing sensitive information. Assign appropriate roles to record producers to verify that they’re accessible only to users that need them.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Deactivated security controls

</td><td>

Identifies new Security Controls that have been introduced, but could impact to your instance. This is flagged to enable you to review the security control and test it against your instances before activating it.

</td><td>

Resolution Recommended

</td></tr></tbody>
</table>**Parent Topic:**[Scan suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sec-center-suites.md)

