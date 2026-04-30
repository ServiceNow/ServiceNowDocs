---
title: Create a Service Account and assign Roles
description: Create a dedicated non-interactive Service Account in User Administration and assign the appropriate SQL API access role to enable secure, programmatic access for BI tools and analytics platforms.
locale: en-us
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure SQL API plugin on your ServiceNow instance, Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create a Service Account and assign Roles

Create a dedicated non-interactive Service Account in User Administration and assign the appropriate SQL API access role to enable secure, programmatic access for BI tools and analytics platforms.

## Before you begin

Role required: admin

## About this task

To enable SQL API access for BI tools and analytics platforms, you must create a dedicated Service Account \(non-interactive user\) in your ServiceNow instance and assign the appropriate role. Service Accounts are the recommended approach for programmatic access. Using personal user accounts is not supported, as reports and dashboards will fail if that user's permissions change or the user leaves the organization.

You can create multiple Service Accounts, each with different roles and access levels. For example, one account may have ODBC access to a limited set of tables, while another has JDBC access to a broader dataset. This lets you apply granular access control per integration or team.

**Note:** Consider creating Service Accounts for BI implementations to maintain report continuity. Personal user accounts are not supported as the reports and dashboards will fail if the user loses access permissions or leaves the organization.

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

Type. Select **Machine** from the dropdown list. This designates the account as a non-interactive user, meaning it can only connect to ServiceNow from an API protocol.

</td></tr><tr><td>

Password needs reset

</td><td>

Do not check this check box as this is a machine account. To set a password for this service account, save the record first, then in the list view double-click \(or use the keyboard shortcut\) the Password field for this account and set the password.

</td></tr></tbody>
</table>    Do not change any other settings.

    **Note:** Non-interactive \(Machine\) users cannot complete MFA challenges. Confirm that MFA is turned off for all SQL API Service Accounts.

4.  Select and hold \(or right-click\) the form header and select **Save**.

5.  On the **Roles** tab, select **Edit**.

    Each Service Account must be assigned at least one role to determine which SQL API protocol it is permitted to use. You can assign a single role or both roles to one account, or create separate accounts for each. Admins should consider using separate accounts with different roles when different security policies or access levels apply.

6.  In the Collection list, select one or all of the following roles and move them to the Roles list:

    -   To access data via the ODBC driver, choose **sn\_odbc\_rest\_access**.
    -   To access data via the JDBC driver, choose **sn\_jdbc\_rest\_access**.
    -   To turn off row and field-level checks at the Service Account level, choose **sn\_sql\_api\_privileged\_mode**.
    ![Selecting desired roles in the Collection list.](../image/sql-api-collection-list-roles.png)

    Make sure that service account has the required roles with read-access enabled on the desired tables.

7.  Select **Save**.


## Result

The Service Account is now created with the appropriate SQL API access role. This account can be used to authenticate ODBC or JDBC connections from BI tools and analytics platforms. The account will only be able to query tables for which explicit access has been granted through Access Control Lists \(ACLs\). See [Create Access Control Lists \(ACLs\) for SQL API](create-acls-sql-api.md).

**Parent Topic:**[Configure SQL API plugin on your ServiceNow instance](configure-sql-api-overview.md)

