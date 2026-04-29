---
title: Product picker bulk actions
description: Learn how to use bulk actions to automate product picker behavior without writing rules. Configure option inclusion, field determination, and quantity limits through table-based logic to control what products appear, how values are set, and when conditions apply—all directly in the product picker interface.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Product picker bulk actions

Learn how to use bulk actions to automate product picker behavior without writing rules. Configure option inclusion, field determination, and quantity limits through table-based logic to control what products appear, how values are set, and when conditions apply—all directly in the product picker interface.

Bulk actions are a simple yet powerful way to manage product pickers. Bulk actions can function as table:based rules to control and modify product pickers without needing to write traditional, global rules. Like global rules, bulk actions consist of conditions and targets. All the bulk actions together control the behavior of the product picker.

![Product Picker: bulk actions](../images/cpq-product-picker-bulk-actions-pp-setup.png)

-   \(1\) Bulk actions tab: displays all associated bulk actions of the product picker
-   \(2\) Name, Variable Name: name and variable to set for the bulk action

There are three basic types of bulk actions:

-   \(3\) Option Inclusion: What options are displayed to the user
-   \(4\) Field Determination: What values should be set for product picker child fields
-   \(5\) Quantity Field Properties: Quantity limits of options

For an example use case, view the following video: [Product Picker bulk actions2](https://www.youtube.com/watch?v=tshsAHS2ha4)

## Bulk actions: Inclusion

Option Inclusion bulk actions can automatically include \(and exclude\) product options in a product picker based on the value of global fields. If no action is in place to include options, all are included by default.

![Product Picker: bulk actions](../images/cpq-product-picker-bulk-actions-new-inclusion.png)

-   \(1\) Bulk Action Name: The name of your Option Inclusion bulk action. Variable Name will be automatically populated, but you can customize it by clicking the pencil icon.
-   \(2\) Info: What this Option Inclusion bulk action will do
-   \(3\) Select Condition fields: Global fields to use for the comparison. Additional fields can be selected, but at least one is required
-   \(4\) Select Comparator for this Condition field: The comparison that should be made against the fieldʼs value. Comparison Options depend on the field type. For example, a Boolean field type would use either ‘Equalsʼ or ‘Does Not Equalʼ. A picklist field type, such as cards\_sender, offers a large number of comparison options.
-   \(5\) Save: When finished, move to the next step to add the data for the bulk action

![Product Picker: bulk actions](../images/cpq-product-picker-bulk-actions-data-1.png)

The bulk action data drives the outcome of the Option Inclusion.

-   \(1\) Current bulk action: In the list of defined bulk actions, the selected bulk action's data is displayed in pane to the right
-   \(2\) When these values occur: One column for each field selected as a condition in the prior step. The corresponding comparator is noted in parenthesis.
-   \(3\) Include these options: product picker Option value to include if the conditions on that row are met
-   \(4\) Add Row and Save Changes: Add a new blank row to input new data; save changes to the data

Additional actions:

-   Import Data: Import a CSV file
-   Export Data: Export the data as a CSV file
-   Delete Rows: Delete the selected rows

## Bulk actions: Field determination

Field determination bulk actions are an easy way to set and default values into product picker subfields.

![Product Picker: bulk actions](../images/cpq-product-picker-bulk-actions-new-determination.png)

-   \(1\) Bulk Action Name: The name of your Option Inclusion bulk action. Variable Name will be automatically populated, but you can customize it by clicking the pencil icon.
-   \(2\) Select the target subfields: Review what this action will do, and select the target fields this action will set
-   \(3\) \[Optional\] Select the condition fields: The global fields to use for the comparison
-   
![Product Picker: bulk actions](../images/cpq-product-picker-bulk-actions-condition-field.png)

Select Comparators: For each condition field, select the comparator with which you will determine the condition. Comparison options will depend on the field type.

Save: When finished, move to the next step to add the data for the bulk action.

![Product Picker: bulk actions](../images/cpq-product-picker-bulk-actions-data-2.png)

The bulk action data drives the outcome of the Field Determination.

-   \(1\) Current bulk action: In the list of defined bulk actions, the selected bulk action's data is displayed in pane to the right
-   \(2\) For this option: the product picker option for which this Field Determination applies
-   \(3\) When these values occur:- one column for each field selected as a condition in the prior step. The corresponding comparator is noted in parenthesis.
    -   If no condition fields and comparators were selected in the condition setup step, this column heading will read "Always" and you will not be able to add data to this column.
    -   To change the conditions on this bulk action, click the pencil icon in the column heading.
-   \(4\) Set this value: the value that this rule will apply to the product picker subfield when the condition is true
-   \(5\) Add Row and Save Changes: Add a new blank row to input new data; save changes to the data

Additional actions:

-   Import Data: Import a CSV file
-   Export Data: Export the data as a CSV file
-   Delete Rows: Delete the selected rows

## Import and export bulk actions and bulk action data

![Product Picker: bulk actions](../images/cpq-product-picker-bulk-actions.png)

Individual bulk actions can be exported from a product picker as a ZIP file. The export will include both the rule definition and the data itself as a CSV file. To export a bulk action, select the action, and then click **Export**.

The data for a bulk action can also be exported in the data pane. The data can be modified and imported in the same location. To export the data from the data pane, select the action, and in the menu, click **Import Data**. Then, select the CSV file that contains the data.

## Forcing data override

By default, bulk actions that set the values of product pickers will not override a value that was set by the end user. To change this setting so that bulk actions will change user-edited values, submit a Support case and request "set the bulk actions Override User Edited Values behavior to True." This setting acts across the environment.

**Related topics**  


[Product picker aggregates](product-picker-aggregates.md)

