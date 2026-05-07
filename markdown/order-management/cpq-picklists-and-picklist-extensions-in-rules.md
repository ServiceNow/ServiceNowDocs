---
title: Picklists and picklist extensions in rules
description: Learn how to use picklist extensions \(PLEs\) effectively in rules. Understand how filtering, inclusion, and exclusion interact, and apply correct operators like equals and contains for single- and multi-select picklists to ensure accurate rule behavior in advanced configurations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure picklist extensions, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Picklists and picklist extensions in rules

Learn how to use picklist extensions \(PLEs\) effectively in rules. Understand how filtering, inclusion, and exclusion interact, and apply correct operators like equals and contains for single- and multi-select picklists to ensure accurate rule behavior in advanced configurations.

Picklist extensions \(PLEs\) are a powerful way for administrators to display as much information as possible about a product while making it easy for end users to select exactly what they want. However, simplicity at the front end can mask complexity at the back end. This article shows administrators how to correctly use PLEs in rules and advanced functions and explains some important caveats.

**Note:**

-   Try using Filter Options &amp; Product Info first.
-   Do not use inclusion rules for PLEs. PLE filtering works like inclusion rules, so in order to remove further options, the user should use exclusion rules.
-   **Contains** and **Equals** act differently on multi-select picklists. `Array.includes()` and `==` also act differently.

## Simple rules

It's best not to use rules with picklist extensions. PLEs are designed so that you can filter options and send data to the bill of materials without writing rules. Therefore, most reasons to use inclusion, exclusion, and product rules are not present in PLEs. Make sure your use case can’t be completed with typical PLE features before you continue to build your rules.

If you are using selections in a PLE to drive actions, make sure to note the difference between the Equals and Contains operators.

-   Equals checks whether the selection in the PLE exactly matches the condition’s value.
    -   It can be used with both single-select and multi-select picklists, but it is recommended to be used with single-select PLEs since it is the closest to what users usually imagine the functionality would be.
    -   If you are using a multi-select in the condition, if the user makes multiple selections, the condition will not be met if using equals.
-   Contains checks whether the selection in the PLE includes the value described. This is the recommended operator for multi-select PLE fields.

For example: A user creates a multi-select picklist field with four options.

![Picklists and picklist extensions in rules](../images/cpq-picklist-field-four-options.png)

Suppose the condition of a rule \(in this case, a determination action\) is set to fire if the multi-select field equals multi option 4.

![Picklists and picklist extensions in rules](../images/cpq-picklist-field-equals.png)

If the end user selects only multi option 4, the rule fires:

![Picklists and picklist extensions in rules](../images/cpq-picklist-field-fires.png)

If the end user selects multi option 3 and multi option 4, the rule does not fire:

![Picklists and picklist extensions in rules](../images/cpq-picklist-field-does-not-fire.png)

On the other hand, if the condition is set to fire if the multi-select field contains option 4, it fires in both instances.

![Picklists and picklist extensions in rules](../images/cpq-picklist-field-contains-option-4.png)

![Picklists and picklist extensions in rules](../images/cpq-picklist-field-fires-both-instances-1.png)

![Picklists and picklist extensions in rules](../images/cpq-picklist-field-fires-both-instances-2.png)

## How PLE filters interact with exclusion rules

Picklist extension filters act in the same way that simple inclusion rules work, except that when the defined filter fields are empty, no options are included instead of all options when a simple inclusion rule is not firing.

If you want to have a field that is not defined as a filter in the PLE and that limits options in your PLE field, you need to use a simple exclusion rule in order to further limit those field options, since using an inclusion rule would combine with the inherent inclusion contained in the PLE filter and leave all field options available.

**Note:** Due to the nature of mapping the extended information via filter fields, using an inclusion rule to show more options for a PLE will show only the option value and no further data. Do not use inclusion rules that act on the options of a PLE.

## Advanced rules

When using picklists in advanced rules, it’s important to know how these fields appear when referenced using the `cfg` object. For single-select picklists, the field has the text of the option, but for multi-select picklists, they will be in an array. This difference can often lead to discrepancies when building advanced functions.

Similar to the differences in simple conditions between Equals and Contains, while single-select picklists can be referenced in an “if” statement as:

```
1 if (cfg.field == "option") {
2 //code
3 }
```

Multi-select picklists should use the function “Array.includes\(\)” to see if one of the options has been selected:

```
1 if (cfg.field.includes("option")) {
2 //code
3 }
```

This function acts on an array and will return true or false depending on whether the array includes the inputted value.

To determine the selections of a multi-select picklist in an advanced function, use the `.push()` function to add the option. Adding an option that is not defined in the picklist’s fields results in an error.

For other manipulations with the multi-select picklist array in advanced functions, refer to the Help menu’s Array functions. If there are conflicting inclusion and exclusion actions, exclusion actions have precedence.

## Additional reading

For an overview of the picklist extension feature, see [Picklist extensions](cpq-picklist-extensions-ples.md).

For a deeper understanding of the back end and how to display PLEs, see [Displaying a picklist extension on a layout](csv_layouts_how_do_i_display_a_picklist_extension.md).

For an overview of the Picklist Extension Pricing enrichment feature, see [The Picklist Extension Pricing enrichment](picklist-extension-pricing-scripts.md).

