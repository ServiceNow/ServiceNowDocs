---
title: Export Access Analyzer queries
description: Export the queries analyzed using Access Analyzer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/access-control/export-access-analyzer-queries.html
release: zurich
product: Access Control
classification: access-control
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use Evaluate access, Use Access Analyzer, Access analyzer, Access Management]
---

# Export Access Analyzer queries

Export the queries analyzed using Access Analyzer.

## Before you begin

Role required: admin, access\_analyzer\_admin

The following procedure describes the steps for accessing Access Analyzer and using various features within Access Analyzer.

**Note:** Access Analyzer is a ServiceNow® Store product.

## Procedure

1.  Navigate to **All** &gt; **Access Analyzer** &gt; **Analyze Permissions**.

    The Analyze access and permissions homepage is displayed.

2.  Select your criteria as follows.

    |Field|Description|
    |-----|-----------|
    |Analyze by|A user, a role, or a group for which to analyze access|
    |Select user|Name of the user, selected from the list.|
    |Rule type|A table, a UI page, a REST endpoint, or a client callable script include for which to analyze access.|
    |Select table|Name of the table, selected from the list.|
    |Select record|Name of the record, selected from the list.|
    |Select field|Name of the field, selected from the list.|

3.  Specify the description in the **Description** field.

4.  Select **Analyze permissions**.

    \[Omitted image "use-access-analyzer.png"\] Alt text: Permission evaluation of Abel Tuter

    The access results for the user are displayed. Similarly you can analyze the permissions of a group or role for the following rule types:

    -   Table \(record\)
    -   Client callable script include
    -   REST endpoints
    The **Access results** for the selected rule type are displayed.

    \[Omitted image "permissions-for-a-user.png"\] Alt text: Permission results

5.  Select **Export**.

    1.  Choose the File Type.

        Available file types are Excel, CSV, JSON, PDF.

        \[Omitted image "export-access-analyzer-queries.png"\] Alt text: Export File Type

    2.  Choose the Delivery Type.

        Available delivery types are Download and Email.

        \[Omitted image "analyzer-queries.png"\] Alt text: Delivery Types


