---
title: Transaction Manager: Rules and rule groupings
description: Rules in Transaction Manager are similar to configuration rules. You can also group rules together when they are intended to run together.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 15
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Rules and rule groupings

Rules in Transaction Manager are similar to configuration rules. You can also group rules together when they are intended to run together.

As in configuration, rules in Transaction Manager govern what actions are taken, if any, when a user makes an input into the Transaction Manager buyside UI. Rules consist of three components in Transaction Manager:

Level: Determines whether the rule runs at the Transaction level or the Transaction Line level of the Transaction. The level chosen for a rule dictates what fields can be used in the definition of conditions and actions in the rule. Transaction level rules can use Transaction level fields in both the conditions and actions in the rule. Transaction Line level rules can use Transaction level and Transaction Line level fields in the conditions of the rule, but only Transaction Line level fields in the actions in the rule.

Conditions: Conditions determine when a rule will execute its actions. If the conditions defined for a rule evaluate to TRUE, then the rule actions will be executed. If the conditions for a rule evaluate to FALSE, then rule actions will not execute. There are 5 different way to implement conditions in a rule:

-   Always True: This will allow the rule to execute every time a buyside user makes a change to the Transaction Manager buyside UI.
-   Any Conditions are Met: This will allow the rule to execute if any single condition in the condition list evaluates to TRUE \(Conditions are logically OR’d together\).
-   All Conditions are Met: This allows the rule to execute if all the conditions in the condition list evaluate to TRUE \(conditions are logically AND’d together\).
-   Custom Logic: allows the use of parenthesis and the mixture of ANDs and ORs to create a custom logic evaluation of the conditions in the condition list \(for example, If Cond\_1 AND \(Cond\_2 OR Cond\_3\)\).
-   Advanced Function: This allows the Administrator to write a script to determine if the rules should be executed. The Script will return either a value of TRUE or a value of FALSE.

Actions– Actions determine what the rule will do when the rule is executed. There are five kinds of actions that a rule can execute:

-   Hiding: A Hiding action allows the Administrator to conditionally hide a field in the buyside UI layout.
-   Message: A Message action allows the Administrator to display text message to the buyside user in the buyside UI layout.
-   Exclusion: Exclusion actions allow the Administrator to hide/disable menu option in a picklist field.
-   Inclusion: Inclusion actions allow the Administrator to display menu option in a picklist field.
-   Determination: Determination actions allow the Administrator to set or clear the value of a field in the buyside UI layout

Each type of action has a unique set of rule parameters that must be defined. We will review the various parameters for each action type later in this article.

## Create a new rule

Navigate to the Transaction Manager Admin UI. In the Admin menu Click "Related Rules". To create a new rule, click the **+ New Rule** button.

![Create a New rule](../images/cpq-txn-mgr-rules-create-new-rule-1.jpeg)

On the New Rule popup enter the name of the new rule, verify the Variable Name \(use the Pencil icon on the right if you would like to change the Variable Name\).

Click either Transaction or Transaction Line to determine the level of this new rule.

Click the Save button to save the new rule.

![Create a New rule](../images/cpq-txn-mgr-rules-create-new-rule-2.jpeg)

On the rule Editor page you can modify the name of the rule, or the Description. Above the Variable Name field is the Active toggle, this allows you to make the rule Active or Inactive.

Below the Description field is the Conditions area. Clicking the Take Action When menu displays the various options you have for implementing the conditions for this new rule. The meaning of each of these values is described earlier in this article. Select the conditions method to use for this new rule.

![Create a New rule](../images/cpq-txn-mgr-rules-create-conditions-3.jpeg)

If you change the value of the Take Action When menu from the default value ofAlways, you will then need to specify the list of conditions that will determine if this rule executes or not. You can define one or more individual conditions for a rule. To define a condition use the Enter/Select a field menu to select the Transaction Manager field to test, then choose the operator for the condition in the Equals menu, then set the test value for the field in the Enter/Select a Value menu to determine whether the condition will be TRUE or FALSE. Use the +Add Condition button to add multiple conditions to the rule.

![Transaction Manager: rules and rule groupings](../images/cpq-txn-mgr-rules-create-conditions-4.jpeg)

Once the conditions are defined, then you can define the actions that the rule will execute. As with conditions you can add one or more actions to a given rule, and different types of actions can be included in the same rule.

