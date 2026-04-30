---
title: Extract fields using the Document Intelligence workspace
description: Use the Document Intelligence workspace for field extraction, searching for recommendations, flagging fields, and identifying missing fields to complete document tasks.Extract text and number fields from your document in the document fields panel.Extract check box fields from your document in the document fields panel.Extract table fields from your document in the table panel.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Complete a document task, Using Document Intelligence, Document Intelligence, Enable AI experiences]
---

# Extract fields using the Document Intelligence workspace

Use the Document Intelligence workspace for field extraction, searching for recommendations, flagging fields, and identifying missing fields to complete document tasks.

## Overview of the Document Intelligence workspace

The Document Intelligence \(DocIntel\) workspace provides document management features that enable you to quickly review and process text extraction.

With the Document Intelligence workspace, you can:

-   Efficiently review the AI's recommendations, and confirm your document's extracted text.
-   Flag fields, identify missing fields, and review pending fields.

To get started with the Document Intelligence workspace:

-   [Create a document task](../task/upload-documents-for-extraction.md) for a document data extraction use case, upload a document, and process the task.
-   After DocIntel has processed the task, you can begin using the workspace. See [Complete a document task](../task/extract-data-from-documents.md).

## Layout of the Document Intelligence workspace

The following illustration shows the Document Intelligence workspace for a document task. The workspace includes the following areas:

-   1 - Thumbnail panel
-   2 - Document image panel
-   3 - Document controls
-   4 - Document fields panel
-   5 - Table panel

**Note:** In this view, the document fields panel is expanded so that the fields are visible.

![Areas of the Document Intelligence workspace for data extraction.](../image/docintel-workspace-overview2.png)

## Thumbnail panel

In the thumbnail panel of the workspace, you can select one page from a multiple-page document. The selected page is displayed in the document image panel. Selecting a page doesn’t affect what is displayed in the document fields panel.

The following image shows a document with two pages in the thumbnail panel.

![Document Intelligence workspace with multiple pages in the thumbnail panel.](../image/using-the-doc-intel-workspace1.png)

## Document image panel

The document image panel displays the page selected in the thumbnail panel.

As you move through the recommendations in the fields in the document fields panel, they’ll be highlighted in the document image panel to help you select the correct option.

![Document panel showing a highlighted recommendation.](../image/docintel-bounding-box.png)

