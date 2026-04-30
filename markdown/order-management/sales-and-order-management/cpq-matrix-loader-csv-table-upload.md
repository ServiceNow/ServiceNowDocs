---
title: Matrix Loader: CSV table upload
description: Use the Matrix Loader to import and manage table data in ServiceNow CPQ. Define table schemas, prepare matching CSV files, and upload them to populate or update tables for use in rules, lookups, and configurations, with no redeployment required for data updates.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-09-17"
reading_time_minutes: 2
breadcrumb: [Configure the Matrix Loader, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Matrix Loader: CSV table upload

Use the Matrix Loader to import and manage table data in ServiceNow CPQ. Define table schemas, prepare matching CSV files, and upload them to populate or update tables for use in rules, lookups, and configurations, with no redeployment required for data updates.

## Before you begin

**Note:** All table data can be added to ServiceNow CPQ via the Matrix Loader. This section assumes that the reader will work in a spreadsheet file \(Google Sheets, Microsoft Excel, or similar\), then download or export the result to a CSV file for upload to the Matrix Loader.

In order to upload data to a table, you must first manually define the schema for the table by creating columns. Columns include a name, data type \(either number or text\), and a description \(optional\).

Limits and boundaries:

-   Rows in a table: no practical limit
-   Columns in a table: no practical limit
-   Length of value stored in a text-type column cell: 2000 characters
-   Length of value stored in a number-type column cell: extremely high \(unlikely to reach in practice\)
-   Scripting: lookup returns a maximum of 10,000 rows from a table

Role required: Admin

## Procedure

1.  In the Admin navigation pane, click **Tables**.

    ![tables list](../images/cpq-tables-pane.png)

2.  In the upper right, click **+ New**.

3.  Name the table.

    ![Create table screen](../images/cpq-create-table.png)

4.  Name the columns, select their table type, and add a description.

5.  Click **Save**.

6.  Create a spreadsheet with your data.

    Name the columns exactly as named in the table that was created in the previous steps, and save the data in CSV format. Note that the name of the CSV file must exactly match the name of the table you created in order for the data to be correctly mapped to the table.

7.  In ServiceNow CPQ Admin, click **Matrix Loader** in the navigation pane.

    ![Matrixloader menu](../images/cpq-matrix-loader.png)

8.  Upload the CSV file to the Matrix Loader.

    ![import matrix loader](../images/cpq-matrix-loader-import.png)

    Note that if the name of the table and CSV file contains the word "table," the Matrix Loader will automatically select the Upload Type as "table." Otherwise, you will need to manually select the Upload Type.

9.  Click **Import**.

10. To confirm that the import was successful, check the import status.

    ![Import status](../images/cpq-matrix-loader-import-status.png)

    If there are error messages, confirm that the CSV file name and table name are the same, and that the column names in the table and the CSV file match exactly. Then upload the corrected CSV.

11. In the Tables section of the Admin navigation pane, click the table, and view the table to confirm that column data imported properly.

    ![tables list](../images/cpq-sample-table.png)


## Result

You are now ready to create queries using the new table. Updates to managed tables do not require a redeployment to take effect. However, updates to rules with lookups to those tables require a redeployment.

**Related topics**  


[Configure the Matrix Loader](../concept/cpq-using-the-matrix-loader.md)

[Matrix Loader: CSV rules upload](../concept/matrix_loader_csv_rules_upload.md)

