---
title: View permissions for a role
description: Use Access Analyzer to view permissions for a selected role.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Evaluate access, Using Access Analyzer, Access Analyzer, Access Management]
---

# View permissions for a role

Use Access Analyzer to view permissions for a selected role.

## Before you begin

Role required: access\_analyzer\_admin

This procedure explains how to view the permissions for a specific role \(such as **user\_admin**\) on a REST API endpoint by using the Evaluate Access feature in Access Analyzer.

**Note:** Access Analyzer is a ServiceNow® Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

    The system displays the Analyze access and permissions homepage.

2.  Select your criteria as follows:

<table id="table_cpw_mgd_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Analyze by \*

</td><td>

Select **Role**.

</td></tr><tr><td>

Select user \*

</td><td>

Specify a role to select from the list. For example, **user\_admin**.

</td></tr><tr><td>

Rule type \*

</td><td>

Analyze access for the following:-   Table
-   UI page
-   REST Endpoint
-   Client callable script include
-   AI Agent
-   Agentic workflow.
For example, **REST Endpoint**.

</td></tr><tr><td>

REST endpoint\*

</td><td>

Specify a REST endpoint. For example, `/api/global/user_role_inheritance`.**Note:** The complete REST endpoint must be used when using the selected field.

</td></tr><tr><td>

REST endpoint method \*

</td><td>

Specify a REST endpoint method. For example, GET.

</td></tr></tbody>
</table>3.  Specify the description in the **Description** field.

4.  Click **Analyze permissions**.

    ![REST endpoint permissions](../images/view-permissions-for-a-role.png)

    The **Access results** for the **user\_admin** role is displayed.

    The results can be read by referring to the Legends, access control list \(ACL\), IAccesshandler, and Data filters.

    The overall access for the role is `passed`, which means that the role \(**user\_admin**\) is able to access the **REST endpoint** for the selected **GET** method.


