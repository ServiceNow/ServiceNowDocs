---
title: Working with external datasets
description: Use the data available outside of ServiceNow environment in Process Mining to optimize your processes and solve business problems. To use external datasets, you must first import them into ServiceNow environment.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Process Mining, Process Mining, Platform Analytics]
---

# Working with external datasets

Use the data available outside of ServiceNow® environment in Process Mining to optimize your processes and solve business problems. To use external datasets, you must first import them into ServiceNow® environment.

**Note:** For Process Mining for External Data subscription, please contact your account team. You can request for the purchase of this feature from ServiceNow® Store.For more information, see [Request Process Mining for external data](access-ext-data.md).

Importing external datasets into ServiceNow® environment lets you use Process Mining on any data without thinking about its source, thus making your life easy.

To import external datasets into ServiceNow® and create a project with it and mine it, you must do the following steps:

-   [Create an audit table](../task/create-table.md)
-   [Import external data into the audit table](../task/import-data.md)
-   [Validate the imported data](../task/verify-data.md)
-   [Create a records table](../task/create-case-record.md)
-   [Create a project and mine it](../task/create-project.md)

![External dataset architecture](../image/ext-dataset-arch.png "External dataset architecture")

-   **[Create an audit table](../task/create-table.md)**  
Create an audit table to store data. Audit table is a staging table that is created with the required columns to populate the external data.
-   **[Add custom fields to the audit table](../task/add-custom-field.md)**  
The custom fields form as breakdown filters when viewing the process graph. Without custom fields, there won't be any breakdown filters.
-   **[Import data into the audit table](../task/import-data.md)**  
Import external dataset into the audit table to start working with the data in Process Mining.
-   **[Verify the imported data](../task/verify-data.md)**  
Verify the data that was imported and validate that the data is accurate. The success of your data mining depends on the accuracy of your imported data.
-   **[Create case records for the imported data](../task/create-case-record.md)**  
Create case records for the imported data as it is important for creating a project and mining it. Without a record table, a project can’t be created.
-   **[Create a project](../task/create-project.md)**  
Create a project with the imported external data. You must mine the project to analyze your data and improve your processes.
-   **[Managing an audit table](managing-audit-table.md)**  
After the audit and record tables are created with the imported data, you can use them to create a project. You can also share, edit, empty, or delete the tables.

**Parent Topic:**[Using Process Mining](use-process-mining.md)