You can also extract information directly from the document image using the draw tool. For more details, see [Extract fields using the draw tool](use-draw-mode-to-extract-fields.md#).

## Document controls

When you’re reviewing a document for extraction, you can use various controls to maximize the viewing area, zoom, or focus on the areas that you need. You can also extract information directly from the document image using the draw tool. For more details, see [Extract fields using the draw tool](use-draw-mode-to-extract-fields.md#).

The following illustration shows document controls. ![Controls in the Document Intelligence workspace.](../image/docintel-doc-image-controls.png)

## Document fields panel

The document fields panel enables you to open items for review, including viewing the AI's recommendations. You can also flag fields or mark fields as missing in the document.

**Note:** An asterisk indicates a required field.

The following illustration shows the different features of the document fields panel.

![Fields panel in Document Intelligence workspace.](../image/docintel-workspace-reviewitems.gif)

## Table panel

The table panel enables you to open table rows for review, including viewing the AI's recommendations. You can also flag fields or mark fields as missing in the document. Other table controls enable you to insert rows and resize columns as needed.

**Note:** An asteriskin the column heading indicates a required field.

The following illustration shows the different features of the table panel.

![Table panel in the Document Intelligence workspace.](../image/docintel-table-panel-image2.png)

## Extract single fields

Extract text and number fields from your document in the document fields panel.

### Before you begin

Role required: sn\_docintel.extraction\_agent

### About this task

Use the following steps to extract single fields from a document.

If the fields are already auto-filled with values, you can review them to ensure they are correct or adjust the fields as needed.

**Tip:** You can also use the draw tool to easily extract fields directly on the document image. For more information, see [Extract fields using the draw tool](use-draw-mode-to-extract-fields.md#).

### Procedure

1.  In the document fields panel, expand **Fields**.

2.  Select a field.

3.  Begin typing in the field and select a recommendation from the drop-down list.

    The recommendation with the highest [confidence score](docintel-confidence-scores.md) displays at the top of the list.

    **Tip:** As you move through the recommendations in the drop-down list, they’re highlighted in the document to help you select the correct option.

4.  If needed, filter or flag the recommendations

    -   To filter the list to show only a recommendation that matches exactly what you type, select the exact match mode icon \(![Exact match mode icon.](../image/icon-docintel-exact-match-mode.png)\) in the field.
    -   To flag the field for later attention, select **Flag for follow-up** in the field options menu \(![Field options menu icon](../image/icon-docintel-field-options-menu.png)\).
    -   If you can’t find an appropriate match in the document, select **Missing in the document** in the field options menu.To undo, select the **Edit** icon \(![Edit icon.](../image/icon-docintel-edit.png)\) in the field.
    The field will be marked as complete when you move to the next field.

5.  If needed, confirm or correct any field value conversions.

    Some field types convert the extracted value into a standard format. See [Data normalization](data-normalization.md).

    When the extracted value is ambiguous in a document, DocIntel interprets it as defined in the field configuration. A note prompts you to confirm or edit the converted value.

    ![Data extraction field and its converted value field](../image/docintel-normalization-example.png)

    -   Select **Confirm** in the converted value field to confirm that the converted value is accurate.
    -   Select **Edit**, enter the updated value, and select **Save** to correct the conversion.

## Extract check box fields

Extract check box fields from your document in the document fields panel.

### Before you begin

Role required: sn\_docintel.extraction\_agent

### About this task

Use the following steps to extract check box fields from a document.

If the check box fields are already auto-filled, you can review them to ensure they are correct or adjust the fields as needed.

### Procedure

1.  In the document fields panel, expand **Fields**.

2.  Select a field.

    A list of check boxes displays if the field is designated as a check box field type.

3.  Select the check boxes that apply to the field group.

    For each check box selected, DocIntel may provide one or more potential matches in the document.

    1.  Select a check box.

    2.  If there's more than one recommendation on the document image that matches the check box, select the one that applies.

        You can select or deselect a recommendation on the document at any time.

        **Tip:**

        -   Press **Tab** on the keyboard to move through the recommendations.
        -   Press **Enter** or **Return** to select one.
        -   To deselect a recommendation, select another one.
    3.  If there are no recommendations found, or if none of the recommendations are correct, select **Show all check box recommendations** in the check box options menu \(![Field options menu icon](../image/icon-docintel-field-options-menu.png)\) and choose from any other options in the document.

        **Tip:** Flag the check box for later attention by selecting **Flag for follow-up** in the check box option menu.

    4.  If you can’t find an appropriate match for the check box in the document, select **No match found** in the check box option menu.

    5.  Repeat these steps for each check box that applies to the field group.

4.  If you're in the Recommendation mode, ensure that all fields are marked complete.

    If you're in the Auto-fill mode, mark the fields as reviewed.


## Extract table fields

Extract table fields from your document in the table panel.

### Before you begin

Role required: sn\_docintel.extraction\_agent

### About this task

Use the following steps to extract table fields from a document.

If the fields are already auto-filled with values, you can review them to ensure they’re correct or adjust the fields as needed.

**Tip:** You can also use the draw tool to easily extract tables directly on the document image. For more information, see [Extract fields using the draw tool](use-draw-mode-to-extract-fields.md#).

### Procedure

1.  In the document fields panel, expand **Tables**.

    The Tables section only displays fields assigned to a table [field group](../task/manage-keys.md).

2.  Select a table.

    The table panel displays.

3.  Select the recommendation that applies to each table field.

    -   To select a recommendation, begin typing in the field and select a recommendation from the drop-down list.

        **Tip:** As you move through the recommendations in the drop-down list, they are highlighted in the document to help you select the correct option.

    -   To flag the field for later attention, select **Flag for follow-up** in the field options menu \( ![Field options menu icon.](../image/icon-docintel-field-options-menu.png)\).
    -   If you can’t find an appropriate match in the document, select **Missing in the document** in the field options menu.To undo, select the **Edit** icon \(![Edit icon.](../image/icon-docintel-edit.png)\) in the field.
4.  If needed, confirm or correct any field value conversions.

    Some field types convert the extracted value into a standard format. See [Data normalization](data-normalization.md).

    When the extracted value is ambiguous in a document, DocIntel interprets it as defined in the field configuration. A note prompts you to confirm or edit the converted value.

    ![Data extraction field and its converted value field](../image/docintel-normalization-example.png)

    -   Select **Confirm** in the converted value field to confirm that the converted value is accurate.
    -   Select **Edit**, enter the updated value, and select **Save** to correct the conversion.
5.  Adjust the table rows as needed.

    **Warning:** If you have a grid on the document image, changes made directly to the table rows can’t be synced to the grid\(s\). The grid\(s\) will be removed to avoid conflicting data.

    -   To add a row, select **New row**.
    -   To clear all field values in the row, select **Clear row values** in the row options menu \(![Row options menu icon.](../image/icon-docintel-field-options-menu.png)\).
    -   To insert a row, select **Insert row above** or **Insert row below** in the row options menu.
    -   To delete a row, select **Delete row** in the row options menu.
    -   To mark a row as reviewed, select **Mark row as reviewed** in the row options menu.
    -   To make changes to multiple rows, select the check box in the first column of each row and select an action from the **Action on selected rows** list.
6.  Review and complete the rows.

    -   If you filled in the fields, ensure that all rows are marked as complete.
    -   If the fields are auto-filled with values, then all rows are marked as reviewed.

