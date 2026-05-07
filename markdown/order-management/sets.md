---
title: Configure sets
description: Sets group related fields into repeatable collections, allowing administrators to streamline configurations and reduce redundancy. They enable dynamic, table-like data entry, support aggregates, and simplify managing repeated questionnaires or configurable options in CPQ.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure sets

Sets group related fields into repeatable collections, allowing administrators to streamline configurations and reduce redundancy. They enable dynamic, table-like data entry, support aggregates, and simplify managing repeated questionnaires or configurable options in CPQ.

[Sets introduction](https://www.youtube.com/watch?v=1Wt_GYaSr7Y&t=2s)

Sets allow the administrator to identify a number of fields in a group. Once associated with a set, the fields may then be replicated an indefinite number of times on the end-user UI in a matrix format. Sets reduce the number of fields and rules that must be defined for use cases that repeat fields and rules. The maximum number of set records \(the number of times a group of fields can be repeated\) is 2000.

In this set, three fields \(Sandwich Choice, Side Choice, and Drink Choice\) are defined in a set; the set is repeated three times:

![Configure sets](../images/cpq-sets-example-set.png)

## Display types

Sets can be displayed in several ways.

-   As table rows:

    ![Display types](../images/cpq-sets-display-type-table-rows.png)

-   As table columns:

    ![Display types](../images/cpq-sets-display-type-table-columns.png)

-   As list rows:

    ![Display types](../images/cpq-sets-display-type-list-rows.png)

-   As a set repeater:

    ![Display types](../images/cpq-sets-display-type-set-repeater.png)


You can manage sets by using the Layout Wizard. For more information about sets and layouts, see [Using sets in layouts](layouts-sets.md).

## Adding and removing set rows

In the end-user UI, the user has four ways to increment or decrement set records:

-   To add a record to the bottom of the set, click the green plus in the upper right corner.

    ![Adding and removing set rows](../images/cpq-sets-add-set.png)

-   To add or remove records from the bottom of the set, edit the Size field and click **Change Size**.

    ![Adding and removing set rows](../images/cpq-sets-change-size.png)

-   To insert a record between two existing records, hold the cursor between them in the Index column.

    ![Adding and removing set rows](../images/cpq-sets-insert-record.png)

-   To add records relative to the current record or to delete a record, use the menu in the Index column.

    ![Adding and removing set rows](../images/cpq-sets-add-or-delete-set.png)

    For more information about managing sets, see [Using sets in layouts](layouts-sets.md) and [How sets interact with the rest of a blueprint](how_sets_interact_with_the_rest_of_the_blueprint.md).


## Creating a set

Sets can be added in the same two areas you would create fields: the blueprint to which to add the set, and the fields administration tab.

![Creating a set](../images/cpq-sets-blueprint.png)

![Creating a set](../images/cpq-sets-field-admin-tab.png)

Select the set field type from among the list of options:

![Creating a set](../images/cpq-sets-new-field.png)

Give your new set a name and choose from the size types.

![New field](../images/cpq-sets-new-field-size-type.png)

The size type cannot be changed after the set is saved. Therefore, keep the following in mind:

-   The set field determines the number of records that will be displayed in the set. This numeric field can be visible and edited by a user or set by determination action, as the case requires.
-   The associated picklist leverages a picklist field to determine how many records to show in the set. When this option is selected, the admin must identify the field that will drive the set size. When the set type is Associated Picklist, CPQ creates two additional fields in the set:

    -   Option Value: The value of each option in the set, represented as a read-only text field.
    -   Select Option: Tracks whether each option of the picklist is selected.
    -       For more information, see [Creating an associated picklist set](creating_an_associated_picklist_set.md).


The next screen is the set screen, where the admin can add fields to the set, enforce distinct values, and create aggregates.

To add a field to the set, search for the name of the field to be added to the set, and then click **+**.

Any field in the set can have the “Distinct Values” option enabled. When this is true, each index of the set must have a unique value for the field. This setting only applies to non-empty fields.

When you create an aggregate for a field in the set, options include Average, Count, Maximum, Minimum, and Sum. For example, a sum aggregate on a number field called Quantity might store the sum of all Quantity field values in the set. Aggregates function as a field external to the set and can be used in global rules.

For more information on set aggregates, see [Creating set aggregates](creating_set_aggregates.md).

When using sets in a configuration, it’s important to understand the scope of fields in the set and what can and cannot be accomplished when creating rules. See [How sets interact with the rest of a blueprint](how_sets_interact_with_the_rest_of_the_blueprint.md).

**Related topics**  


[Using sets in layouts](layouts-sets.md)