To add an action, select the type of action you want to add and click it in the Actions area. You will then be taken to the specific Action Type parameter set to define the action. A review of the different action parameter sets follows.

![New rule actions](../images/cpq-txn-mgr-rules-create-actions-5.jpeg)

## The Hiding action

The Hiding action allows you to hide a field on the buyside layout. The only parameter for this type of action is the field to hide from view. Use the field search box to identify the field to be hidden.

![The Hiding action](../images/cpq-txn-mgr-rules-hiding-action.jpeg)

## The Message action

A Message action enables the display of a text message to the buyside user in the Transaction Manager layout. There are four message types, which can be found in the **I want to display** menu:

Info Message: Uses a circular blue icon and blue message text, icon and text color cannot be changed.

Warning Message - Uses a triangular yellow icon and yellow message text, icon and text color cannot be changed.

Error Message - Uses a triangular red icon and red message text, icon and text color cannot be changed.

Custom Message: Admin has control over the icon used with the display of the message as well as the text color of the message.

![The Message action](../images/cpq-txn-mgr-rules-message-action.jpeg)

Use the **Show the message on** field to define where on the buyside layout you want the message to appear. The message is often attached to a field, but can also be attached to a Layout component like a Tier or Columnset.

The **Message Content** field allows you to write out the Message you would like to be displayed to the buyside user. Clicking the **Advanced** toggle allows the Administrator the ability to write a script to build the Message that will be displayed in the layout. Use the **When Message is Displayed** field to determine whether the Transaction can be saved when the Message is displayed to the buyside user.

## The Exclusion/Inclusion action

Exclusion and Inclusion actions allow you to manipulate the visibility and use of the menu options defined for a given picklist field. Exclusion actions allow you to hide/disable menu options in the layout, while Inclusion actions allow you to show/enable menu options in the layout. Exclusion and Inclusion actions use the same set of parameters.

Use the **For this Field** menu to select the picklist field whose menu options you will Exclude or Include in the menu.

![The Exclusion/Inclusion action](../images/cpq-txn-mgr-rules-exclusion-action.jpeg)

Use the **I want to exclude/include these options** menu to select the specific menu options for the selected picklist field that will be Excluded or Included in the menu. You can select multiple options; they are selected one at a time. Use the Advanced toggle to allow for the writing of script to determine which menu options will be part of the rule execution.

Use the **For excluded options** menu to determine how excluded menu options will be treated. \(in an Inclusion action, any menu options not included in the menu are treated as excluded menu options\):

-   Hide them: these excluded item will be hidden from the user’s view on the buyside UI.
-   Disable them: these excluded options will appear in the menu, but will be grayed out and not selectable.

Use the If any are already selected menu to determine what to do in the instance that the buyside user has already selected an item in the menu that is excluded by the rule, but the selection was made prior to the rule being executed:

-   Leave Unchanged– This option will leave the excluded item as the selected item in the menu since it was selected prior to the execution of the rule.
-   Deselect Them– This option deselects the excluded option, forcing the user to re-select an option from the current menu options.
-   Select the first valid option instead– this option deselects the excluded option but replaces it with the first available option currently in the menu following the execution of the rule.

## The Determination action

Determination actions allow you to set and clear the value of a field in Transaction Manager.

Use the **For this Field** menu to search for and select the field for the rule to act upon.

![The Determination action](../images/cpq-txn-mgr-rules-determination-action-1.jpeg)

Next we need to define what we want to do with the field we have chosen. In the fields under **I want to…** you define whether you want to **Set** the value of the chosen field or Clear the value of the chosen field, and whether you will **Allow** or **Prevent** the buyside user from editing the value of the chosen field after it has been modified by the rule.

In the **If user has modified values** menu you can choose whether you want to **Retain** a value in the chosen field that was modified by the buyside user or if you want to Override that value with the value in the rule. Further, if you decide to Retain the modified value from the buyside user you can use the **When user values are retained** menu to define if you want to **Show** the buyside user a message with a recommendation about the value of the chosen field or not.

![The Determination action](../images/cpq-txn-mgr-rules-determination-action-2.jpeg)

Finally, you need to define the value that would be assigned to the chosen field. You can use the **Use this value** field define the value you want to place in the chosen field. You can also use the **Advanced** toggle to allow the Administrator to write a script that will determine the value that will be placed in the chosen field.

![The Determination action](../images/cpq-txn-mgr-rules-determination-action-3.jpeg)

