---
title: Screen fields
description: Screen fields improve the usability of your form screens. With screen fields, your users can view and edit attachments, view and complete checklist items, or display a field without a label.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure a details screen for a record screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Screen fields

Screen fields improve the usability of your form screens. With screen fields, your users can view and edit attachments, view and complete checklist items, or display a field without a label.

When configuring a details screen, you select fields to display on your form. When you save the details screen, the instance creates a Screen Field \[sys\_sg\_screen\_field\] each selected field. You can modify these records to change the screen field type. Change the screen field type to change how your information is presented, and improve the appearance and usability of the screen for your users.

## Screen field types

<table id="table_sqv_52l_vhb"><tbody><tr><td>

**Text** Use a text screen field to display text on your form. This text can come from any field on the current record. The text field type has a **Value only** option, which displays the field without a label. In this example, the **Description** field is shown without a label.

</td><td>

![Text screen field with value only option selected.](../image/screen-field-value-only.png)

</td></tr><tr><td>

**Percentage** Use a percentage screen field to display a percentage value on your form. This value comes from a field on the current record. Percentages are determined by using a decimal value. For example, a value of `0.35` displays in a percentage field as 35%. This field type has a **Value only** option, which displays the field without a label.

</td><td>

![Percentage screen field.](../image/screen-field-percent.png)

</td></tr><tr><td>

**Image** Use an image screen field to display an image on your form. The value for this field comes from an image field or field that contains the sys\_ID of an image in the Attachment \[sys\_attachment\] table. Users can tap an image to open a preview screen to display the full image.

</td><td>

![Screen field on form and image preview screen.](../image/screen-field-image.png)

</td></tr><tr><td>

**Attachment** Use an attachment screen field to display all the attachments of a record. Buttons to rename or delete attachments display automatically for your users. Users can tap a button to modify attachments.

</td><td>

![Attachment screen field on the incident table.](../image/screen-enhance-attachment.png)

</td></tr><tr><td>

**Video** Use a video screen field so that your users can watch a video in your form. The video screen field gets its value from a field on your current record and contains a link to a video. The video must be externally hosted. Users can see the video in a new window when they tap **Play Video**.

</td><td>

![Video screen field.](../image/screen-field-video.png)

</td></tr><tr><td>

**File** Use a file screen field to display a PDF file within your form. The PDF displays as a preview on your form. Users can tap the preview \(![PDF preview icon](../image/pdf-preview-icon.png)\) icon to open it in a preview screen where they can scroll and zoom on the PDF document. The file screen field gets its value from a field on the current record. The value must be the sys\_ID of an attachment \[sys\_attachment\] record on your instance that contains a PDF file.

</td><td>

![File screen field.](../image/screen-field-file.png)

</td></tr><tr><td>

**HTML** Use an HTML screen field to display HTML content within your form. The HTML screen field can get its value from an HTML field in your current record or a string field that contains an HTML code.

</td><td>

![HTML screen field.](../image/field-screen-html.png)

</td></tr><tr><td>

**Checklist** Use checklist screen fields to display all the checklist items that are associated with a record. Users can tap individual checklist items to mark them as complete or incomplete.

</td><td>

![Checklist screen field.](../image/screen-enhance-checklist.png)

</td></tr><tr><td>

**Date** Use a date screen field to display a date value on your form. This value comes from a date or date/time field on the current record. Dates are displayed in the format that are defined by your instance. This field type has a**Value only** option, which displays the value of the field without the field label. If the field is configured with an action function, users can change the values of these fields. For more information, see [Configure an action function](../task/sg-studio-config-action-function.md).

</td><td>

![Date screen field.](../image/screen-field-date.png)

</td></tr><tr><td>

**Stage** Use stage fields to display a read-only approval or completion status of requested items and services. Stage fields are displayed under the following conditions:

-   A stage field is added on a form for Requested items \[sc\_req\_item\] records.
-   A stage field is added on a form for Catalog item \[sc\_cat\_item\] records, as long the stage names and statuses are configured using one of the following flow types:
    -   Workflow Studio
    -   Workflow \[wf\_workflow\]
    -   Execution Plan \[sc\_cat\_item\_delivery\_plan\]
-   A stage field is added on a form for any other tables if the stage names and statuses are configured using Workflow \[wf\_workflow\].

</td><td>

![Mobile stage field.](../image/mobile-stage-field.png)

</td></tr></tbody>
</table>-   **[Add screen fields to a record screen](../task/sg-mobile-add-screen-field.md)**  
Add screen fields to improve the usability of your record screens. Screen fields enable you to change how information is shown in your form or you can provide access to additional elements, such as attachments, videos, or links.
-   **[Add a video screen field to a record screen](../task/sg-mobile-add-video-field.md)**  
Learn how to use a video screen field to view embedded videos in your mobile screens.

