---
title: Add a formula to a column in Table Builder
description: Use a predefined function or create a formula to calculate a value for a column without writing a script in Table Builder. You can use two or more functions to create a formula according to your requirements.
locale: en-US
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Field configuration in Table Builder, Table Builder reference, Table Builder, Builder library, Developing your application, Building applications]
---

# Add a formula to a column in Table Builder

Use a predefined function or create a formula to calculate a value for a column without writing a script in Table Builder. You can use two or more functions to create a formula according to your requirements.

## Before you begin

-   The scope of the table should be within the scope of the application. Otherwise, you cannot add a formula to a column in the table that is outside the scope of the app.
-   Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

## Procedure

1.  From the **Data** or **Forms** tabs, click the Open side panel icon \(![Open side panel icon](../image/side-panel-icon.png)\) for a column.

2.  In the **Config** tab of **Formula** section, click **+ Add**.

3.  Enter a predefined function or a formula in the **Formula editor** modal.![Formula editor modal in Table Builder](../image/formula-builder-table-builder.gif)

    For example, to concatenate the First name column value with the Last name column value and populate the Full name column value, enter `CONCATENATE(first_name,last_name)`. For more information about available predefined functions and example formulas, see [Formulas for column values in Table Builder](../reference/formulas-columns-table-builder.md#)

    For syntax guidance and examples, click the function in the auto-suggestion that appears as you begin typing.

    **Note:** You cannot add a formula for unsupported columns, columns that are function fields, and the columns that already have script as the calculated value type.

4.  Click **Submit**.


## Result

The formula is validated and added to the column if it doesn't have any errors.

**Parent Topic:**[Field configuration in Table Builder](../reference/field-parameters.md)

