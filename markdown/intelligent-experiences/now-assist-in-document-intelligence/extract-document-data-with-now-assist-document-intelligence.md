---
title: Extract document data with Now Assist in Document Intelligence
description: Use the Document Intelligence workspace to review the information that was extracted from a document by Now Assist in Document Intelligence. You can also flag fields for follow-up and identify missing information in the document.
locale: en-US
release: yokohama
product: Now Assist in Document Intelligence
classification: now-assist-in-document-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Using Now Assist in Document Intelligence, Now Assist in Document Intelligence, Enable AI experiences]
---

# Extract document data with Now Assist in Document Intelligence

Use the Document Intelligence workspace to review the information that was extracted from a document by Now Assist in Document Intelligence. You can also flag fields for follow-up and identify missing information in the document.

## Before you begin

Role required: sn\_docintel.admin, sn\_docintel.creation\_agent, or sn\_docintel.extraction\_agent

## About this task

Now Assist uses generative AI capabilities to provide recommendations for the field values that were extracted from the document. The Document Intelligence workspace provides document management features that enable you to quickly review and process text extraction.

With the Document Intelligence workspace, you can:

-   Efficiently review the Now Assist recommendations, and confirm your document's extracted text.
-   Flag fields, identify missing fields, and review pending fields.

For more information, see [Document Intelligence workspace with Now Assist](../concept/document-intelligence-workspace-with-now-assist.md).

## Procedure

1.  Open the Document Intelligence workspace to view the document and the extracted values.

2.  In the document fields panel, select a field.

    The field’s review status is set to In progress.

    If Now Assist can detect the source of its prediction in the document, it will highlight it in the document image panel.

    Collapse a side panel using the Collapse icon \(![Collapse icon.](../image/icon-docintel-na-collapse-panel.png)\), if needed.

3.  Review the field for accuracy.

    **Note:** The field value is a generative AI prediction based on the document text. Review the field carefully to ensure it is accurate.

4.  Take the appropriate action on the field.

    For more information on extracting fields, see [Extract fields using the Document Intelligence workspace](../concept/doc-intel-workspace.md#).

<table id="choicetable_k5x_lfh_b2c"><thead><tr><th align="left" id="d41075e184">

Option

</th><th align="left" id="d41075e187">

Description

</th></tr></thead><tbody><tr><td id="d41075e193">

**Edit the field**

</td><td>

To change the field value, type a new value in the field.

</td></tr><tr><td id="d41075e205">

**Mark the field as missing in the document**

</td><td>

If you can’t find an appropriate match in the document, select **Missing in the document** in the field options menu. To undo, select the **Edit** icon \(![Edit icon.](../image/icon-docintel-edit.png)\) in the field.

</td></tr><tr><td id="d41075e229">

**Mark the field as reviewed**

</td><td>

The field will be marked as complete when you move to the next field.

 If needed, select the **Reviewed** icon \(![Completed icon.](../image/icon-docintel-completed.png)\) to mark the field as unreviewed.

</td></tr><tr><td id="d41075e253">

**Flag the field**

</td><td>

To flag the field for later attention, select **Flag for follow-up** in the field options menu \(![Field options menu icon](../image/icon-docintel-field-options-menu.png)\).

</td></tr></tbody>
</table>5.  Select the next field and repeat steps 3 to 4.

6.  Select **Submit**.

    **Note:** Generative AI may not always produce accurate, complete, or appropriate information. It is important to review all fields for accuracy before submitting.


## Result

The field values are saved. Empty fields are submitted with no values.

**Parent Topic:**[Using Now Assist in Document Intelligence](../concept/docintel-using-now-assist.md)

**Related topics**  


[Review document Q&amp;As with Now Assist in Document Intelligence](review-document-qnas-with-now-assist-document-intelligence.md)

