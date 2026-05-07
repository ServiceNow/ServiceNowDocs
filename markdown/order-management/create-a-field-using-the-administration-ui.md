---
title: Create a field using the Administration UI
description: Learn how to create a field in the CPQ UI for use in Blueprint.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure fields, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a field using the Administration UI

Learn how to create a field in the CPQ UI for use in Blueprint.

## Before you begin

Role required: Admin

## Procedure

1.  In the CPQ navigation pane, click **Fields**.

    ![Menu](../images/cpq-fields-menu-item.png)

    The Fields administration page opens, listing the fields in the current environment.

    ![Admin fields](../images/cpq-fields-list.png)

    To edit a field, click its name \(a\). To create a new field, click **+ New** \(b\).

2.  Click **+ New**.

3.  In the New Field window, name the field and select a field type.

    ![New field](../images/cpq-fields-new-field-dialog.png)

    -   \(A\) Valid field names can be composed of up to 255 characters, including letters, numbers, spaces, and the following special characters: `{}[]()|\~`_^@?<=>;:/.-,+*ʼ&%$#”!`
    -   \(B\) The variable name is automatically populated. To set a different variable name, click the pencil icon. \(You cannot edit the variable name later.\) Valid field variable names consist of letters, numbers, and underscores. The first and last character must be a letter or number.
    -   \(C\) Fill in the type-specific details, as necessary.
    -   \(D\) The New Field window shows the Component Display Types available for the field type.
4.  Click **Save**.

    If you need to create a large number of fields or field options, use the Matrix Loader.

    When you create a field, it becomes available to any layout or rule in the environment. However, you must associate a field with a blueprint so that the field can be used in a configuration experience.


## What to do next

[Associate a field with a blueprint](cpq-associate-field-with-a-blueprint.md)

**Related topics**  


[Configure the Matrix Loader](cpq-using-the-matrix-loader.md)

