---
title: View permissions for a user
description: Use Access Analyzer to view permissions for a selected user.
locale: en-US
release: xanadu
product: Identity
classification: identity
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Evaluate access, Using Access Analyzer, Access Analyzer, Identity]
---

# View permissions for a user

Use Access Analyzer to view permissions for a selected user.

## Before you begin

Role required: admin

The following procedure describes the sample steps to view permissions for a selected user \(**ITIL User**\) to view the permissions of the **Incident** table using the evaluate access in Access Analyzer.

**Note:** Access Analyzer is a ServiceNow® Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

    The Analyze access and permissions homepage is displayed.

2.  Select your criteria as follows:

    |Field|Description|
    |-----|-----------|
    |Analyze by \*|Select **User**.|
    |Select user \*|Specify a user name to select from the list. In this example, **ITIL User**.|
    |Rule type \*|Analyze access for a **Table**, a **UI page**, a **REST Endpoint**, or a **client callable script include**. In the example, `Table`.|
    |Select table \*|Specify a table name to select from the list. In this example, **Incident**.|
    |Select record|Specify a record name to select from the list. In this example, **INC0000001**.|
    |Select field|Specify a field name to select from the list. This field can be used to analyze permission even at a field level. For example, Active, Created By, and so on.|

3.  Specify the description in the **Description** field.

4.  Select **Analyze permissions**.

    ![Permission evaluation of Abel Tuter](../images/view-permissions-for-a-user.png)

    The **Access results** for the **ITIL User** is displayed.

    ![Permission results](../images/permissions-for-a-user.png)

    The results can be read, by referring to the Legends, access control list \(ACL\), IAccesshandler, and Data filters.

    Let's take the example of **read** operation. For the **ITIL User** overall access is Passed, which means the user is able to read the record with the correct permissions \(ACL\).

    Similarly for **create** operation, the overall access is passed with an alert icon, which means that there could be a presence of script for the ACL evaluation.

    **Note:** In the example, **write** and **delete** operations are blocked for the selected user and the user can’t edit or delete the selected record \(INC0000001\).

5.  Select read operation to know more about the Debug logs.

    ![ACL Details](../images/acl-details-for-user.png)

    The Debug logs page displayed the business rule and associated ACLs that are required to perform the **read** operation for the record.

    The Debug logs shows that there’s a business rule and 4 ACLs associated for the read operation.

    There’s a status **Passed** for one of the ACL, which means to read the selected record, the user has the required ACL and can read the record. Since one of the ACL is **Passed**, the other ACL evaluations are **Skipped**.

6.  Select the Access Control that is Passed to know the details of the ACL.

    ![Details of the Access Control for the selected ACL](../images/view-details-for-a-user.png)

    The details of the Access Control for the selected ACL are displayed.

    For a selected operation with the **Passed** and a presence of a script. The Access Control page displays the associated script for the record.

    ![Script Condition in Access Control](../images/script-for-a-user.png)


