---
title: Transaction Manager: Rules and rule groupings
description: Rules in Transaction Manager are similar to configuration rules. You can also group rules together when they are intended to run together.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Rules and rule groupings

Rules in Transaction Manager are similar to configuration rules. You can also group rules together when they are intended to run together.

As in configuration, rules in Transaction Manager govern what actions are taken when a user makes an input into the Transaction Manager buyside UI. Rules consist of three components in Transaction Manager: level, conditions, and actions.

The level determines whether the rule runs at the transaction level or the transaction line level. The level dictates which fields can be used in the definition of conditions and actions in the rule.

Conditions determine when a rule executes its actions. If the conditions defined for a rule evaluate to TRUE, the rule actions are executed. If the conditions for a rule evaluate to FALSE, rule actions do not execute.

Actions determine what rules do when they are executed.

Each type of action has a unique set of rule parameters that must be defined. Actions are more fully described in the sections following.

## Create a new rule

In the Transaction Manager Admin menu, click **Related Rules**. To create a new rule, click **+ New Rule**.

![Create a New rule](../images/cpq-txn-mgr-rules-create-new-rule-1.jpeg)

In the **New Rule** popup window, enter the name of the new rule, and verify the variable name. To change the variable name, click the pencil icon on the right.

To set the level of the new rule, click either **Transaction** or **Transaction Line**.

-   Transaction-level rules can use transaction-level fields in both the conditions and actions in the rule.
-   Transaction line-level rules can use transaction-level and transaction line-level fields in the conditions of the rule, but only transaction line-level fields in the actions in the rule.

Click **Save**.

![Create a New rule](../images/cpq-txn-mgr-rules-create-new-rule-2.jpeg)

On the rule editor page, you can modify the name and the description of the rule. The Active toggle lets you activate or deactivate the rule.

Below the Description field is the Condition area. Clicking the **Take Action When** menu displays options for implementing the conditions for this new rule. Select the conditions method to use for this new rule.

-   **Always True** executes the rule every time a user makes a change to the Transaction Manager buyside UI.
-   **Any Conditions are Met** executes the rule if any condition evaluates to TRUE. \(Conditions are logically OR’d together.\)
-   **All Conditions are Met** executes the rule if all the conditions evaluate to TRUE. \(Conditions are logically AND’d together.\)
-   **Custom Logic** enables the use of parenthesis and a mixture of ANDs and ORs to create a custom logic evaluation of the conditions in the condition list \(for example, If Cond\_1 AND \(Cond\_2 OR Cond\_3\)\).
-   **Advanced Function** enables the admin to write a script to determine whether the rules should be executed. The script returns a value of either TRUE or FALSE.

![Create a New rule](../images/cpq-txn-mgr-rules-create-conditions-3.jpeg)

If you change the value of the **Take Action When** menu from the default value of **Always**, you need to specify the list of conditions that determine whether the rule executes. You can define one or more individual conditions for a rule. To define a condition use the Enter/Select a field menu to select the Transaction Manager field to test, then choose the operator for the condition in the Equals menu, then set the test value for the field in the Enter/Select a Value menu to determine whether the condition is TRUE or FALSE. Use the +Add Condition button to add multiple conditions to the rule.

![Transaction Manager: rules and rule groupings](../images/cpq-txn-mgr-rules-create-conditions-4.jpeg)

Once the conditions are defined, then you can define the actions that the rule executes. As with conditions you can add one or more actions to a rule, and different types of actions can be included in the same rule.

To add an action, select the type of action to add and click it in the Actions area. You are then be taken to the Action Type parameter set to define the action.

-   A hiding action conditionally hides a field.
-   A message action displays a text message to the buyside user.
-   An exclusion action hides or disables a menu option in a picklist field.
-   An inclusion action displays a menu option in a picklist field.
-   A determination action sets or clears the value of a field.

![New rule actions](../images/cpq-txn-mgr-rules-create-actions-5.jpeg)

A review of the different action parameter sets follows.

## The Hiding action

The Hiding action lets you hide a field on the buyside layout. The only parameter for this type of action is the field to hide. Use the field search box to identify the field.

![The Hiding action](../images/cpq-txn-mgr-rules-hiding-action.jpeg)

## The Message action

A Message action enables the display of a text message to the buyside user in the Transaction Manager layout. Four message types are found in the **I want to display** menu:

-   An info message uses a circular blue icon and blue message text. The icon and text color cannot be changed.
-   A warning message uses a triangular yellow icon and yellow message text. The icon and text color cannot be changed.
-   An error message uses a triangular red icon and red message text. The icon and text color cannot be changed.
-   Custom messages can have any icon and text color.

![The Message action](../images/cpq-txn-mgr-rules-message-action.jpeg)

Use the **Show the message on** field to define where on the buyside layout you want the message to appear. The message is often attached to a field, but it can also be attached to a layout component such as a tier or a columnset.

