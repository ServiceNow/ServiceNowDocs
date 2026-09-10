---
title: Create Access Control Lists \(ACLs\) for Live Connect
description: Configure table-level access control using the egress\_sql and read operations to grant user accounts \(personal and service accounts\) query access to specific tables through Live Connect.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/create-acls-sql-api.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Live Connect configuration on your ServiceNow instance, Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create Access Control Lists \(ACLs\) for Live Connect

Configure table-level access control using the egress\_sql and read operations to grant user accounts \(personal and service accounts\) query access to specific tables through Live Connect.

## Before you begin

Confirm the following:

-   You have assigned the **sn\_odbc\_rest\_access** or **sn\_jdbc\_rest\_access** role to a user account \(personal or service account\).
-   You have identified which ServiceNow tables must be accessible via Live Connect.

Role required: security\_admin

## About this task

Access to tables through the Live Connect is not granted globally. For each table that a user account needs to query, the user account must have explicit read access. You can grant this access in any of the following ways:

-   Create two access control lists \(ACL\), one for the egress\_sql operation \(which controls Live Connect data export\) and one for the read operation \(which controls record-level access\).
-   Assign a role to a user account that includes read permissions for the table.

A user account can only query tables for which it has explicit read access through either method.

By default, Live Connect checks access at the table, row, and field level for every query. This follows ServiceNow's secure-by-default approach. Live Connect validates all ACLs in your instance record by record. This may result in longer response times. This is expected.

If your use case does not require row and field-level checks, you can turn them off. Assign the **sn\_live\_connect\_privileged\_mode** role to the user account \(personal or service account\). For example, you might build a dashboard used by multiple people or a Business Intelligence integration. Table-level ACL checks remain in effect and can't be turned off.

The following configurations are required for each table:

-   egress\_sql ACL: Allows Live Connect to access the table but does not grant read permission to the data.
-   Read access: The user account must have explicit read access through either an explicit read ACL or an assigned role with read permissions.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Access Control \(ACL\)**.

2.  Select **New**.

3.  On the Access Control form, configure the first ACL for the egress\_sql operation.

    This operation controls whether data can be exported via Live Connect.

<table><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Operation

</td><td>

Select **egress\_sql** from the drop-down list.

</td></tr><tr><td>

Decision Type

</td><td>

Select **Allow if** from the drop-down list.

</td></tr><tr><td>

Name

</td><td>

Select the table to grant access to \(for example, **incident \[incident\]**.

</td></tr><tr><td>

Requires role

</td><td>

Enter the role assigned to your user account \(for example, **sn\_odbc\_rest\_access** or **sn\_jdbc\_rest\_access**\).**Optional**: Add the **sn\_live\_connect\_privileged\_mode** role to turn off row and field-level checks at the user account level.

</td></tr></tbody>
</table>4.  Select and hold \(or right-click\) the form header, and select **Save**.

5.  Create the second ACL for the same table by selecting **New**.

6.  On the Access Control form, configure the second ACL for the **read** operation:

    |Field|Value|
    |-----|-----|
    |Operation|Select **read** from the drop-down list. This operation controls record-level access to the table.|
    |Decision Type|Select **Allow if** from the drop-down list.|
    |Name|Select the same table you specified in the egress\_sql ACL.|
    |Requires role|Enter the same role you specified in the egress\_sql ACL.|

7.  Select and hold \(or right-click\) the form header and select **Save**.

8.  To grant access to additional tables, repeat steps 2 through 7 for each table.

    **Note:** Access is granted on a per-table basis.


## Result

You have successfully configured table-level access control for Live Connect. The user account can query the tables for which both egress\_sql and read ACLs have been created, subject to the role requirements you specified.

**Parent Topic:**[Live Connect configuration on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-sql-api-overview.md)

