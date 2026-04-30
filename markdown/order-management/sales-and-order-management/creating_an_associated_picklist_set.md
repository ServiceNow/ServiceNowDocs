---
title: Creating an associated picklist set
description: Learn to use an associated picklist instead of a set field when you create a new set.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 4
breadcrumb: [Configure picklist extensions, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Creating an associated picklist set

Learn to use an associated picklist instead of a set field when you create a new set.

**Note:** Be sure to read about product pickers and their functionality before building associated picklists, as they may be better suited to your use case. See [Product pickers](product_picker_overview.md).

The New Set dialog box includes an option for size type. **Set Field** is the default. If you select **Associated picklist**, a new field appears where you can select the picklist field that will be associated with the set.

![picklist set](../images/cpq-associated-picklist-new-set.png)

This associated picklist must be a multi-select picklist field. This field determines the size of the set based on the number of field options in the picklist. If you edit the field to add or remove field options, the set size will adjust accordingly. This is the only way to adjust the size of the set associated with the picklist.

For example, a “Condiments” picklist could let users choose to include specific condiments, such as ketchup, mustard, or relish. A “Packets” associated picklist set could then let users specify the quantity of each item using set subfields.

Unlike a regular set where a user can add as many rows as they want, each non-excluded field option of a picklist generates a row and index of the set. Inclusion and exclusion rules still work on the associated field, which can dynamically change the number of rows in the associated picklist set. The following is the sample picklist field we will use in this example. \(Note that the labels and values differ.\)

![picklist set](../images/cpq-associated-picklist-field-sample.png)

Once we select Condiments as the associated picklist, the normal set UI appears. Associated picklist sets automatically create three fields in the set:

-   Index: the row number of the set, starting at 1
-   Option Value: the associate picklistʼs field option values
-   Select Option: a Boolean field to indicate that the set index is selected

![picklist set](../images/cpq-associated-picklist-fields.png)

Like all other fields in the set, the option value, the select option, and the set itself need to be added to the layout. The following image shows the interaction between the Condiments associated picklist and the packets set:

![picklist set](../images/cpq-associated-picklist-interaction.png)

Note that the option values in the set reflect the associate picklistʼs field option values. \(“Ketchup” is reflected as “K”, the field option value.\) Also note that option values are read-only and cannot be edited.

Associated picklist sets can still be acted upon with determination actions, inclusion actions, and exclusion actions. In the example below, a new field called KetchupBan removes Ketchup as a value from the Condiments picklist:

![picklist set](../images/cpq-associated-picklist-interaction-new-field.png)

## Benefits of the associated picklist set

Depending on the configuration, there may be several reasons why an associated picklist set would be better than a regular set.

-   Situations where each option value can only be used once
-   Situations where select Option and Option Value fields that are used for index specific actions and other rules
-   Associated picklist sets have a finite size, with as many indexes as the picklist has field options

Note that picklist extension fields can also be used as the associated picklist. Furthermore, the associated picklist can live elsewhere on the page layout or in the background—it does not need to be near the set it controls.

## Example: A complex rule

The customer has 100 different fees that could be applied to the configuration. To determine the value of these fees, each fee is calculated using a complex formula. Each fee is only be applied once. The formula is the same for all fees. The customer does the following in ServiceNow CPQ:

-   Creates a multi-select picklist field called Fees with 100 field options \(one for each fee\)
-   Creates an associated picklist set and selects Fees as the associated picklist
-   Creates inclusion rules for the Fees field
    -   This would create an inclusion rule for each fee based on the condition of that fee.
    -   This would also create an inclusion rule that included none of the fees as a default. This way, the Fees are added, as inclusion rules are additive.
-   Creates a rule for calculating the fee

    This is where the associated picklist set is really beneficial. The customer only has to write 1 rule, and it is applied to each row of the set. If the customer did not use the set, they would have had to replicate this script multiple times in multiple rules throughout the configuration. This can lead to errors downstream when the complex calculation changes.


## Example: Picklist extension with varying quantities for product rules

Another customer has effectively used the picklist extension to filter field options and provide columns of extra information. However, they cannot use the picklist extension to add products to the bill of materials because they want to give the end user the ability to specify the quantities as each field option is added to the BOM.

They put the picklist extension grid on a single tab tier, and then they put the set, which shows all the field options selected on the first Tab Tier, on the second tab tier. Using the associated picklist set, the end user can customize for each customer the quantity added to the BOM.

