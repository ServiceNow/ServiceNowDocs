---
title: Data table guidelines for Guided Application Creator
description: When you create an application in Guided Application Creator, you can optionally create a data table for your application. To ensure that you are within the limits of your subscription and that your application performs as expected, consult the data table guidelines before you create a data table.One way to create a new data table in Guided Application Creator is to upload an external spreadsheet. Prepare your spreadsheet beforehand so that you can transfer your data seamlessly and build custom applications faster.One option for creating a data table in Guided Application Creator is to copy an existing data table and then add more fields to the newly created table. Before you extend a data table, review the extension model for the table so that you can track which database tables are created after extension.You can optionally create a new table in Guided Application Creator, but it's possible to create more custom tables than your subscription permits. To ensure that you remain within the limits of your subscription, review the custom table entitlements for your organization.
locale: en-US
release: xanadu
product: Guided Application Creator
classification: guided-application-creator
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Guided Application Creator, Building pro-code applications, Developing your application, Building applications]
---

# Data table guidelines for Guided Application Creator

When you create an application in Guided Application Creator, you can optionally create a data table for your application. To ensure that you are within the limits of your subscription and that your application performs as expected, consult the data table guidelines before you create a data table.

![Creating data tables](../image/GAC-data-tables.png)

**Note:**

ServiceNow AI Platform application subscriptions include custom table entitlements. You can create custom tables for any purpose, up to the entitlement limit in the subscription. To learn more about how your usage administrator maps the custom tables that you create to subscriptions, see [Map custom tables to a product subscription in Subscription Management](https://www.servicenow.com/docs/access?context=allocate-custom-table-subsc-app-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Guided Application Creator](guided-app-creator.md)

## Spreadsheet guidelines

One way to create a new data table in Guided Application Creator is to upload an external spreadsheet. Prepare your spreadsheet beforehand so that you can transfer your data seamlessly and build custom applications faster.

Ensure your spreadsheet is:

-   Formatted with horizontal columns and a header label for each
-   Saved as an XLSX file type

For example, format your spreadsheet as follows.

![A spreadsheet with horizontal columns and a header label for each](../image/gac-good-spreadsheet.png)

In Guided Application Creator, you would designate the second row as the header row so that **Client name** and **Phone number** are uploaded as table fields.

## Table extension guidelines

One option for creating a data table in Guided Application Creator is to copy an existing data table and then add more fields to the newly created table. Before you extend a data table, review the extension model for the table so that you can track which database tables are created after extension.

Extending a base table incorporates all the fields of the original table and creates system fields for the new table. If they are in the same scope or if they can be configured from other scopes, you can extend tables that are marked as extensible.

For more information on extension models, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Table creation guidelines

You can optionally create a new table in Guided Application Creator, but it's possible to create more custom tables than your subscription permits. To ensure that you remain within the limits of your subscription, review the custom table entitlements for your organization.