The **Message Content** field lets you write the message to be displayed to the buyside user. Setting the **Advanced** toggle lets you write a script to build the message. Use the **When Message is Displayed** field to determine whether the transaction can be saved when the message is displayed.

## The Exclusion/Inclusion action

Exclusion and Inclusion actions let you set the visibility and the use of the menu options that are defined for a picklist field. Exclusion actions let you hide or disable menu options. Inclusion actions let you show or enable menu options. Exclusion and inclusion actions use the same set of parameters.

Use the **For this Field** menu to select the picklist field whose menu options to exclude or include in the menu.

![The Exclusion/Inclusion action](../images/cpq-txn-mgr-rules-exclusion-action.jpeg)

Use the **I want to \[exclude\|include\] these options** menu to select the picklist menu options to exclude or include in the menu. You can select multiple options one at a time. Use the **Advanced** toggle to use a script to determine which menu options are part of the rule execution.

Use the **For excluded options** menu to determine how excluded menu options are treated. \(In an Inclusion action, menu options not included in the menu are treated as excluded menu options.\) Choose **hide them** to hide the options. Choose **disable them** to retain them in menu in a disabled state.

Use the **If any are already selected** menu to determine what to do when the user has already selected an excluded menu item when the rule is executed:

-   **leave unchanged** leaves the excluded item as the selected item.
-   **deselect them** deselects the excluded option, forcing the user to select another option.
-   **select the first valid option instead** deselects the excluded option but replaces it with the first available option in the menu following the execution of the rule.

## The Determination action

Determination actions enable you to set and clear the value of a field in Transaction Manager.

Use the **For this Field** menu to search for and select the field for the rule to act upon.

![The Determination action](../images/cpq-txn-mgr-rules-determination-action-1.jpeg)

Under **I want to…**, define whether to set or clear the value of the field and whether to allow or prevent the user from editing its value after it has been modified by the rule.

In the **If user has modified values** menu, you can choose whether to retain a value in the field that the user modified or to override the value with the value in the rule. To retain the value that the user entered, use the **When user values are retained** menu to define whether to show the user a message with a recommendation about the value of the field.

![The Determination action](../images/cpq-txn-mgr-rules-determination-action-2.jpeg)

Finally, define the value to assign to the field. The **Use this value** field defines this value. You can use the **Advanced** toggle to enable a script to determine the value.

![The Determination action](../images/cpq-txn-mgr-rules-determination-action-3.jpeg)

## Rule groupings

Rule groupings are collections of rules to be executed together. A rule grouping can contain both transaction-level and transaction line-level rules.

Rule groupings are used in stages and events to link groups of rules for execution. Each stage can have any number of rule groupings associated with it, determining which rules execute when a user makes changes to a field in the stage. For rules to execute, the admin must associate a rule grouping with a stage or event. For instructions on how to do so, see the following articles:

[Transaction Manager: Events](transaction-manager-events.md)

[Transaction Manager: Stages](transaction-manager-stages.md)

## Creating a rule grouping

To begin, click **Rule Groupings** in the Admin menu, and then click **+ New Rule Grouping**.

![Creating a rule grouping](../images/cpq-txn-mgr-rules-grouping-new-1.jpeg)

In the **New Rule Grouping** window, enter a variable name for the new rule grouping, and click **Save**.

![Creating a rule grouping](../images/cpq-txn-mgr-rules-grouping-new-2.jpeg)

The rule Grouping Editor page opens. Click **+ Associate Rules**.

![Creating a rule grouping](../images/cpq-txn-mgr-rules-grouping-editor-3.jpeg)

A slideout pane appears, where you can select the rules to include in the new rule grouping. Click **+** in the **Results** column to move a rule to the **Selected** column. Repeat this for each rule to include in the rule grouping.

![Associating a rule grouping](../images/cpq-txn-mgr-rules-grouping-associate-4.jpeg)

![Associating rules](../images/cpq-txn-mgr-rules-grouping-associate-5.jpeg)

When you have finished selecting rules, click **Done**. You are taken back to the rule grouping editor page, where you see the rules that have been added to the group.

![Associating rules](../images/cpq-txn-mgr-rules-grouping-approved-6.jpeg)

## Rule Aggregates

Aggregates are script functions for use in a rule determination action. Aggregates can enhance automation, optimize pricing calculations, and improve data organization in quoting and transaction workflows and were created to optimize rule engine performance in Transaction Manager.

Aggregate functions perform various math calculations on transaction line fields. Results of these calculations are stored in either a transaction \(header\) field or in a transaction line field.

**Note:** Aggregates always run, even in cases when the aggregate function has no children. If an aggregate function does not have a default set and there are no children, the value returned by an aggregate is null, and for lookups, the value returned is an empty array. To avoid errors, set a default or handle empty array responses.

Rule aggregates include the following categories:

-   Avg, Count, Min, Max, Sum
-   AvgIf, CountIf, SumIf
-   SumChildren
-   Lookup

