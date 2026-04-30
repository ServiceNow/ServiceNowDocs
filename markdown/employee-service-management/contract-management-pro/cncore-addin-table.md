---
title: Map contract document tables using the Microsoft Word add-in for ServiceNow Contracts
description: Use the Microsoft Word add-in to map a contract table to a source table in your ServiceNow instance to determine the data that will be added in a contract document. When a contract document is generated from the template, the rows and columns are dynamically added in the mapped table of the contract document.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Add document content controls using Microsoft Word add-in for ServiceNow Contracts, Creating a contract template using Microsoft Word add-in for ServiceNow Contracts, Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Map contract document tables using the Microsoft Word add-in for ServiceNow Contracts

Use the Microsoft Word add-in to map a contract table to a source table in your ServiceNow instance to determine the data that will be added in a contract document. When a contract document is generated from the template, the rows and columns are dynamically added in the mapped table of the contract document.

## Before you begin

The Microsoft Word add-in for ServiceNow Contracts must be configured. For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md).

An active contract template must exist in the Draft or Editing state. For more information, see [Create a contract template to contain content controls](cncore-create-ct-word-addin.md).

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open the Microsoft Word document in which you want to map tables.

2.  From the Microsoft Word ribbon, select the ServiceNow Contracts add-in.

3.  On the login screen, enter the credentials of the ServiceNow instance for which the Microsoft Word add-in is configured.

    For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md)

4.  In the **Templates** tab of the Microsoft Word add-in screen, select the contract template to which you want to map the data source table.

5.  In the **Table** tab, create a table mapping for the template.

    -   For a first table mapping, select **Configure table mapping**.
    -   For subsequent table mappings, select the add icon ![Add icon](../../ppe-inventory-management/image/plus-icon.png) beside the search bar.
6.  In the **Table mapping details** section, configure the details for the data source table from which you want to add data in the contract document.

    1.  In the **Table** field, select the data source table from which you want to add data in a contract document.

    2.  In the **Name** field, either retain the default name or enter a unique table name.

    3.  In the **Record identifier** field, select a table field to determine which records are added to the contract document.

        For example, if you have selected the Quote Line Item table and you want to include data only from the Quote record that initiated the contract, you would select the **Quote** field.

    4.  In the **Table Columns** field, select the columns of the data source table that you want to map to the contract template.

    5.  Select **Next**.

7.  In the **Table display configuration** section, set the display properties to define how the data appears within the table in the contract document and then select **Next**.

<table id="choicetable_cv4_gdw_bcc"><thead><tr><th align="left" id="d464660e271">

Field

</th><th align="left" id="d464660e274">

Description

</th></tr></thead><tbody><tr><td id="d464660e280">

**Sort by**

</td><td>

The criteria by which to sort the data.

</td></tr><tr><td id="d464660e289">

**Sorting order**

</td><td>

Sorts the data either in ascending or descending order.

</td></tr><tr><td id="d464660e298">

**Enable hierarchy**

</td><td>

Option to group the data based on parent-child relationships.

</td></tr><tr><td id="d464660e307">

**Parent field**

</td><td>

The parent field for the hierarchy view.This field appears only when **Enable hierarchy** has been selected.

</td></tr><tr><td id="d464660e322">

**Hierarchy column\(s\)**

</td><td>

The columns for which data should be displayed in the hierarchy view.This field appears only when **Enable hierarchy** has been selected.

</td></tr><tr><td id="d464660e336">

**Row indentation**

</td><td>

The number of spaces that child columns should be indented.This field appears only when **Enable hierarchy** has been selected.

</td></tr></tbody>
</table>8.  Display the formatting symbols by selecting the Show/Hide formatting marks icon \(![Show/Hide formatting marks icon](../image/lsd-word-formatting-icon.png)\) on the Microsoft Word Home ribbon.

9.  Initiate the table mapping in the contract template by selecting it along with the paragraph symbol \(¶\), and then selecting the table tag in the **Map dynamic table** section.

10. Select **Next**.

11. Map the columns in the contract template table by selecting a column in the mapped table and then selecting the appropriate column tag in the **Map table columns** section.

12. Select **Complete**.


## Result

The table mapping is completed and is listed under the **Table** tab on the add-in panel.

You can add conditions for the table mapping to filter for the data that appears in the contract. For more information, see [Add conditions for a contract table mapping](cncore-add-filter-table-map.md).

**Parent Topic:**[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

**Related topics**  


[Configure metadata for fields, variables, and variables sets in a contract document](cncore-addin-add-metadata.md)

[Configuring signatories in Contract template using Microsoft Word add-in](../concept/cncore-config-sign-addin.md)

[Map clauses and clause variations using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-add-clauses.md)

