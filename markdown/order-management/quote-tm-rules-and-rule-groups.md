---
title: Quote transaction rules and rule groupings
description: Rules in ServiceNow Quote Experience evaluate conditions and perform actions on quote fields and layouts. Rule groupings bundle rules together to run at stages and events in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-rules-and-rule-groups.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 8
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Quote transaction rules and rule groupings

Rules in ServiceNow Quote Experience evaluate conditions and perform actions on quote fields and layouts. Rule groupings bundle rules together to run at stages and events in ServiceNow CPQ.

Rules in ServiceNow Quote Experience govern what actions occur when a user interacts with the quote interface. Rules are similar to configuration rules — each rule has three components: level, conditions, and actions.

## Rule components

-   **Level**

    Determines whether the rule runs at the transaction level or the transaction line level. The level dictates which fields can be used in conditions and actions.

    -   Transaction-level rules can use transaction-level fields in both conditions and actions.
    -   Transaction line-level rules can use transaction-level and line-level fields in conditions, but only transaction line-level fields in actions.
-   **Conditions**

    Determine when a rule executes its actions. If conditions evaluate to TRUE, actions execute. If conditions evaluate to FALSE, actions don't execute. The following condition logic options are available.

    -   **Always True**

        Executes the rule every time a user makes a change to the quote interface.

    -   **Any Conditions are Met**

        Executes the rule if any condition evaluates to TRUE. Conditions are logically OR'd together.

    -   **All Conditions are Met**

        Executes the rule if all conditions evaluate to TRUE. Conditions are logically AND'd together.

    -   **Custom Logic**

        Enables parentheses and a mixture of AND and OR operators to build a custom logic expression — for example, `Cond_1 AND (Cond_2 OR Cond_3)`.

    -   **Advanced Function**

        Enables a script that returns `TRUE` or `FALSE` to control whether the rule executes.

    Each individual condition tests a field against an operator and a value. Use **+ Add Condition** to add multiple conditions to a rule.

-   **Actions**

    Define what the rule does when it executes. A rule can have one or more actions, and a single rule can include actions of different types. For full parameter details for each action type, see the Action types section below.


## Action types

The following action types are available in ServiceNow Quote Experience rules. Each type has a distinct set of parameters configured in the rule editor.

-   **Hiding**

    Hides a field on the quote layout when the rule conditions are met. The only parameter is the field to hide — use the field search box in the action editor to select it.

-   **Message**

    Displays a text message to the user on the quote layout. The following parameters are available.

    -   **Message type**

        Set using the **I want to display** menu. The four message types are:

        -   **Info** — circular blue icon and blue message text. Icon and text color cannot be changed.
        -   **Warning** — triangular yellow icon and yellow message text. Icon and text color cannot be changed.
        -   **Error** — triangular red icon and red message text. Icon and text color cannot be changed.
        -   **Custom** — configurable icon and text color.
    -   **Message location**

        Set using the **Show the message on** field. Messages can be attached to a field, or to a layout component such as a tier or a columnset.

    -   **Message content**

        Enter the text to display in the **Message Content** field. Enable the **Advanced** toggle to use a script to build the message content dynamically.

    -   **Save behavior**

        Use the **When Message is Displayed** field to determine whether the transaction can be saved when the message is visible.

-   **Exclusion**

    Hides or disables one or more menu options in a picklist field. Exclusion and Inclusion actions share the same parameter set.

    -   **Target field**

        Select the picklist field whose options to exclude using the **For this Field** menu.

    -   **Options to exclude**

        Select the picklist options to exclude using the **I want to exclude these options** menu. Select options one at a time. Enable the **Advanced** toggle to use a script to determine which options are excluded.

    -   **Excluded option treatment**

        Use the **For excluded options** menu to choose how excluded options appear:

        -   **Hide them** — removes excluded options from the menu.
        -   **Disable them** — retains excluded options in the menu in a disabled state.
    -   **Behavior when excluded option is already selected**

        Use the **If any are already selected** menu to control what happens when the user has already selected an option that the rule excludes:

        -   **Leave unchanged** — retains the excluded item as the selected value.
        -   **Deselect them** — removes the selection and requires the user to choose another option.
        -   **Select the first valid option instead** — removes the selection and replaces it with the first available option after the rule executes.
-   **Inclusion**

    Shows or enables one or more menu options in a picklist field. Inclusion and Exclusion actions share the same parameter set — in an Inclusion action, options not specified for inclusion are treated as excluded. For parameter descriptions, see the Exclusion action above.

-   **Determination**

    Sets or clears the value of a field. The following parameters are available.

    -   **Target field**

        Select the field to act on using the **For this Field** menu.

    -   **Set or clear**

        Under **I want to…**, define whether to set a value or clear the field, and whether to allow or prevent the user from editing the field after the rule modifies it.

    -   **User-modified value handling**

        The **If user has modified values** menu controls whether to retain a value the user already entered or override it with the rule's value. When user values are retained, the **When user values are retained** menu lets you optionally show the user a recommendation message about the field value.

    -   **Value to assign**

        Define the value in the **Use this value** field. Enable the **Advanced** toggle to use a script — including aggregate functions — to calculate the value.


## Aggregate functions in determination actions

