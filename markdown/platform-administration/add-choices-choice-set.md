---
title: Add choices to a dynamic choice set
description: Build out a dynamic choice set by defining the choices that belong to it.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a dynamic choice set, Working with Dynamic Schema, Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Add choices to a dynamic choice set

Build out a dynamic choice set by defining the choices that belong to it.

## Before you begin

Role required: dynamic\_schema\_writer

## Procedure

1.  Navigate to **All** &gt; **Dynamic Schema** &gt; **Dynamic Choice Sets**.

2.  Select the dynamic choice set that you want to update.

3.  In the Dynamic Choices related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Choice Set|The dynamic choice set that contains this choice.|
    |Label|Label used for displaying the dynamic choice.|
    |Value|Internal name for the dynamic choice.|
    |Order|Value that determines the choice's order in a list.|
    |Active|Option to activate the choice in the dynamic choice set.|

5.  Limit the availability of the choice that you want to add.

    -   Restrict the choice to a specific namespace by selecting that namespace in **Within Namespace**.
    -   Restrict the choice to attributes in a specific category by selecting a namespace in **Within Namespace** and the category in **Within Category**.
    -   Restrict the choice to one attribute in a namespace by selecting the namespace in **Within Namespace** and selecting the attribute in **For attribute**.
    The choice is only available in the dynamic attribute store field that belongs to the namespace you selected in **Within Namespace**. Further restrictions might apply if you selected a category or a specific attribute.

6.  Select **Submit**.


## Result

A dynamic choice is added to the dynamic choice set.

## Add a dynamic choice to a dynamic choice set

![Add a choice to the screen type choice set.](../image/dynamic-choice-example.png)

## Define a specific choice in the Televisions category

![Add a choice that's limited to a specific attribute in a specific category.](../image/dynamic-choice-limited-example.png)

## Choices defined in choice set

![Choices in a choice set.](../image/dynamic-choice-set-choices-example.png)

## What to do next

Add more choices as needed. Create a dynamic attribute whose values are derived from the dynamic choice set.

