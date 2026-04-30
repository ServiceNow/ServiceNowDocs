---
title: Configure mapped columns to append or add fields from related tables
description: Configure dynamic tables in a contract template to display additional data from related table fields by appending it to existing columns or adding it as new columns.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-06-16"
reading_time_minutes: 2
breadcrumb: [Configure dynamic tables in contract template, Add document content controls using Microsoft Word add-in for ServiceNow Contracts, Creating a contract template using Microsoft Word add-in for ServiceNow Contracts, Configure contract templates, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure mapped columns to append or add fields from related tables

Configure dynamic tables in a contract template to display additional data from related table fields by appending it to existing columns or adding it as new columns.

## About this task

As a contract configurator, you can add scripts for configuring the mapped table columns in a contract template to include additional fields from related tables. You can choose to either append this information to an existing column or add it as a new column.

## Before you begin

-   Map tables in Microsoft Word document using the Microsoft Word add-in for ServiceNow Contracts. For more information, see [Map contract tables using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-table.md).
-   Upload and parse the document with the content controls. For more information, see [Upload and parse a Microsoft Word document that includes content controls](cncore-upload-doc-addin.md).
-   Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

2.  From the list, open the contract template for which you want to add table mapping conditions.

3.  In the Table Mappings related list, select a mapping.

4.  In the Column Mapping related list, select a column.

5.  In the Column Mapping form, select the **Advanced script** check box.

    The **Script** field appears.

    ![Advanced script on the column mapping form to configure additional fields for mapped table](../image/cmpro-script-table.png "Advanced script for column mapping")

6.  In the **Script field**, add the script to include additional fields from related tables.

7.  Select **Update**.

8.  In the Table Mapping form, select **Update**.


## Result

The additional fields will be appended to a column or added as a new column in the contract document that is generated using this template.

**Parent Topic:**[Map contract tables using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-table.md)

