---
title: Create a raw field
description: A raw field is a custom field created by an administrator to show the original \(raw\) input in a field on a form after it has been normalized or transformed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a raw field

A raw field is a custom field created by an administrator to show the original \(raw\) input in a field on a form after it has been normalized or transformed.

## About this task

An administrator might add a custom field to a form to show the original, or raw, value of a normalized field.

This is a read-only field that might be called something like **Raw CPU type** or **Original Name**. In the following example, the **CPU type** field was normalized to **Xeon** from an original, raw value of **Xeon L3350**.

![Normalized and raw fields](../image/NormalizedAndRawFields.png)

## Procedure

1.  In the form containing the field that is being normalized or transformed, right-click in the header bar.

2.  Select **Personalize** &gt; **Form Layout**.

3.  Complete the Create new field form at the bottom of the page, and then click **Add**.

    -   **Name**: Type the field label. In this case, use Raw + &lt;field label&gt;.
    -   **Type**: Select a data type from the list for this field.
    -   **Field length**: Select the character limit for this field. The default is 40.
4.  Move the new field adjacent to the normalized field using the direction arrows in the slushbucket.

5.  Click **Save**.

    ![Normalize raw field](../image/NormalizeRawField1.png)


