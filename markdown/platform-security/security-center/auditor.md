---
title: Auditor checks
description: Use the Auditor suite to SecureCheck to detect misconfiguration that can impact the security posture of your instance.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Scan suites, Security scanner, Security configuration console, Security Center, Platform Security]
---

# Auditor checks

Use the Auditor suite to SecureCheck to detect misconfiguration that can impact the security posture of your instance.

The Auditor suite is provided as an update set. You can use this suite within [Security Center](../concept/sec-center-v2.md). Confirm that Security Center is activated on your instance if you’re using Utah or earlier.

## Import the update set

Administrators can download the update set from support.servicenow.com using this link: [https://support.servicenow.com/sys\_attachment.do?sys\_id=821e1e724732969077748d01426d4393](https://support.servicenow.com/sys_attachment.do?sys_id=821e1e724732969077748d01426d4393).

Commit the update set using the steps detailed in [Commit an update set](https://www.servicenow.com/docs/access?context=t_CommitAnUpdateSet&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

Once the update set has been committed, you can access the Auditor suite at **All** &gt; **Security Center** &gt; **Scanner** &gt; **Suites**.

## Check information

<table id="table_ez5_r21_qcc"><thead><tr><th>

Check Name

</th><th>

Description

</th><th>

Scan finding type

</th></tr></thead><tbody><tr><td>

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

Review allowed JavaScript libraries

</td><td>

Identifies scripts where JavaScript Content Access Control is used to allow or deny specific third-party JavaScript libraries.

 Review instance customizations to verify that libraries aren’t in use before blocking access. The JavaScript Content provider Access Tracking \[sys\_js\_content\_provider\_access\_tracking\] table can be reviewed to see the last date that the library was accessed.

 **Note:** This check can be ignored in instances initially provisioned on Tokyo or later. Records on the associated table have deny rules set by default. In instances initially provisioned prior to Tokyo, there may be allow rules in the JavaScript Access Control tables.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Review client callable script includes with no corresponding ACL

</td><td>

Identifies client callable script includes that don’t have a corresponding ACL. These scripts use the default \("\*"\) client callable script include ACL.

 For these scripts, create ACLs that defines the appropriate criteria for access to verify that only expected users can interact with the functionality provided.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Review custom tables with record producers and no business rule

</td><td>

Identifies record producers that don’t have additional server-side validation. This check identifies custom tables with a Record Producer but without an associated business rule.

 These may enable users to submit unexpected data into the associated table.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Review empty ACLs

</td><td>

Identifies ACL records which have no script, condition, security attribute, or role, or ACLs with the **public** role.

 Leaving ACLs empty or using the **public** role provides open access to any content protected by this ACL.

</td><td>

Resolution Recommended

</td></tr><tr><td>

Review fields with HTML Sanitization disabled

</td><td>

Identifies HTML fields where [HTML Sanitization](../../security/concept/c_HTMLSanitizer.md) is inactive.

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

Identifies IP Address Access Control Ranges that contain a large number of IP Addresses.

 **Note:**

If you’re seeing a large number of false positives, consider adjusting the largestExpectedCIDRBlock variable for your specific business needs.

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

Review public knowledge base articles

</td><td>

Identifies knowledge bases and knowledge base Articles configured to enable access to unauthenticated users.

 Review and confirm that the current configuration aligns with your business needs.

</td><td>

Review and Decide

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

Securing record producers

</td><td>

Identifies insecure record producers.

 If not assigned to appropriate roles unauthorized users can access them, potentially revealing sensitive information. Assign appropriate roles to record producers to verify that they’re accessible only to users that need them.

</td><td>

Resolution Recommended

</td></tr><tr><td>

UI action visibility

</td><td>

Identifies UI actions that can be accessed by a user with no roles who doesn’t have read access to the table.

 These users may be able to alter data on a table they don’t have access to via these UI actions. Verify that UI actions are only available to users with access to the table they affect.

</td><td>

Resolution Recommended

</td></tr></tbody>
</table>**Parent Topic:**[Scan suites](../concept/sec-center-suites.md)

