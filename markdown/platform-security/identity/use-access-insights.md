---
title: Use Access Insights
description: Use Access Insights to understand the users peer level access to a selected resource.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access Insights, Access Analyzer, Identity]
---

# Use Access Insights

Use Access Insights to understand the users peer level access to a selected resource.

## Before you begin

Role required: admin, access\_analyzer\_admin

**Note:** To view the details of though Access Insights feature, you must use the [Compare user access](comparing-access-controls.md) feature.

The following procedure describes the steps for viewing the peer level role or group assignments statistics within the Access Insights feature.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

    The Analyze access and permissions home page is displayed.

2.  Select the **Compare user access** tab.

3.  Fill in the following fields:

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

5.  Select an operation.

    For example, **read** operation.

6.  Select any of the **Access Control** to learn more about the access.

7.  Select **Show role Hierarchy** to view the access comparison at a peer level access.

    The Access Insights is displayed as follows:

    -   **Peer Insights**: Displays how many users have the same role assigned within their peers \(the same manager or department\).
    -   **Org Insights**: Displays how many users have the same role assigned within the organization.
    ![Access Insights](../images/access-insights-homepage.png)

    Based on this information, you can choose to provide or revoke access to the user that you’d compared.


