---
title: Components installed with Employee Document Management
description: Several types of components install with the activation of the Employee Document Management \[com.sn\_employee\_document\_management\] plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: zurich
product: Employee Document Management
classification: employee-document-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Employee Document Management, HR Documents, HR Service Delivery, Employee Service Management]
---

# Components installed with Employee Document Management

Several types of components install with the activation of the Employee Document Management \[com.sn\_employee\_document\_management\] plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

**Note:** The Employee Document Management \[com.sn\_employee\_document\_management\] plugin activates the sn\_hr\_ef.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only Employee Document Management admin user by requiring a minimum number \(default is two\) of active users with this role.

## Document management roles and descriptions

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

EF admin \[sn\_hr\_ef.admin\]

</td><td>

Has full control over the Employee Document Management application. Can:-   Access Employee Document Management.
-   Assign Employee Document Management roles.
-   Search and read employee documents.
-   Create and update employee documents.
-   Manage administration of employee documents. Can create, read, and write to the following tables:
    -   Retention Period \[sn\_hr\_ef\_retention\_period\]
    -   Retention Policy \[sn\_hr\_ef\_retention\_policy\]
    -   Security Policy \[sn\_hr\_ef\_security\_policy\]
    -   Document Type \[sn\_hr\_ef\_document\_type\]
-   Manage legal holds on profiles and document types.

**Note:** Contains the HR basic \[sn\_hr\_core.basic\] role that contains the HR profile writer \[sn\_hr\_core.profile\_writer\] role.

-   Administer the Employee Documents Properties.
-   Configure and administer Employee Document Management Bulk Imports.

</td><td>

-   Employee Document Management Reader \[sn\_hr\_ef.document\_reader\]
-   Employee Document Management Writer \[sn\_hr\_ef.document\_writer\]
-   Employee Document Management Legal Hold Writer \[sn\_hr\_ef.legal\_hold\_writer\]
-   Employee Document Management Manager \[sn\_hr\_ef.manager\]
-   HR basic \[sn\_hr\_core.basic\]
-   sn\_hr\_ef.document\_import

</td></tr><tr><td>

Employee Document Management Reader\[sn\_hr\_ef.document\_reader\]

</td><td>

Can:-   Access Employee Document Management.
-   Search and read employee documents.

