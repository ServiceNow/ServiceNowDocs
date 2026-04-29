---
title: Enable a field type for normalization or transformation
description: Create or modify a normalization field type record to enable a specific field data type for use with normalization or transformation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable a field type for normalization or transformation

Create or modify a normalization field type record to enable a specific field data type for use with normalization or transformation.

## About this task

To normalize or transform a value in a reference field, apply the processing to the field in the target table.

## Procedure

1.  Navigate to **All** &gt; **Field Normalization** &gt; **Administration** &gt; **Normalization Field Types**.

2.  Click **New** in the record list.

3.  Enter a **Name** for the field type that clearly describes the type in the dictionary.

    This value is for reference only and is not used in any processing. For example, you might enter **IP Address** for the field type of `ip_address`.

4.  Enter the **Type** from the dictionary.

5.  Select the appropriate check box to use this field type to normalize or transform fields.

    In the base system, only the **String** field type is used for normalization.

6.  Right-click in the header bar and select **Save** from the choice list.

    The **Transform Categories** Related List appears.

7.  If this field type is being used for transforms, click **Edit** to associate an existing Transform Category with this field type.

    **Note:** If you create a custom field type that is used for normalizations only, a link to a transform category is not necessary.

    The relationship of a field type to a category, and the category to a list of transformation definitions, is completely configurable.

    The String field type is associated with the Text Transform Category, which contains these transform definitions. Any of these associations are configurable.

    ![Normalization Field Type](../image/NormalizationFieldType.png)


