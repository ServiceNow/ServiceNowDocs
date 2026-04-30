---
title: Using variables for price setup
description: You can define a price for every service catalog item. The price or recurring price of a catalog item can be modified with variables, increasing the base price for that item.A reference variable includes a Pricing implications field.A lookup select box variable is more powerful than a reference variable.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using variables for price setup

You can define a price for every service catalog item. The price or recurring price of a catalog item can be modified with variables, increasing the base price for that item.

This pricing is useful if you want the price or recurring price dynamically calculated based on how a user completes the ordering form. For example, the cost of an item can be increased based on options the user selects, such as extra memory in a PC.

The following [variable types](../reference/r_VariableTypes.md) can be configured to modify the total cost of an item:

-   Check box
-   Multiple choice
-   Reference
-   List collector
-   Select box
-   Lookup select box

## Check box

A check box variable helps to set the price or recurring price of the item being ordered.

You can [Create a check box variable](../task/t_CreateAVariableForACatalogItem.md) and set the price of the item. Use the **Price if checked** or **Recurring price if checked** field to specify the price or recurring price difference for that variable when the option is selected.

Under the **Type Specifications** tab, you can specify the price in different currency types. Also, you can configure the price in the following pricing models:

-   Calculated
-   Fixed
-   Multiple

For information on the pricing models, see [Price fields](https://www.servicenow.com/docs/access?context=price-fields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) .

## Multiple choice

For a multiple choice variable, there are two options for pricing.

-   Specify the price difference in the **Price** field on the question choices.
-   Specify the recurring price difference in the **Recurring Price** field on the question choices.

**Note:** Select boxes operate the same as multiple choice variables but are displayed as select boxes.

**Parent Topic:**[Service Catalog customization](../topic/p_ServiceCatalogCustomization.md)

## Reference

A reference variable includes a **Pricing implications** field.

If this field is selected and there is a **price**, **u\_price**, **recurring\_price**, or **u\_recurring\_price** field on the referenced table, the value of that field is used to modify the cost of the item being ordered when a reference value is selected.

For example, suppose that computers in Phoenix cost $100 more than the ordering price, and computers in Boise cost $100 less than the ordering price.

1.  Set up a reference variable to the Location \[cmn\_location\] table.
2.  Put a **u\_price** field on the Location table.
3.  Set that field to `100` for the Phoenix location.
4.  Set that field to `-100` for the Boise location.

When ordering a computer, if **Phoenix** is selected as the location for this variable, the ordering price is increased by $100. If **Boise** is selected, the ordering price is decreased by $100.

**Note:** List collectors operate the same as a reference variable, but use the **List table** field to specify the table being referenced. Since it is a list collector variable, multiple selections can be made that all modify the ordering price or recurring price.

## Lookup select box

A lookup select box variable is more powerful than a reference variable.

Specify the following when [creating a lookup select box variable](../task/t_CreateAVariableForACatalogItem.md):

-   **Lookup from table**: the table from which values are queried.
-   **Lookup value field**: the field on the lookup table whose value is used as the value of the variable \(typically sys\_id\).
-   **Lookup label field\(s\)**: a comma-separated list of fields on the lookup table whose values are used to display the selections in the select box. For example,**manufacturer,name** for the Software \[cmdb\_ci\_spkg\] table would display selections as:
    -   Microsoft \| Excel
    -   Adobe \| Photoshop Elements
-   **Lookup price field**: the field whose value is used to modify the price of the item being ordered.
-   **Lookup recurring price field**: the field whose value is used to modify the recurring price of the item being ordered.

