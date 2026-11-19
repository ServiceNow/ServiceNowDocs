---
title: Use the ODBC driver in Excel
description: After installing the ODBC driver and its associated DSN, use it in Excel as a data source provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/t\_UsingTheODBCDriverInExcel2010.html
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ODBC and client applications, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Use the ODBC driver in Excel

After installing the ODBC driver and its associated DSN, use it in Excel as a data source provider.

## Before you begin

Role required: admin

## Procedure

1.  In Excel, open the **Data** tab.

2.  Under **From Other Sources**, open **From Microsoft Query**.

    \[Omitted image "ExcelOtherQuery.png"\] Alt text: From Microsoft Query.

3.  Select **ServiceNow** as your database \(the default DSN name\).

4.  Clear the **Use the Query Wizard to create/edit queries** check box.

    **Note:** The Excel Query Wizard does not support the listing of columns from a table name that contain an underscore \( \_ \). Clearing this check box uses the Query Builder instead, which supports the use of this character.

    \[Omitted image "ExcelServiceNowDataSource.png"\] Alt text: ServiceNow Data Source.

5.  Supply the ServiceNow user name and password.

    \[Omitted image "ExcelDataSourceLogin.png"\] Alt text: Data Source Login.

6.  Select a table from the ServiceNow instance and click **Add**.

    \[Omitted image "ExcelODBCAddTable.png"\] Alt text: Add Table.

7.  Close the dialog box.

8.  Select the table columns that the Query Builder retrieves the data from.

    Use the list above the table or enter the names directly into the columns, and then press **Enter**.

9.  Retrieve the data and create the Excel record by clicking the **Return Data** icon or selecting **File &gt; Return Data to Microsoft Office Excel**.

    \[Omitted image "QueryBuilderRetrieveData.png"\] Alt text: Query Builder Retrieve Data.

    The requested data is brought into Excel.

    \[Omitted image "ExcelODBCResults.png"\] Alt text: Excel ODBC Results.


**Parent Topic:**[ODBC and client applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/r_ODBCAndClientApplications.md)