**Note:** Add this role to the Read access tab on the security policy of the employee document. See [Add or modify document security policies](../concept/hr-doc-management-config.md#).


</td><td>

None

</td></tr><tr><td>

Employee Document Management Writer\[sn\_hr\_ef.document\_writer\]

</td><td>

Can:-   Access Employee Document Management.
-   Search and read employee documents.
-   Create and update employee documents.

 **Note:** Add this role to the Write access tab on the security policy of the employee document. See [Add or modify document security policies](../concept/hr-doc-management-config.md#).

</td><td>

Employee Document Management Reader \[sn\_hr\_ef.document\_reader\]

</td></tr><tr><td>

Employee Document Management Legal Hold Writer\[sn\_hr\_ef.legal\_hold\_writer\]

</td><td>

Can:-   Access Legal Holds to view employee documents on legal hold.
-   Manage legal holds on HR profiles.

**Note:** Requires the HR profile writer \[sn\_hr\_core.profile\_writer\] role. HR profile writer can also create and search for employee documents.

-   Cannot manage legal holds on document types unless combined with the Employee Document Management Manager \[sn\_hr\_ef.manager\] role.

</td><td>

None

</td></tr><tr><td>

Employee Document Management Manager\[sn\_hr\_ef.manager\]

</td><td>

Can:-   Access Employee Document Management.
-   Search and read employee documents.
-   Create and update employee documents.
-   Manage administration of employee documents. Can create, read, and write to the following tables:

    -   Retention Period \[sn\_hr\_ef\_retention\_period\]
    -   Retention Policy \[sn\_hr\_ef\_retention\_policy\]
    -   Security Policy \[sn\_hr\_ef\_security\_policy\]
    -   Document Type \[sn\_hr\_ef\_document\_type\]
**Note:** All default security policies with the base system are part of the sn\_hr\_ef.manager role by default. Provides both read and write capabilities. No roles are automatically part of new security policies.

-   Add or remove legal holds on profiles and document types.

**Note:** Requires the HR profile writer \[sn\_hr\_core.profile\_writer\] role with the Employee File Management Legal Hold Writer \[sn\_hr\_ef.legal\_hold\_writer\] role to place HR profiles on legal hold.


</td><td>

-   Employee Document Management Reader \[sn\_hr\_ef.document\_reader\]
-   Employee Document Management Writer \[sn\_hr\_ef.document\_writer\]
-   Employee Document Management Legal Hold Writer \[sn\_hr\_ef.legal\_hold\_writer\]

</td></tr><tr><td>

Document Import\[sn\_hr\_ef.document\_import\]

</td><td>

Grants access to the Employee Document Management Bulk Import Employee Document Staging \[sn\_hr\_ef\_import\_staging\] table and process flow.

</td><td>

None

</td></tr></tbody>
</table>## Document management scheduled jobs

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clean up inactive employee documents

</td><td>

Deletes uploaded but not submitted employee documents.

</td></tr><tr><td>

EF Bulk Import from Staging - Hourly

</td><td>

Processes up to 100 import staging records in the Ready state. It runs the capture step to upload the attachments and create an employee document.This job picks up 100 records per configuration.

 This job picks up the oldest configurations first regardless of the number of associated staging records. For example:

-   Configuration A has only one staging record created on 11/01/2018 at 8:00 AM.
-   Configuration B has 99 staging records created on 11/01/2018 at 8:05 AM.
-   Configuration A runs first and Configuration B runs in an hour.

</td></tr><tr><td>

Purge employee documents

</td><td>

This job purges employee documents flagged as eligible for purging.

</td></tr><tr><td>

Purge Notification Daily Job

</td><td>

Determines what documents require notification or authorization to purge based on security policy. This job sends an email with a link to the list of documents to all members of the group assigned.

</td></tr><tr><td>

Refresh Purge Dates for Employee Documents

</td><td>

This job ensures that any employee documents that have a changed retention period since the last run does not purge a document.This scheduled job works with the sn\_hr\_ef.purge\_stride\_length property to determine which employee documents for a user \[sys\_user\] record get purge dates recalculated.

</td></tr></tbody>
</table>**Note:** The Employee Document Management scheduled jobs run daily by default. To change when a scheduled job runs, see [Default schedules](https://www.servicenow.com/docs/access?context=r_DefaultSchedules&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Document management tables and descriptions

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attachment Tracking\[sn\_hr\_ef\_attachment\_tracking\]

</td><td>

Tracks copied attachments for purging. Also used to for attachments that get copied to an HR case from an HR task.

</td></tr><tr><td>

Document Type \[sn\_hr\_ef\_document\_type\]

</td><td>

Records about employee document categorization, access, retention policy, and legal holds.

</td></tr><tr><td>

Employee Document\[sn\_hr\_ef\_employee\_document\]

</td><td>

Records about an employee document, document type, purge hold, purge date, employee, tags, size, format, creation date, and created by.

</td></tr><tr><td>

Employee Document Stagingsn\_hr\_ef\_import\_staging

</td><td>

Contains information on employee documents from your source repository. This information maps to elements required for import to Employee Document Management.

</td></tr><tr><td>

Legal Hold \[sn\_hr\_ef\_legal\_hold\]

</td><td>

Records about legal hold placed on either a document type or HR profile.

</td></tr><tr><td>

Purge Log \[sn\_hr\_ef\_purge\_log\]

</td><td>

Configurable by the Employee Documents Properties. Determines what fields appear on the purge logs.

</td></tr><tr><td>

Retention Period \[sn\_hr\_ef\_retention\_period\]

</td><td>

Records about retention periods including date offset type, units, and quantity.

</td></tr><tr><td>

Retention Policy \[sn\_hr\_ef\_retention\_policy\]

</td><td>

Records about retention policies including conditions the policy applies to, retention period, and created by.

</td></tr><tr><td>

Security Policy \[sn\_hr\_ef\_security\_policy\]

</td><td>

Records about security policies including COE, purge authorization, groups, roles, and created by.

</td></tr><tr><td>

Document Type Security Policy\[sn\_hr\_ef\_m2m\_doc\_type\_sec\_policy\]

</td><td>

Associates security policies to a document type.

</td></tr></tbody>
</table>**Parent Topic:**[Employee Document Management reference](../concept/reference-employee-document-management.md)

**Related topics**  


[Properties for Employee Document Management application](employee-doc-properties.md)

