---
title: Create a dynamic choice set
description: Define a fixed set of values for an attribute.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with Dynamic Schema, Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Create a dynamic choice set

Define a fixed set of values for an attribute.

## Before you begin

Role required: dynamic\_schema\_writer

## About this task

For some dynamic attributes, you might want to limit the possible values that are accepted. You can define a choice set that holds a fixed set of choices, and then create a dynamic attribute whose values are limited to the choices defined in the choice set.

Dynamic choice sets aren't associated with a specific namespace. After you define a dynamic choice set, you can use it in any dynamic namespace.

For example, you can define a choice set for colors, with red, blue, and green as the choices. You can select this choice set in the bike\_color dynamic attribute in one namespace and use it again in the paint\_color dynamic attribute in a different namespace.

## Procedure

1.  Navigate to **All** &gt; **Dynamic Schema** &gt; **Dynamic Choice Sets**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Label used for displaying the dynamic choice set.|
    |Name|Internal name for the dynamic choice set.|
    |Description|A brief summary of what the choice set stores.|
    |Active|Option to activate the dynamic choice set.|

4.  Select **Submit**.


## Add choice set for screen types

![Add a choice set for type of screens.](../image/dynamic-choice-set-example.png)

## What to do next

[Add choices to a dynamic choice set](add-choices-choice-set.md)

