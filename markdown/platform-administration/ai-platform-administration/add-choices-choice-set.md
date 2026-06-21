---
title: Add choices to a dynamic choice set
description: Build out a dynamic choice set by defining the choices that belong to it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/ai-platform-administration/add-choices-choice-set.html
release: yokohama
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Dynamic Schema, Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add choices to a dynamic choice set

Build out a dynamic choice set by defining the choices that belong to it.

## Before you begin

Role required: admin

## About this task

After you create a dynamic choice set, define each of the choices that comprise the dynamic choice set.

## Procedure

1.  Navigate to **All** &gt; **Dynamic Schema** &gt; **Dynamic Choice Sets**.

2.  Select the dynamic choice set that you want to update.

3.  In the Dynamic Choices related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Choice Set|The dynamic choice set that contains this choice.|
    |Label|Label used for displaying the dynamic choice.|
    |Name|Internal name for the dynamic choice.|
    |Order|Value that determines the choice's order in a list.|
    |Active|Option to activate the choice in the dynamic choice set.|

5.  Select **Submit**.


## Add a dynamic choice to a dynamic choice set

\[Omitted image "dynamic-choice-example.png"\] Alt text: Add a choice to the screen type choice set.

## Choices defined in choice set

\[Omitted image "dynamic-choice-set-choices-example.png"\] Alt text: Choices in a choice set.

## What to do next

Add more choices as needed. Create a dynamic attribute whose values are derived from the dynamic choice set.