## Rule groupings

Rule groupings are collections of rules designed for easier association and access, consisting of rules that are intended to be executed together. A rule grouping can contain both Transaction level and Transaction Line-level rules.

Rule groupings will then be utilized in Stages and/or Events to link groups of rules for execution. Each stage can have 0 to N rule groupings associated with it, determining which rules will execute when a user makes any changes to a specific field in that stage. The Admin will have to associate a rule grouping with a Stage and/or Event for rules to execute. For instructions on how to associate a rule grouping to a Stage or Event, see the following articles:

[Transaction Manager: Events](transaction-manager-events.md)

[Transaction Manager: Stages](transaction-manager-stages.md)

## Creating a rule grouping

To begin, click **Rule Groupings** in the Admin menu, then click the **+ New Rule Grouping** button.

![Creating a rule grouping](../images/cpq-txn-mgr-rules-grouping-new-1.jpeg)

In the **New Rule Grouping** popup, provide a **Variable Name** for the new rule grouping. Once the **Variable Name** is satisfactory, click the **Save** button.

![Creating a rule grouping](../images/cpq-txn-mgr-rules-grouping-new-2.jpeg)

Next we need to associate rules with the new rule grouping. When you click **Save** in the New Rule Grouping popup, you are taken to the rule Grouping Editor page. Here you need to click the **+ Associate Rules** button.

![Creating a rule grouping](../images/cpq-txn-mgr-rules-grouping-editor-3.jpeg)

Clicking the **+ Associate Rules** button will open a slideout where you can select the individual rules that you want to include in the new rule grouping. Click the “+” sign to the left of a rule in the **Results** column of rules and the rule will be moved over to the **Selected** column. Do this for each rule you want to include in the rule Grouping.

![Associating a rule grouping](../images/cpq-txn-mgr-rules-grouping-associate-4.jpeg)

![Associating rules](../images/cpq-txn-mgr-rules-grouping-associate-5.jpeg)

Once all rules have been selected, click the **Done** button. You will be taken back to the rule Grouping Editor page where you will see the rules that have been added to the group.

![Associating rules](../images/cpq-txn-mgr-rules-grouping-approved-6.jpeg)

## Rule Aggregates

Aggregates are script functions that you can use in Advanced Functions in Rule Determination action. These functions enhance automation, optimize pricing calculations, and improve data organization in quoting and transaction workflows. Aggregates were created to optimize Rule Engine performance in Transaction Manager. Aggregate functions are used to perform various math calculations on Transaction Line fields. Results of these calculations are stored in either a Transaction/Header field or in a Transaction Line field.

Note: Aggregates elements will always run, including in cases when the aggregate function has no children. If an aggregate function does not have a default set and there are no children, the value returned by an aggregate will be null, and for lookups, the value returned will be an empty array. To avoid errors, set a default or handle the null/empty array responses.

Rule aggregates include the following categories:

-   Avg, Count, Min, Max, Sum
-   AvgIf, CountIf, SumIf
-   SumChildren
-   Lookup

## Avg, Count, Min, Max, Sum

These aggregate functions will aggregate the chosen Transaction Line field value for all Lines and store the result in a chosen Header field \(the target field of the Determination action\):

`return txn.line.functions.<function>(txn.line.<fieldVarName>)`

Values for &lt;function&gt; include avgField, countField, minField, maxField, and sumField.

## AvgIf, CountIf, SumIf

These aggregate functions will apply a filter to the chosen Transaction Line field value for all Lines, then perform the calculation on the remaining lines and store result in a chosen Header field \(the target field of the Determination action\):

`txn.line.functions.<function>(txn.line.<fieldVarName>, <condition> [, <default>])`

Values for &lt;function&gt; include avgFieldIf, countFieldIf, and sumFieldIf.

&lt;condition&gt; is set to something like:

-   booleanField = true OR
-   txn.line.functions.sumChildrenField\(txn.line.&lt;fieldVarName&gt;\)&gt; 0

If the default value is not defined, then `null` is returned when there are no children to aggregate.

Remember that conditional checks for text are case sensitive.

## Use case example: Summing list prices for sales BOM type

In a draft-stage sample transaction as shown below, I want to sum the list prices of items whose BOM type isSALES. The BOM type is a system-derived line field reflecting the type set first when the configuration item was created.

![Rule Aggregates](../images/cpq-txn-mgr-rules-aggregates-use-case-1.png)

