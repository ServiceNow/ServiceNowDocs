---
title: View permissions for a group
description: Use Access Analyzer to view permissions for a selected group.
locale: en-US
release: xanadu
product: Identity
classification: identity
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Evaluate access, Using Access Analyzer, Access Analyzer, Identity]
---

# View permissions for a group

Use Access Analyzer to view permissions for a selected group.

## Before you begin

Role required: admin

The following procedure describes the sample steps to view permissions for a selected group \(**Incident Management**\) to view the permissions of an **Incident UI** page using the evaluate access in Access Analyzer.

**Note:** Access Analyzer is a ServiceNow® Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

    The Analyze access and permissions homepage is displayed.

2.  Select your criteria as follows:

    |Field|Description|
    |-----|-----------|
    |Analyze by \*|Select **Group**.|
    |Select user \*|Specify a user name to select from the list. For example, **Incident Management**.|
    |Rule type \*|Analyze access for a table, a UI page, a REST Endpoint, or a client callable script include. For example, **UI page**.|
    |UI Page \*|Specify the UI page. For example, **incident.do**.|

3.  Specify the description in the **Description** field.

4.  Select **Analyze permissions**.

    ![View permission of the group for a UI page](../images/view-permissions-for-a-group.png)

    The **Access results** for the **Incident Management** group is displayed.

    ![Permission results](../images/permissions-for-a-group.png)

    The results can be read, by referring to the Legends, access control list \(ACL\), IAccesshandler, and Data filters.

    The overall access for the group is passed, which means that the users within the group \(**Incident Management**\) are able to access the Incident record.


