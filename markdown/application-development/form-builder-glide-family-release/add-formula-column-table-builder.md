---
title: Add a formula to a column in Table Builder
description: Use a predefined function or create a formula to calculate a value for a column without writing a script in Table Builder. You can use two or more functions to create a formula according to your requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/form-builder-glide-family-release/add-formula-column-table-builder.html
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [Field configuration, Reference, Table Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Add a formula to a column in Table Builder

Use a predefined function or create a formula to calculate a value for a column without writing a script in Table Builder. You can use two or more functions to create a formula according to your requirements.

## About this task

The following limitations apply when adding formulas to columns:

-   You can add a formula to a column only if the table is in the same scope as the application.
-   You can't add a formula to unsupported columns, function field columns, or columns that already use a script as the calculated value.

## Before you begin

Role required: formula\_read and either personalize\_dictionary or AES user role and delegated developer permissions. For more information, see the following resources:

-   [Delegate developers using AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/app-engine-studio/aes-app-dev-workflow.md)
-   [Accessing Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/form-builder-glide-family-release/accessing-form-builder.md)

## Procedure

1.  From the **Data** or **Forms** tab, select the Open side panel icon \(\[Omitted image "side-panel-icon.png"\] Alt text: Open side panel icon\) for a column.

2.  In the **Config** tab of the **Formula** section, select **+ Add**.

3.  Enter a predefined function or a formula in the Formula editor modal.

    For example, to combine the First name and Last name column values into a Full name column, enter `CONCATENATE(first_name,last_name)`. For syntax guidance and examples, select a function in the auto-suggestion list as you type. For all available functions, see [Formulas for column values in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/form-builder-glide-family-release/formulas-columns-table-builder.md).

    **Note:** A formula can use only fields that you have read access to, including fields reached by dot-walking.

    \[Omitted image "formula-builder-table-builder.gif"\] Alt text: Formula editor modal in Table Builder

4.  Select **Submit**.


## Result

The formula is validated and added to the column if it doesn't have any errors.

**Parent Topic:**[Field configuration in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/form-builder-glide-family-release/field-parameters.md)

