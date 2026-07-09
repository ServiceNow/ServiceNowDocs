---
title: Create a transaction field
description: Create a custom field in ServiceNow Quote Experience to capture additional data at the transaction \(header\) level or the transaction line level in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-create-field.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 5
breadcrumb: [Fields, Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a transaction field

Create a custom field in ServiceNow Quote Experience to capture additional data at the transaction \(header\) level or the transaction line level in ServiceNow CPQ.

## Before you begin

Role required: admin

## About this task

Fields created through the ServiceNow Quote Experience administration interface are automatically associated with the blueprint. The variable name is set at creation and cannot be changed afterward — to change a variable name, delete the field and re-add it. The field editor that opens after the initial save varies by field type — the following steps cover all five types.

## Procedure

1.  Create the field
2.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** &gt; **Associated Fields**.

3.  Select **Create Field**.

    The **New Field** dialog opens.

4.  In the **Name** field, enter the name of the new field.

    As you type, the name is mirrored in the **Variable Name** field in camel case with spaces and special characters removed. For example, entering `Customer Billing Address` produces the variable name **customerBillingAddress**. To enter a custom variable name, select the pencil icon to the right of the **Variable Name** field.

5.  In the **Level** field, select whether the field is a transaction-level \(header\) field or a transaction line-level field.

6.  Select the field type: **Text**, **Number**, **Boolean**, **Picklist**, or **Date/Time**.

7.  Select **Save**.

    The field editor opens. The available options depend on the field type selected. Continue with the section for your field type.

8.  Configure common options
9.  If the name requires updating, in the field editor, update the **Name**.

    The variable name shown in the field editor is locked and cannot be edited here. To change it, delete the field and re-add it.

10. In the **Description** field, enter a description of the field.

11. If the field must be completed on the layout before a quote can be submitted, enable the **Required** toggle.

12. In the **Default Access** field, set the field's access in the default view.

    |Option|Behavior|
    |------|--------|
    |**Editable**|The field is read and write accessible on the quote layout.|
    |**No Access**|The field is hidden from the quote layout and is not accessible through APIs.|
    |**Read Only**|The field is read only on the layout.|

13. Configure text field options
14. In the **Default Value** field, enter the text that the field displays by default when a quote is created.

15. In the **Minimum Field Length** field, enter the minimum number of characters that a user must enter in this field.

16. In the **Maximum Field Length** field, enter the maximum number of characters that a user can enter in this field.

17. Configure number field options
18. Select the form the number field takes.

    -   Select **Number** for a plain numeric value.
    -   Select **Currency** for a monetary value. The unit label defaults to the currency symbol configured for your ServiceNow CPQ site.
    -   Select **Percentage** for a percentage value. The unit label defaults to the percent symbol \(%\).
19. In the **Unit Label** field, enter a custom label to display alongside the number value.

    For Currency and Percentage forms, the unit label is set automatically. Override it here only if a custom label is needed.

20. In the **Minimum Value** field, enter the lowest value a user can enter for this field.

21. In the **Maximum Value** field, enter the highest value a user can enter for this field.

22. In the **Default Value** field, enter the number value that the field displays by default when a new quote is created.

23. Configure boolean field options
24. If the field should default to **True** when a quote is created, enable the **Default Checked** toggle.

    When the toggle is not enabled, the field defaults to **False**.

25. In the **True Label** field, enter the text to display when the field value is true.

    For example, entering `Yes` displays **Yes** on the quote layout when the Boolean value is true.

26. In the **False Label** field, enter the text to display when the field value is false.

27. Configure picklist field options
28. In the **Selection Type** field, select how users choose values from this picklist.

    -   Select **Single-select** so users can choose one option at a time.
    -   Select **Multi-select** so users can choose more than one option.
29. In the **Comparison Type** field, select how the selected option's value is treated when used in a rule condition.

    -   Select **Text** to treat the option value as a string in comparisons.
    -   Select **Number** to treat the option value as a numeric value in comparisons.
30. Select **+ Add Picklist Options** to add the first option to the picklist.

31. Configure the option properties using the following fields.

    |Property|Description|
    |--------|-----------|
    |**Order**|Controls the position of this option in the picklist. Lower numbers appear higher in the list. Use increments of 10 \(10, 20, 30\) rather than 1, 2, 3 to leave room for inserting options later.|
    |**Option Label**|The option name displayed to users on the quote layout.|
    |**Option Value**|The internal value that ServiceNow CPQ uses to identify this option in rules and integrations.|
    |**Selected**|When enabled, this option is the default selected value when a new quote is created.|
    |**Description**|An optional description of the option, visible in the administration interface.|
    |**Image URL**|The URL of a image to display in place of the option label text on the quote layout.|

32. Select **Save Option** to add the option to the picklist.

33. Select **+ Add Option** to add another option and repeat the previous two steps until all options are added.

34. Configure date/time field options
35. In the **Default Value** field, enter the default date and time for the field.

    The value is stored and displayed in UTC format: `YYYY-MM-DDTHH:MM:SSZ`. For more information about date and time field behavior, see [Date and time field fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-date-time-field-behavior.md).

36. In the **Not Before** field, enter the earliest date and time a user can select for this field.

37. In the **Not After** field, enter the latest date and time a user can select for this field.

38. Select **Save** to save the field configuration.

    The field is saved and associated with the blueprint. It appears in the Associated Fields list and is available to add to a quote layout.


## What to do next

Add the field to the quote layout to make it visible to users on the quote interface. For more information, see [Create a quote transaction layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-layout.md).

**Related topics**  


[Date and time field fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-date-time-field-behavior.md)

[Transaction-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-header-level-system-fields.md)

[Transaction line-level system fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-line-level-system-fields.md)

