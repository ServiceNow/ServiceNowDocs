---
title: Create a dynamic attribute
description: Define one or more dynamic attributes that describe a record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Dynamic Schema, Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a dynamic attribute

Define one or more dynamic attributes that describe a record.

## Before you begin

You can define each of the dynamic attributes that describe your records in a dynamic namespace that's associated with a dynamic attribute store field. You can create a dynamic namespace the following ways:

-   Create a dynamic attribute store field. When you create a dynamic attribute store field, a dynamic namespace is automatically created and associated with the store field. See [Create a dynamic attribute store field](create-dynamic-attribute-store-field.md).
-   Create a dynamic namespace manually. See [Create a dynamic namespace](create-dynamic-namespace.md).

Role required: dynamic\_schema\_writer

## Procedure

1.  Navigate to **All** &gt; **Dynamic Schema** &gt; **Dynamic Namespaces**.

2.  Select the dynamic namespace that you want to update.

3.  In the Dynamic Attributes related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_szt_vrp_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Namespace

</td><td>

Dynamic namespace that contains this attribute.

</td></tr><tr><td>

Label

</td><td>

Label used for displaying the dynamic attribute.

</td></tr><tr><td>

Name

</td><td>

Internal name for the dynamic attribute.

</td></tr><tr><td>

Type

</td><td>

Data type of the attribute.-   To define the attribute using a choice set, select String.
-   To define the attribute as a reference to a record in another table, select Reference.

Defining the attribute as a reference maintains accuracy by automatically reflecting changes from the linked record. This simplifies maintenance when related information changes. For example, a Covered Vehicle attribute in a policy record can reference a vehicle in the Vehicle table so updates to vehicle details appear in the policy without manual edits.

</td></tr><tr><td>

Choice Set

</td><td>

Fixed set of values defined in a choice set. For example, if you created a choice set for Colors with choices for red, green, and blue, you can select the Colors choice set to limit the attribute's values to the color choices defined in the choice set. See [Create a dynamic choice set](create-choice-set.md).

 This option only appears when you select String in the **Type** field.

</td></tr><tr><td>

Description

</td><td>

A brief summary of what the attribute stores.

</td></tr><tr><td>

Active

</td><td>

Option to activate the dynamic attribute.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Add a dynamic attribute for screen resolution

![Add a dynamic attribute that captures the screen resolution of products in the Departments namespace.](../image/dynamic-attribute-example.png)

## What to do next

Add more dynamic attributes to the dynamic namespace as needed. For example, when defining metadata for products in the Electronics category, you might add dynamic attributes that describe screen size, screen type, and watts.

