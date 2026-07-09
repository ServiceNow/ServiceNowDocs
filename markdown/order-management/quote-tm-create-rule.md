---
title: Create a transaction rule
description: Create a rule in ServiceNow Quote Experience to define conditions and actions that control field behavior and layout presentation on a quote in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-create-rule.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 5
breadcrumb: [Rules and rule groupings, Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a transaction rule

Create a rule in ServiceNow Quote Experience to define conditions and actions that control field behavior and layout presentation on a quote in ServiceNow CPQ.

## Before you begin

The fields to use in rule conditions and actions must exist before creating the rule. For more information, see [Create a transaction field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-field.md).

Role required: admin

## About this task

Rules are created through the ServiceNow Quote Experience administration interface and consist of a level, conditions, and one or more actions. The rule editor opens after the initial save — the name, description, and active state are all editable there. For full descriptions of each action type and its parameters, see [Quote transaction rules and rule groupings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-rules-and-rule-groups.md).

## Procedure

1.  Create the rule
2.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** &gt; **Related Rules**.

3.  Select **+ New Rule**.

4.  In the **New Rule** window, enter the rule name and verify the variable name.

    The variable name is set in camel case from the name you enter. To use a custom variable name, select the pencil icon to the right of the **Variable Name** field.

5.  Select the rule level.

    -   Select **Transaction** to create a rule that uses transaction-level fields in both conditions and actions.
    -   Select **Transaction Line** to create a rule that can use transaction-level and line-level fields in conditions but only line-level fields in actions.
6.  Select **Save**.

    The rule editor opens. The **Name**, **Description**, and **Active** toggle are available at the top of the page.

7.  Enter a description of the rule in the **Description** field.

8.  Define the conditions
9.  In the **Take Action When** menu, select the condition logic method.

    |Option|Behavior|
    |------|--------|
    |**Always True**|Rule executes every time a user makes a change to the quote interface. No conditions to define.|
    |**Any Conditions are Met**|Rule executes if any one condition is TRUE \(OR logic\).|
    |**All Conditions are Met**|Rule executes only when all conditions are TRUE \(AND logic\).|
    |**Custom Logic**|Enables parentheses and mixed AND/OR logic — for example, `Cond_1 AND (Cond_2 OR Cond_3)`.|
    |**Advanced Function**|Enables a script that returns TRUE or FALSE to control rule execution.|

10. If using a condition-based logic method, select **+ Add Condition** and define each condition.

    For each condition, use the field menu to select the ServiceNow Quote Experience field to test, choose the operator, then set the test value. Repeat for each additional condition.

11. Add a hiding action
12. In the **Actions** area, select **Hiding**.

13. In the field search box, search for and select the field to hide on the quote layout.

14. Add a message action
15. In the **Actions** area, select **Message**.

16. In the **I want to display** menu, select the message type.

    -   Select **Info** for a circular blue icon and blue text.
    -   Select **Warning** for a triangular yellow icon and yellow text.
    -   Select **Error** for a triangular red icon and red text.
    -   Select **Custom** for a configurable icon and text color.
17. In the **Show the message on** field, specify where the message appears on the quote layout.

    Messages can be attached to a field, or to a layout component such as a tier or a columnset.

18. In the **Message Content** field, enter the text of the message to display.

    Enable the **Advanced** toggle to write a script that builds the message content dynamically.

19. In the **When Message is Displayed** field, set whether the transaction can be saved when the message is visible.

20. Add an exclusion or inclusion action
21. In the **Actions** area, select **Exclusion** or **Inclusion**.

22. In the **For this Field** menu, select the picklist field whose options to exclude or include.

23. In the **I want to exclude/include these options** menu, select the picklist options one at a time.

    Enable the **Advanced** toggle to use a script to determine which options are excluded or included.

24. In the **For excluded options** menu, choose how excluded options appear to the user.

    -   Select **Hide them** to remove excluded options from the menu.
    -   Select **Disable them** to retain excluded options in the menu in a disabled state.
25. In the **If any are already selected** menu, choose what happens when an excluded option is already selected by the user.

    -   Select **Leave unchanged** to keep the excluded item as the selected value.
    -   Select **Deselect them** to clear the selection and require the user to choose another option.
    -   Select **Select the first valid option instead** to clear the selection and replace it with the first available option after the rule executes.
26. Add a determination action
27. In the **Actions** area, select **Determination**.

28. In the **For this Field** menu, search for and select the field for the rule to act on.

29. Under **I want to…**, select whether to set or clear the field value, and whether to allow or prevent the user from editing the field after the rule modifies it.

30. In the **If user has modified values** menu, choose whether to retain the value the user entered or override it with the rule's value.

    When user values are retained, use the **When user values are retained** menu to optionally show the user a recommendation message about the field value.

31. In the **Use this value** field, define the value to assign.

    Enable the **Advanced** toggle to enter a script — including aggregate functions — to calculate the value. For aggregate function syntax and examples, see [Quote transaction rules and rule groupings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-rules-and-rule-groups.md).

32. Add additional actions and save
33. To add another action of any type to this rule, return to the **Actions** area and repeat the steps for the relevant action type above.

    A single rule can contain multiple actions of different types.

34. Verify that the **Active** toggle is enabled, then select **Save**.

    The rule is saved and appears in the Related Rules list. It is available to add to a rule grouping.


## What to do next

Add the rule to a rule grouping so that it can be assigned to stages and events. For more information, see [Create a transaction rule grouping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-rule-grouping.md).

