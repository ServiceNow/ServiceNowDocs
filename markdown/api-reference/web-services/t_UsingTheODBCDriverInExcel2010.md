---
title: Use the ODBC driver in Excel
description: After installing the ODBC driver and its associated DSN, use it in Excel as a data source provider.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
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

    ![From Microsoft Query.](../image/ExcelOtherQuery.png)

3.  Select **ServiceNow** as your database \(the default DSN name\).

4.  Clear the **Use the Query Wizard to create/edit queries** check box.

    **Note:** The Excel Query Wizard does not support the listing of columns from a table name that contain an underscore \( \_ \). Clearing this check box uses the Query Builder instead, which supports the use of this character.

    ![ServiceNow Data Source.](../image/ExcelServiceNowDataSource.png)

5.  Supply the ServiceNow user name and password.

    ![Data Source Login.](../image/ExcelDataSourceLogin.png)

6.  Select a table from the ServiceNow instance and click **Add**.

    ![Add Table.](../image/ExcelODBCAddTable.png)

7.  Close the dialog box.

8.  Select the table columns that the Query Builder retrieves the data from.

    Use the list above the table or enter the names directly into the columns, and then press **Enter**.

9.  Retrieve the data and create the Excel record by clicking the **Return Data** icon or selecting **File &gt; Return Data to Microsoft Office Excel**.

    ![Query Builder Retrieve Data.](../image/QueryBuilderRetrieveData.png)

    The requested data is brought into Excel.

    ![Excel ODBC Results.](../image/ExcelODBCResults.png)


**Parent Topic:**[ODBC and client applications](../reference/r_ODBCAndClientApplications.md)

