---
title: Compare user access
description: Use Access Analyzer to compare two users' access control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/comparing-access-controls.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use Access Analyzer, Access Analyzer, Access Management]
---

# Compare user access

Use Access Analyzer to compare two users' access control.

## Before you begin

Role required: access\_analyzer\_admin

The following procedure describes the steps for comparing the access control between two users using the Access Analyzer.

**Note:** Access Analyzer is a ServiceNow® Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

2.  On the **Analyze access and permissions** homepage, select the **Compare user access** tab.

3.  Fill in the following fields.

    \[Omitted image "comparing-access-controls.png"\] Alt text: Compare user access

<table id="table_urw_xh5_szb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select user 1

</td><td>

User name, chosen from the list for the comparison.

</td></tr><tr><td>

Select user 2

</td><td>

User name, chosen from the list to compare with the user 1.

</td></tr><tr><td>

Rule Type

</td><td>

Access permissions analyzed for a table.**Note:** Only access permissions for a table can be used in **Compare user access**.

</td></tr><tr><td>

Select table

</td><td>

Table name, chosen from the list.

</td></tr><tr><td>

Select record

</td><td>

Record name, chosen from the list.

</td></tr><tr><td>

Select field

</td><td>

Field name, chosen from the list.

</td></tr></tbody>
</table>4.  Select **Compare user access**.

    The **Compare &lt;user 1&gt; to &lt;user 2&gt;: access controls** results show the operation and the access evaluation status for the users. For example, Abel Tuter and ITIL User.

    \[Omitted image "comparing-access-controls-results.png"\] Alt text: Compare user access results

5.  Select an **Operation** in the list for details about the permission evaluation and assigned roles.

    In this example, select the **read** operation.

6.  Select any of the **Access Control** to know more about the access.

    \[Omitted image "comparing-access-controls-operation.png"\] Alt text: ACL details

    Access Control details are shown such as Roles, Security Attribute, Condition, and Script evaluation status.

    \[Omitted image "comparing-access-controls-details.png"\] Alt text: ACL details

7.  Select **Show role Hierarchy** to show the current roles and groups both users are assigned to.

    Based on the **Role hierarchy**, you can assign the necessary role and group assignments to the user to have access to the resources \(table\).

    \[Omitted image "comparing-access-controls-role-details.png"\] Alt text: Role or group details

    In the example, **Abel Tuter** doesn't have `itil` assigned.

    Select a node to learn more about the role, resources the role can access, or the group.


