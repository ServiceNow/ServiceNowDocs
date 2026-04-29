---
title: Create Access Control Lists \(ACLs\) for SQL API
description: Configure table-level access control using the egress\_sql and read operations to grant Service Accounts query access to specific tables through the SQL API.
locale: en-us
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure SQL API plugin on your ServiceNow instance, Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create Access Control Lists \(ACLs\) for SQL API

Configure table-level access control using the egress\_sql and read operations to grant Service Accounts query access to specific tables through the SQL API.

## Before you begin

Verify the following prerequisites are in place:

-   You created a Service Account and assigned it with sn\_odbc\_rest\_access or/and sn\_jdbc\_rest\_access role.
-   You identified which ServiceNow tables must be accessible via the SQL API.

Role required: security\_admin

## About this task

Access to tables through the SQL API is not granted globally. For each table that a Service Account needs to query, you must create two Access Control Lists \(ACLs\). Create one for the egress\_sql operation \(which controls SQL API data export\) and one for the read operation \(which controls record-level access\). A Service Account can only query tables for which both ACLs have been explicitly configured.

By default, the SQL API checks access at the table, row, and field level for every query. This follows ServiceNow's secure-by-default approach. The SQL API validates all ACLs in your instance record by record. This may result in longer response times. This is expected.

If your use case does not require row and field-level checks, you can turn them off by assigning the `sn_sql_api_privileged_mode` role to the service account. For example, a Business Intelligence integration. Table-level ACL checks remain in effect and cannot be turned off.

Repeat this procedure for each table and role combination that requires SQL API access. If you have multiple Service Accounts with different roles, create separate ACLs for each role and table combination.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Access Control \(ACL\)**.

2.  Select **New**.

3.  On the Access Control form, configure the first ACL for the egress\_sql operation.

<table><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Operation

</td><td>

Select **egress\_sql** from the drop-down list. This operation controls whether data can be exported via the SQL API.

</td></tr><tr><td>

Decision Type

</td><td>

Allow if

</td></tr><tr><td>

Name

</td><td>

Select the table you want to grant access to. For example, **incident \[incident\]** or **cmdb\_ci**.

</td></tr><tr><td>

Requires role

</td><td>

Enter the role assigned to your Service Account \(for example, **sn\_odbc\_rest\_access**, **sn\_jdbc\_rest\_access**\).Add the role **sn\_sql\_api\_privileged\_mode** to turn off row and field-level checks at the Service Account level.

</td></tr></tbody>
</table>    ![UI screen example showing configuration of access control definition with the required roles.](../image/sql-api-acl-conditions.png)

4.  Select and hold \(or right-click\) the form header and select **Save**.

5.  Create the second ACL for the same table by selecting **New**.

6.  On the Access Control form, configure the second ACL for the **read** operation:

    |Field|Description|
    |-----|-----------|
    |Operation|Select **read** from the drop-down list. This operation controls record-level access to the table.|
    |Decision Type|Allow if|
    |Name|Select the same table you specified in the egress\_sql ACL.|
    |Requires role|Enter the same role you specified in the egress\_sql ACL.|

7.  Select and hold \(or right-click\) the form header and select **Save**.

8.  Repeat steps 2 through 7 for each additional table that requires SQL API access.

    You have created both required ACLs \(egress\_sql and read\) for each table.


## Result

You have successfully configured table-level access control for the SQL API. The Service Account can query the tables for which both egress\_sql and read ACLs have been created, subject to the role requirements you specified.

Remember that access is granted on a per-table basis. If you grant access to additional tables, or if you create additional Service Accounts with different roles, repeat this procedure to create the appropriate ACLs.

**Parent Topic:**[Configure SQL API plugin on your ServiceNow instance](configure-sql-api-overview.md)

