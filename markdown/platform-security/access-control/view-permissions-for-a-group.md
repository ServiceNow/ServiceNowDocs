---
title: View permissions for a group
description: Use Access Analyzer to view permissions for a selected group.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Evaluate access, Using Access Analyzer, Access Analyzer, Access Management]
---

# View permissions for a group

Use Access Analyzer to view permissions for a selected group.

## Before you begin

Role required: access\_analyzer\_admin

This procedure explains how to view the permissions for a specific role \(such as **ITIL User**\) on the **Incident** table by using the Evaluate Access feature in Access Analyzer.

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

Select **Group**.

</td></tr><tr><td>

Select user \*

</td><td>

Specify a user name to select from the list. For example, **Incident Management**.

</td></tr><tr><td>

Rule type \*

</td><td>

Analyze access for the following:-   Table
-   UI page
-   REST Endpoint
-   Client callable script include
-   AI Agent
-   Agentic workflow.
For example, **UI page**.

</td></tr><tr><td>

UI Page \*

</td><td>

Specify the UI page. For example, **incident.do**.

</td></tr></tbody>
</table>3.  Specify the description in the **Description** field.

4.  Click **Analyze permissions**.

    ![View permission of the group for a UI page](../images/view-permissions-for-a-group.png)

    Access Analyzer displays the **Access results** for the **Incident Management** group.

    ![Permission results](../images/permissions-for-a-group.png)

    The results can be read by referring to the Legends, access control list \(ACL\), IAccesshandler, and Data filters.

    The overall access for the group is `passed`, which means that the users within the group \(**Incident Management**\) are able to access the Incident record.


