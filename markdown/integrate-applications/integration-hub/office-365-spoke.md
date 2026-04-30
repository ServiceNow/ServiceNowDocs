---
title: Microsoft 365 Excel Spoke
description: Manage Microsoft Office 365 Excel workbooks stored in Microsoft OneDrive from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Microsoft 365 Excel Spoke

Manage Microsoft Office 365 Excel workbooks stored in Microsoft OneDrive from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft 365 Excel spoke v1.0.4 is the latest version.

## Supported versions

This spoke was built for Microsoft Office 365 Excel v1.0, but may be compatible with later versions.

## Spoke requirements

-   Microsoft Azure Portal account
-   Client ID and Client Secret of the application registered in Azure Portal

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Microsoft 365 Excel Spoke provides actions to automate  tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Cell and Range Management|Get Cell Details|Retrieves the properties of the specified cell.|
|Get Cells|Retrieves the properties of the selected range of cells.|
|Update Cells|Updates the properties of the selected range of cells.|
|Table Management|Add Rows|Adds one or more rows to the given table.|
|Create Table|Adds a table to the worksheet.|
|Get Table Cells|Retrieves the properties of the selected range of table cells.|
|Get Table Details|Retrieves the properties of the specified table.|
|Look up Table Columns|Lists the details of the specified range columns from the selected table.|
|Look up Table Rows|Lists the details of the specified range of rows from the selected table.|
|Workbook Management|Look up Workbooks|Lists all the workbooks in the specified folder.|
|Worksheet Management|Add Worksheet|Adds a worksheet to a workbook.|
|Get Used Cells|Retrieves the properties of the specified range of cells in the worksheet.|
|Get Worksheet Details|Retrieves the properties of the worksheet.|
|Look up Worksheets|Lists all the worksheets in the workbook.|
|Update Worksheet|Updates a worksheet of a workbook.|

**Note:** You must specify the input values for **Update Cells** and **Add Row** actions as shown in the following examples.

Add Row action: The action input, Value 1 corresponds to the first row in your table. The values Hello and 100 correspond to the values of the first and second column respectively.![Input value examples for Add Row action.](../image/excel365_spoke_add_row1.png) ![Example input values format for Add Row action.](../image/excel365_spoke_add_row2.png)You must provide values in the same format for the action inputs: Formulas, Formulas R1C1, Formulas Local, and Number Format. For more information, see [Add Row](https://docs.microsoft.com/en-us/graph/api/table-post-rows?view=graph-rest-1.0&tabs=http).

Update Cells action: The action input, Value 1 corresponds to the first row in your range. The values Hello and 100 correspond to the values of the first and second column respectively.![Input value examples for Update Cellls action.](../image/excel365_spoke_update_cells1.png) ![Example input values format for Add Row action.](../image/excel365_spoke_update_cells2.png)You must provide values in the same format for the action inputs: Formulas, Formulas R1C1, Formulas Local, and Number Format. For more information, see [Update Rage](https://docs.microsoft.com/en-us/graph/api/range-update?view=graph-rest-1.0&tabs=http).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Microsoft 365 Excel spoke](../task/setup-office-365-excel.md#).

