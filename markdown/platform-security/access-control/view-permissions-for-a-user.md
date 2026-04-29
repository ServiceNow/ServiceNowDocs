---
title: View permissions for a user
description: Use Access Analyzer to view permissions for a selected user.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Evaluate access, Using Access Analyzer, Access Analyzer, Access Management]
---

# View permissions for a user

Use Access Analyzer to view permissions for a selected user.

## Before you begin

Role required: access\_analyzer\_admin

This procedure explains how to view the permissions for a specific user \(such as **ITIL User**\) on the **Incident** table by using the Evaluate Access feature in Access Analyzer.

**Note:** Access Analyzer is a ServiceNow AI Platform Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

    The Analyze access and permissions homepage is displayed.

2.  Select your criteria as follows:

<table id="table_cpw_mgd_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Analyze by \*

</td><td>

Select **User**.

</td></tr><tr><td>

Select user \*

</td><td>

Specify a user name to select from the list. In this example, **ITIL User**.

</td></tr><tr><td>

Rule type \*

</td><td>

Analyze access for the following:-   Table
-   UI page
-   REST Endpoint
-   Client callable script include
-   AI Agent
-   Agentic workflow.
In the example, `Table`

.

</td></tr><tr><td>

Select table \*

</td><td>

Specify a table name to select from the list. In this example, **Incident**.

</td></tr><tr><td>

Select record

</td><td>

Specify a record name to select from the list. In this example, **INC0000001**.

</td></tr><tr><td>

Select field

</td><td>

Specify a field name to select from the list. This field can be used to analyze permissions even at the field level. For example, Active, Created By, and so on.

</td></tr></tbody>
</table>3.  Specify the description in the **Description** field.

4.  Click **Analyze permissions**.

    ![Permission evaluation of Abel Tuter](../images/view-permissions-for-a-user.png)

    The system displays **Access results** for the **ITIL User**.

    ![Permission results](../images/permissions-for-a-user.png)

    The results can be read by referring to the Legends, access control list \(ACL\), IAccesshandler, and Data filters.

    Let's take the example of **read** operation. For the **ITIL User** overall access is Passed, which means the user is able to read the record with the correct permissions \(ACL\).

    Similarly for **create** operation, the overall access is passed with an alert icon, which means that there could be a presence of script for the ACL evaluation.

    **Note:** In the example, **write** and **delete** operations are blocked for the selected user and the user can’t edit or delete the selected record \(INC0000001\).

5.  Select read operation to know more about the Debug logs.

    ![ACL Details](../images/acl-details-for-user.png)

    The Debug logs page displayed the business rule and associated ACLs that are required to perform the **read** operation for the record.

    The Debug logs shows that there’s a business rule and four ACLs associated for the read operation.

    There’s a status **Passed** for one of the ACL, which means to read the selected record, the user has the required ACL and can read the record. Since one of the ACL is **Passed**, the other ACL evaluations are **Skipped**.

6.  Select the Access Control that is Passed to see the details of the ACL.

    ![Details of the Access Control for the selected ACL](../images/view-details-for-a-user.png)

    The system displays the Access Control details for the selected ACL.

    If a selected operation that has `Passed` contains a script, the Access Control page displays the associated script for the record.

    ![Script Condition in Access Control](../images/script-for-a-user.png)


