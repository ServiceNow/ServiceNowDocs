---
title: Comparing user access
description: Compare the user's access control using the Access Analyzer.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Access Analyzer, Access Analyzer, Identity]
---

# Comparing user access

Compare the user's access control using the Access Analyzer.

## Before you begin

Role required: admin, access\_analyzer\_admin

The following procedure describes the steps for comparing the access control between the users using the Access Analyzer.

**Note:** Access Analyzer is a ServiceNow® Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

    The Analyze access and permissions homepage is displayed.

2.  Select the **Compare user access** tab.

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

Analyze access permissions for a table.**Note:** Only access permissions for a table can be used in the **compare user access**.

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
</table>4.  Select **Compare user access**.

    The **compare user access** results for the selected users are displayed.

    The compare user access results show the operation and the access evaluation status for the users. For example, Abel Tuter and ITIL User.

    ![Compare user access results](../images/comparing-access-controls-results.png)

5.  Select the Operation to know more about the permission evaluation and the roles the users are assigned to.

    For example, **read** operation.

6.  Select any of the **Access Control** to know more about the access.

    ![ACL details](../images/comparing-access-controls-operation.png)

    The Access Control details such as Roles, Security Attribute, Condition, and Script evaluation status are displayed.

    ![ACL details](../images/comparing-access-controls-details.png)

7.  Select **Show role Hierarchy** to know more about the roles and groups the user is assigned and compare both the users.

    Based on the role hierarchy, you can assign the necessary role and group assignments to the user to have access to the resources \(table\).

    ![Role or group details](../images/comparing-access-controls-role-details.png)

    In the example, **Abel Tuter** doesn't have `itil` assigned. You can determine the necessary role and group assignments to the user by looking into the role hierarchy.

    You can select the node to learn more about the role, resources the role can access, or group.


