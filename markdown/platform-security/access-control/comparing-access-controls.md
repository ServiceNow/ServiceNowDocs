---
title: Comparing user access
description: Use Access Analyzer to compare two users' access control.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Access Analyzer, Access Analyzer, Access Management]
---

# Comparing user access

Use Access Analyzer to compare two users' access control.

## Before you begin

Role required: access\_analyzer\_admin

The following procedure describes the steps for comparing the access control between two users using the Access Analyzer.

**Note:** Access Analyzer is a ServiceNow® Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

2.  On the **Analyze access and permissions** homepage, select the **Compare user access** tab.

3.  Fill in the following fields:

    ![Compare user access](../images/comparing-access-controls.png)

<table id="table_urw_xh5_szb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select user 1\*

</td><td>

Specify a user name to select from the list for the comparison.

</td></tr><tr><td>

Select user 2\*

</td><td>

Specify a user name to select from the list to compare with the user 1.

</td></tr><tr><td>

Rule Type\*

</td><td>

Analyze access permissions for a table.**Note:** Only access permissions for a table can be used in **Compare user access**.

</td></tr><tr><td>

Select table\*

</td><td>

Specify a table name to select from the list.

</td></tr><tr><td>

Select record

</td><td>

Specify a record name to select from the list.

</td></tr><tr><td>

Select field

</td><td>

Specify a field name to select from the list.

</td></tr></tbody>
</table>4.  Click **Compare user access**.

    The **Compare &lt;user 1&gt; to &lt;user 2&gt;: access controls** results show the operation and the access evaluation status for the users. For example, Abel Tuter and ITIL User.

    ![Compare user access results](../images/comparing-access-controls-results.png)

5.  Click an **Operation** in the list for details about the permission evaluation and assigned roles.

    In this example, click the **read** operation.

6.  Select any of the **Access Control** to know more about the access.

    ![ACL details](../images/comparing-access-controls-operation.png)

    Access Control details are shown such as Roles, Security Attribute, Condition, and Script evaluation status.

    ![ACL details](../images/comparing-access-controls-details.png)

7.  Click **Show role Hierarchy** to show the current roles and groups both users are assigned to.

    Based on the **Role hierarchy**, you can assign the necessary role and group assignments to the user to have access to the resources \(table\).

    ![Role or group details](../images/comparing-access-controls-role-details.png)

    In the example, **Abel Tuter** doesn't have `itil` assigned.

    Select a node to learn more about the role, resources the role can access, or the group.


