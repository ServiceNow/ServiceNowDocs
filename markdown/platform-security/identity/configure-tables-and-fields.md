---
title: Configuring Tables and Fields
description: Configure tables and fields for Identity and Access Audit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/identity/configure-tables-and-fields.html
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Auditable Fields, Identity and Access Audit, Identity]
---

# Configuring Tables and Fields

Configure tables and fields for Identity and Access Audit.

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

**Note:** To understand which fields can be configured for the tables, see [Supported and unsupported fields in Identity Access and Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/identity/allowed-fields-for-audit.md).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Identity and Access Audit** &gt; **Configure Tables &amp; Fields**.

2.  Select the table that you want to audit.

    For example, **sys\_user**.

    \[Omitted image "configure-fields.png"\] Alt text: Sys user table

3.  Add one or more fields to be audited.

    For example, **Password**.

    \[Omitted image "configure-tfield-password.png"\] Alt text: Adding password field

    **Note:** The following modifications for the security auditable fields result in more processing time when doing bulk import:

    -   Adding more fields from the available field list for audit.
    -   Enabling additional operations such as create, update, or delete.
4.  Click **Update**.

    Any changes to the password field add a new record to the Security Table Audits. In this example, the audit shows a changed password field for the user **Abel Tuter**.

    \[Omitted image "conf-password-fields.png"\] Alt text: New Audit

    Selecting the created record displays the details of the changes.

    \[Omitted image "confi-fields-result.png"\] Alt text: Detail of the audit


