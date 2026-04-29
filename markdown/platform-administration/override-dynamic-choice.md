---
title: Override a dynamic choice
description: Make a choice appear differently in a specific dynamic namespace by creating a dynamic choice override.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a dynamic choice set, Working with Dynamic Schema, Dynamic Schema, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Override a dynamic choice

Make a choice appear differently in a specific dynamic namespace by creating a dynamic choice override.

## Before you begin

Role required: dynamic\_schema\_writer

## Procedure

1.  Navigate to **All** &gt; **Dynamic Schema** &gt; **Dynamic Namespaces**.

2.  Select the dynamic namespace that you want to update.

3.  In the Dynamic Choice Overrides related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Choice|The choice that you want to override.|
    |Override Label|Optional label to use instead of the original choice label.|
    |Hidden|Option to hide the choice.|

5.  Define where the choice override applies in your dynamic schema.

    -   Restrict the override to a specific namespace by selecting that namespace in **Within Namespace**.
    -   Restrict the override to attributes in a specific category by selecting a namespace in **Within Namespace** and the category in **Within Category**.
    -   Restrict the override to one attribute in a namespace by selecting the namespace in **Within Namespace** and selecting the attribute in **For attribute**.
6.  Select **Submit**.


## Result

The choice is overridden in the dynamic namespace that you selected in **Within Namespace**. Further restrictions might apply if you selected a category or a specific attribute.

## An override is defined for the LED choice. In the Smartphones category, the choice appears as microLED

![A dynamic choice override is defined on the LED choice. When LED is used in the Smartphones dynamic category, it appears as microLED.](../image/dynamic-choice-override-example.png)

