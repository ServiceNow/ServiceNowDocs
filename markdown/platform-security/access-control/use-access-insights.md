---
title: Using Access Insights
description: Use Access Insights to understand users' peer-level access to a selected resource.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access Insights, Access Analyzer, Access Management]
---

# Using Access Insights

Use Access Insights to understand users' peer-level access to a selected resource.

## Before you begin

Role required: access\_analyzer\_admin

**Note:** To view the details of though Access Insights feature, you must use the [Compare user access](comparing-access-controls.md) feature.

The following procedure describes the steps for viewing the peer level role or group assignment statistics within the Access Insights feature.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

2.  On the Analyze access and permissions home page, select the **Compare user access** tab.

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

Analyze access permissions for a table.**Note:** Only access permissions for a table can be used in the **Compare user access**.

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

    The **Compare user access** results show the access evaluation status for the operation per user. For example, **Charlier Fuhri** and **Charlie Knower**.

5.  Click an operation.

    For example, click the **read** operation.

6.  Select an **Access Control** to learn more about access.

7.  Select **Show role Hierarchy** to view a peer-level access comparison.

    **Access Insights** show:

    -   **Peer Insights**: Displays how many users have the same role assigned within their peers \(the same manager or department\).
    -   **Org Insights**: Displays how many users have the same role assigned within the organization.
    ![Access Insights](../images/access-insights-homepage.png)


## Result

Based on the insights gained, you can decide if a user has inappropriate access \(either too much or too little\) and make the necessary adjustments to their roles and groups to ensure consistency and compliance.