Aggregate functions are script functions available in determination rule actions. They perform math calculations on transaction line fields and store results in a header field or a transaction line field. Aggregates enhance automation, optimize pricing calculations, and improve data organization in quoting workflows.

**Note:** Aggregate functions always run, even when they have no child lines to aggregate. If an aggregate function has no default value set and there are no children, it returns `null`. Lookup functions without children return an empty array. To avoid downstream errors, always set a default value or handle empty array responses in any logic that depends on aggregate output.

-   **Avg, Count, Min, Max, Sum**

    Aggregate the value of a transaction line field across all lines and store the result in the target header field.

    ```
    return txn.line.functions.<function>(txn.line.<fieldVarName>)
    ```

    Values for `<function>`: `avgField`, `countField`, `minField`, `maxField`, `sumField`.

-   **AvgIf, CountIf, SumIf**

    Apply a filter to the transaction line field values, then perform the calculation on the remaining lines and store the result in the target header field. Text conditional checks are case sensitive.

    ```
    txn.line.functions.<function>(txn.line.<fieldVarName>, <condition> [, <default>])
    ```

    Values for `<function>`: `avgFieldIf`, `countFieldIf`, `sumFieldIf`.

    Example condition expressions:

    -   `booleanField = true`
    -   `txn.line.functions.sumChildrenField(txn.line.<fieldVarName>) > 0`
    If there are no children to aggregate and the default value is undefined, the function returns `null`.

-   **SumChildren**

    Aggregates the value of a line field across all child lines and stores the result in the immediate parent line field.

    ```
    txn.line.functions.sumChildrenField(txn.line.<fieldVarName>)
    ```

-   **Lookup functions**

    Retrieve values rather than computing totals. Lookup functions return either a single value or an array of values from transaction line fields, enabling dynamic use in pricing calculations, validation rules, and output documents. Lookup aggregations dynamically adjust when line items are removed — references to deleted transaction lines are cleared automatically.

    Lookup functions follow a structured naming convention.

    -   `lookup` returns an array. `lookupFirst` returns a single value.
    -   Context: no context suffix = all lines. `Children` suffix = child line items only.
    -   Condition: no suffix = no filter. `If` suffix = conditional filter applied.
    Basic lookup functions:

    -   `txn.line.functions.lookupField(<field>)` — array of values from the specified field across all lines.
    -   `txn.line.functions.lookupFirstField(<field> [, <default>])` — first matching value, with optional default.
    -   `txn.line.functions.lookupChildrenField(<field>)` — array of values from child line items.
    -   `txn.line.functions.lookupFirstChildrenField(<field> [, <default>])` — first matching value from child line items, with optional default.
    Conditional lookup functions \(text comparisons are case sensitive\):

    -   `txn.line.functions.lookupFieldIf(<field>, <condition>)`
    -   `txn.line.functions.lookupFirstFieldIf(<field>, <condition> [, <default>])`
    -   `txn.line.functions.lookupChildrenFieldIf(<field>, <condition>)`
    -   `txn.line.functions.lookupFirstChildrenFieldIf(<field>, <condition> [, <default>])`
    Lookup functions store retrieved values in intermediate fields, making them available for further calculations and automation. Using intermediate fields offers the following benefits.

    -   Minimizes redundant calculations by storing commonly referenced values.
    -   Maintains a consistent set of field values across pricing and quoting processes.
    -   Enables dynamic updates to dependent fields, ensuring real-time accuracy in pricing and approvals.
    Code examples:

    ```
    var taxCodes =
      txn.line.functions.lookupFieldIf("taxCode", txn.line.amount > 0);
    
    var firstPrice =
      txn.line.functions.lookupFirstField("price", 0);
    
    var childService =
      txn.line.functions.lookupChildrenField("serviceType");
    
    var totalTax =
      txn.line.functions.lookupFirstField(txn.line.taxAmount, 0);
    
    return totalTax * 1.05; // Applies a 5% surcharge based on retrieved tax amount
    ```


The following example calculates the sum of list prices for lines whose BOM type is `SALES`. The BOM type is a system-derived line field that reflects the type set when the configuration item was created.

The determination rule uses the `sumFieldIf` function at the draft stage with this script:

```
return txn.line.functions.sumFieldIf(
  txn.line.pricing.list,
  txn.line.configuration.item.bomType == 'SALES'
);
```

**Note:** The conditional check is case sensitive. Use `'SALES'`, not `'sales'`. Incorrect casing produces no error but returns a sum of 0 because no lines match.

With lines whose BOM types are SALES \(values 40,000 / 2,500 / 1,000 / 2,500\) and one non-SALES line \(0\), the field correctly returns **$46,000**.

## Rule groupings

Rule groupings are collections of rules that execute together. A rule grouping can contain both transaction-level and transaction line-level rules. Rule groupings are assigned to stages and events. When a stage is entered or an event fires, the associated rule groupings execute — including all rules within them that meet their conditions.

For rules to execute on a quote, an administrator must associate a rule grouping with a stage or event. Using rule groupings allows the same set of rules to be reused across multiple stages and events without duplicating rule definitions.

For information about creating a rule grouping and associating rules with it, see [Create a transaction rule grouping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-rule-grouping.md).

