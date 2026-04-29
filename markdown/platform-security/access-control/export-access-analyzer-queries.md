---
title: Export Access Analyzer queries
description: Export the results from an Access Analyzer query.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Evaluate access, Using Access Analyzer, Access Analyzer, Access Management]
---

# Export Access Analyzer queries

Export the results from an Access Analyzer query.

## Before you begin

Role required: access\_analyzer\_admin

The following procedure describes the steps for accessing Access Analyzer and using various features within Access Analyzer.

**Note:** Access Analyzer is a ServiceNow® Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

    The system displays the **Analyze access and permissions** homepage.

2.  Select your criteria as follows:

    |Field|Description|
    |-----|-----------|
    |Analyze by \*|Analyze access for a user, a role, or a group.|
    |Select user \*|Specify a user name to select from the list.|
    |Rule type \*|Analyze access for a table, UI page, REST Endpoint, or a client callable script include.|
    |Select table \*|Specify a table name to select from the list.|
    |Select record|Specify a record name to select from the list.|
    |Select field|Specify a field name to select from the list.|

3.  Specify the description in the **Description** field.

4.  Click **Analyze permissions**.

    ![Permission evaluation of Abel Tuter](../images/use-access-analyzer.png)

    Access Analyzer displays **Access results** for the user. Similarly, you can analyze the permissions of a Group or Role for the following rule types:

    -   Table \(record\)
    -   Client callable script include
    -   REST endpoints
    Access Analyzer displays **Access results** for the selected rule type.

    ![Permission results](../images/permissions-for-a-user.png)

5.  Click **Export**.

    1.  Choose the **File Type**.

        Available file types are **Excel**, **CSV**, **JSON**, **PDF**.

        ![Export File Type](../images/export-access-analyzer-queries.png)

    2.  Choose the **Delivery Type**.

        Available delivery types are **Download** and **Email**.

        ![Delivery Types](../images/analyzer-queries.png)


