---
title: Configure Tables and Fields
description: Identity and Access Audit to understand the changes made for a user, group, role, and ACL.
locale: en-US
release: zurich
product: Identity
classification: identity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Auditable Fields, Identity and Access Audit, Identity]
---

# Configure Tables and Fields

Identity and Access Audit to understand the changes made for a user, group, role, and ACL.

## Before you begin

Role required: security\_admin

You must elevate your role to Security Admin to configure tables and fields for Identity and Access Audit.

The following tables can be configured for auditing​:

-   Group \[sys\_user\_group\]​
-   Role \[sys\_user\_role\]​
-   Access Control \[sys\_security\_acl\]​
-   User \[sys\_user\]​
-   Group Role \[sys\_group\_has\_role\]​
-   User Role \[sys\_user\_has\_role\]​
-   Access Roles \[sys\_security\_acl\_role\]​
-   Contained Role \[sys\_user\_role\_contains\]​
-   Group Member \[sys\_user\_grmember\]​

**Note:** To understand which fields can be configured for the tables, see [Supported and unsupported fields in Identity Access and Audit](../concept/allowed-fields-for-audit.md).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Identity and Access Audit** &gt; **Configure Tables &amp; Fields**.

2.  Select the table that you want to audit a field from.

    For example, **sys\_user**.

    ![Sys user table](../images/configure-fields.png)

3.  Add the field to be audited.

    For example, **Password**.

    ![Adding password field](../images/configure-tfield-password.png)

    **Note:** The following modifications for the security auditable fields result in more processing time when doing bulk import:

    -   Adding more fields from the available field list for audit.
    -   Enabling additional operations such as create, update, or delete.
4.  Update the record.

    Any changes to the password field add a new record to the Security Table Audits. In this example, the audit shows a changed password field for the user **Abel Tuter**.

    ![New Audit](../images/conf-password-fields.png)

    Selecting the created record displays the details of the changes.

    ![Detail of the audit](../images/confi-fields-result.png)


