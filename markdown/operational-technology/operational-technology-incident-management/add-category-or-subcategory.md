---
title: Create a category or subcategory
description: Create an Operational Technology incident category or subcategory that you want to use to classify incidents.
locale: en-US
release: yokohama
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2025-08-06"
reading_time_minutes: 1
breadcrumb: [Incident categories and subcategories, Configure, Operational Technology Incident Management, Operational Technology]
---

# Create a category or subcategory

Create an Operational Technology incident category or subcategory that you want to use to classify incidents.

## Before you begin

-   Set the application scope to **Operational Technology Incident Management**.
-   Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Choice Lists**.

2.  To create a category, do these actions:

    1.  Select **New**.
    2.  In the **Element** field, enter the word `category`.
    3.  In the **Label** field, enter the category name.
    4.  In the **Value** field, enter the category value.
    5.  In the **Sequence** field, enter the sequence number.
    6.  Select **Submit**.
3.  To add a new subcategory, do these actions:

    1.  Select **New**.
    2.  In the **Element** field, enter the word `subcategory`.
    3.  In the **Label** field, enter the subcategory name.
    4.  In the **Value** field, enter the subcategory value.
    5.  In the **Sequence** field, enter the sequence number.
    6.  If the subcategory belongs to an existing category, add the category value to the **Dependent value** field.
    7.  Select **Submit**.

## Result

The new category or subcategory is available to select on an Operational Technology incident record.

**Parent Topic:**[Incident categories and subcategories](../reference/ot-incident-categories-subcategories.md)