Steps:

1.  Create a header field named **Total Sales Type Price**.

    ![Total Sales Type Price](../images/cpq-txn-mgr-rules-aggregates-use-case-2.png)

2.  Add it to the layout and deploy the transaction.

    ![deploy the transaction](../images/cpq-txn-mgr-rules-aggregates-use-case-3.png)

3.  Set up a determination rule using the`sumFieldIf` function, applied at the draft stage with the following script:

    ```
    return txn.line.functions.sumFieldIf(txn.line.pricing.list,
            txn.line.configuration.item.bomType == 'SALES');
    ```

    **Note:** The conditional check is case sensitive. Use `SALES`, not `sales`. Incorrect casing yields no error, but results in a sum of 0 as in the use case there are no lines where bom type is Sales.

    ![deploy the transaction](../images/cpq-txn-mgr-rules-aggregates-use-case-4.png)

4.  Deploy and reload the transaction. The field correctly returns the total of matching line prices: $46,000 \(from 0, 40,000, 2,500, 1,000, 2,500\).

    ![deploy the transaction](../images/cpq-txn-mgr-rules-aggregates-use-case-5.jpeg)


## SumChildren

This aggregate function will aggregate the chosen Transaction Line field value for all child lines and store the result in the immediate parent line-level field of those child lines \(the target field of the Determination action\):

`txn.line.functions.sumChildrenField(txn.line.<fieldVarName>)`

## Lookup

These aggregate functions focus on retrieving specific values rather than computing totals. They return either a single value or an array of values, allowing users to extract key information dynamically for use in pricing calculations, validation rules, and output documents:

Basic lookup functions:

-   `txn.line.functions.lookupField(<field>)`

    Retrieves an array of values from the specified field across all transaction lines.

-   `txn.line.functions.lookupFirstField(<field> [, <default>])`

    Retrieves the first matching field value. If none is found, returns the optional default.

-   `txn.line.functions.lookupChildrenField(<field>)`

    Retrieves an array of values from child line items.

-   `txn.line.functions.lookupFirstChildrenField(<field> [, <default>])`

    Retrieves the first matching value from child line items, with an optional default.


Conditional checks for text are case sensitive. Conditional lookup functions:

-   `txn.line.functions.lookupFieldIf(<field>, <condition>)`

    Retrieves an array of field values based on a condition.

-   `txn.line.functions.lookupFirstFieldIf(<field>, <condition> [, <default>])`

    Retrieves the first matching field value based on a condition, with an optional default.

-   `txn.line.functions.lookupChildrenFieldIf(<field>, <condition>)`

    Retrieves an array of values from child line items based on a condition.

-   `txn.line.functions.lookupFirstChildrenFieldIf(<field>, <condition> [, <default>])`

    Retrieves the first matching child line item field value based on a condition, with an optional default.


Naming Structure:

Functions follow a structured naming convention for clarity and consistency:

-   Base Function:`lookup` \(returns an array\),`lookupFirst` \(returns a single value\).
-   Context: No context \(all lines\) or`Children` \(child line items only\).
-   Object:`Field` \(applies to a field lookup only\).
-   Condition: No condition or`If` \(conditional lookup\).

Intermediate fields:

Lookup functions automatically store retrieved values in intermediate fields, making them readily available for further calculations and automation. This ensures seamless integration with pricing rules, approvals, and output documents.

Benefits of Intermediate fields:

-   Efficiency: Reduces redundant calculations by storing commonly referenced values.
-   Data Integrity: Maintains a consistent set of field values across pricing and quoting processes.
-   Automation: Enables dynamic updates to dependent fields, ensuring real-time accuracy in pricing and approvals.

Managing Deleted Lines in Aggregations:

-   Lookup aggregations dynamically adjust when quoted line items are removed.
-   The system ensures that references to deleted transaction lines are cleared, maintaining data accuracy in recalculated pricing and discounts.

Examples:

```
var taxCodes =
              txn.line.functions.lookupFieldIf("taxCode", txn.line.amount > 0);
            var firstPrice =
            txn.line.functions.lookupFirstField("price", 0);   var childService =
            txn.line.functions.lookupChildrenField("serviceType");   var totalTax =
            txn.line.functions.lookupFirstField(txn.line.taxAmount, 0);   return totalTax * 1.05; //
            Applies a 5% surcharge based on retrieved tax amount
```

