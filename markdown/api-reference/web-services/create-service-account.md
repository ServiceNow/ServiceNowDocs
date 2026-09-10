---
title: Assign roles and create service accounts
description: Assign the sn\_odbc\_rest\_access or sn\_jdbc\_rest\_access role to users who need Live Connect access. You can assign these roles to personal user accounts or create dedicated non-interactive \(Machine\) service accounts.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/create-service-account.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Live Connect configuration on your ServiceNow instance, Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Assign roles and create service accounts

Assign the **sn\_odbc\_rest\_access** or **sn\_jdbc\_rest\_access** role to users who need Live Connect access. You can assign these roles to personal user accounts or create dedicated non-interactive \(Machine\) service accounts.

## Before you begin

Role required: admin

## About this task

To enable Live Connect access for BI tools and analytics platforms, assign the **sn\_odbc\_rest\_access** or **sn\_jdbc\_rest\_access** role to personal user accounts or create dedicated service accounts. You can create multiple service accounts for different use cases with appropriate roles and access levels. For example, one account might support finance reporting \(ODBC, limited tables\) while another supports analytics \(JDBC, broader dataset\).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select **New**.

3.  On the User form, fill in the following fields:

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User ID

</td><td>

Unique identifier for this service account's login username. For example: odbc.user, jdbc.user, or sqlapi.user.

</td></tr><tr><td>

First name

</td><td>

Optional for service account.

</td></tr><tr><td>

Last name

</td><td>

Optional for service account.

</td></tr><tr><td>

Identity Type

</td><td>

For service accounts, select **Machine** from the drop-down list. This designates the account as a non-interactive user, meaning it can only connect to ServiceNow from an API protocol. For personal user accounts via OAuth, leave this as the default value.

</td></tr><tr><td>

Password needs reset

</td><td>

-   Service accounts: Leave this check box cleared. To set a password for this service account, save the record first, then in the list view double-select the **Password** field for this account and enter the password.
-   Personal accounts: Leave this check box cleared \(password is managed by the user\).


</td></tr></tbody>
</table>    Don't change any other settings.

    **Note:** Non-interactive \(Machine\) users can't complete MFA challenges. Confirm that MFA is turned off for all Live Connect service accounts.

4.  Select and hold \(or right-click\) the form header, and then select **Save**.

5.  On the **Roles** tab, select **Edit**.

    Assign one or both roles to this account. Consider creating separate accounts when different security policies or access levels apply.

6.  In the Collection list, select one or more of the following roles and move them to the Roles list.

    -   To access data via the ODBC driver: **sn\_odbc\_rest\_access**.
    -   To access data via the JDBC driver: **sn\_jdbc\_rest\_access**.
    -   To turn off row and field-level checks: **sn\_live\_connect\_privileged\_mode**.
7.  Select **Save**.


**Parent Topic:**[Live Connect configuration on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-sql-api-overview.md)