## Avg, Count, Min, Max, Sum

These aggregate functions aggregate the transaction line field value for all lines and store the result in a header field \(the target field of the determination action\):

`return txn.line.functions.<function>(txn.line.<fieldVarName>)`

Values for &lt;function&gt; include avgField, countField, minField, maxField, and sumField.

## AvgIf, CountIf, SumIf

These aggregate functions apply a filter to the transaction line field value for all lines, then perform the calculation on the remaining lines, storing the result in a header field \(the target field of the determination action\):

`txn.line.functions.<function>(txn.line.<fieldVarName>, <condition> [, <default>])`

Values for &lt;function&gt; include avgFieldIf, countFieldIf, and sumFieldIf.

&lt;condition&gt; can be set to an expression such as the following:

-   booleanField = true
-   txn.line.functions.sumChildrenField\(txn.line.&lt;fieldVarName&gt;\)&gt; 0

If there are no children to aggregate and the default value is undefined, the function returns `null`.

Conditional checks for text are case sensitive.

## Use case example: Summing list prices for sales BOM type

The draft-stage sample transaction below calculates the sum of the list prices of items whose BOM type isSALES. The BOM type is a system-derived line field that reflects the type set first when the configuration item was created.

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

    **Note:** The conditional check is case sensitive. Use `SALES`, not `sales`. Incorrect casing yields no error, but results in a sum of 0 because in the use case no lines have a BOM type of Sales.

    ![deploy the transaction](../images/cpq-txn-mgr-rules-aggregates-use-case-4.png)

4.  Deploy and reload the transaction. The field correctly returns the total of matching line prices: $46,000 \(from 0, 40,000, 2,500, 1,000, 2,500\).

    ![deploy the transaction](../images/cpq-txn-mgr-rules-aggregates-use-case-5.jpeg)


## SumChildren

This aggregate function aggregates the transaction line field value for all child lines and stores the result in the immediate parent line-level field of the child lines \(the target field of the determination action\):

`txn.line.functions.sumChildrenField(txn.line.<fieldVarName>)`

## Lookup

These aggregate functions retrieve values instead of computing totals. They return either a single value or an array of values, enabling users to extract key information dynamically for use in pricing calculations, validation rules, and output documents.

Basic lookup functions include:

-   `txn.line.functions.lookupField(<field>)`

    Retrieves an array of values from the specified field across all transaction lines.

-   `txn.line.functions.lookupFirstField(<field> [, <default>])`

    Retrieves the first matching field value. If none is found, returns the optional default.

-   `txn.line.functions.lookupChildrenField(<field>)`

    Retrieves an array of values from child line items.

-   `txn.line.functions.lookupFirstChildrenField(<field> [, <default>])`

    Retrieves the first matching value from child line items, with an optional default.


Conditional checks for text are case sensitive. Conditional lookup functions include:

-   `txn.line.functions.lookupFieldIf(<field>, <condition>)`

    Retrieves an array of field values based on a condition.

-   `txn.line.functions.lookupFirstFieldIf(<field>, <condition> [, <default>])`

    Retrieves the first matching field value based on a condition, with an optional default.

-   `txn.line.functions.lookupChildrenFieldIf(<field>, <condition>)`

    Retrieves an array of values from child line items based on a condition.

-   `txn.line.functions.lookupFirstChildrenFieldIf(<field>, <condition> [, <default>])`

    Retrieves the first matching child line item field value based on a condition, with an optional default.


Functions follow a structured naming convention for clarity and consistency.

-   `lookup` returns an array. `lookupFirst` returns a single value.
-   Context: No context \(all lines\), or `Children` \(child line items only\).
-   Object: `Field` \(applies only to a field lookup\).
-   Condition: No condition, or `If` \(conditional lookup\).

Lookup functions store retrieved values in intermediate fields, making them available for further calculations and automation. This enables integration with pricing rules, approvals, and output documents.

The benefits of intermediate fields include the following:

-   They minimize redundant calculations by storing commonly referenced values
-   They maintain a consistent set of field values across pricing and quoting processes
-   They enable dynamic updates to dependent fields, ensuring real-time accuracy in pricing and approvals

Lookup aggregations dynamically adjust when quoted line items are removed. The system ensures that references to deleted transaction lines are cleared, maintaining data accuracy in recalculated pricing and discounts. See the following examples.

```
var taxCodes =
              txn.line.functions.lookupFieldIf("taxCode", txn.line.amount > 0);
            var firstPrice =
            txn.line.functions.lookupFirstField("price", 0);   var childService =
            txn.line.functions.lookupChildrenField("serviceType");   var totalTax =
            txn.line.functions.lookupFirstField(txn.line.taxAmount, 0);   return totalTax * 1.05; //
            Applies a 5% surcharge based on retrieved tax amount
```

**Related topics**  


[Transaction Manager: Events](transaction-manager-events.md)

[Transaction Manager: Stages](transaction-manager-stages.md)

