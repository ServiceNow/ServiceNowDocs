---
title: Image field type
description: Image fields enable you to add images to forms.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Image field type

Image fields enable you to add images to forms.

## Before you begin

Role required: personalize\_form

## About this task

For example, you can add portraits to the user records in your system. The image type must be `.gif`, `.jpg`/`.jpeg`, or `.png`.

Image resizing is defined by the CSS. Larger images are resized to 250 pixels. For most browsers, the larger of the height and width measurements is reduced to 250 pixels and the proportion of the image is maintained. For example, an image with a size of 1508 x 663 pixels is resized to 250 x 110 pixels. Some browsers resize both the height and width measurements to 250 pixels, resulting in a square image.

You can add a new image field.

## Procedure

1.  Open the desired form.

2.  Create a new field with the **Type** set to **Image**.

    For instructions, see [Add and customize a field in a table](t_CreatingNewFields.md).

3.  Add the new field to the form and save your customization.

    The form displays the new blank image field.

4.  Click **Click to add** in the image field, select an image to upload, and click **OK**.

    The selected image is attached to the form and displayed in the image field.


## Result

![Picture displayed in image field](../image/PhotoField.png)

**Parent Topic:**[Field types](../../reference-pages/reference/r_FieldTypes.md)

**Related topics**  


[Configuring the form layout](../../form-administration/concept/configure-form-layout.md#)

