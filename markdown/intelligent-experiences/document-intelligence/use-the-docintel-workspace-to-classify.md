---
title: Classify documents using the Document Intelligence workspace
description: Use the Document Intelligence workspace to label your documents. The workspace enables you to train the AI model by providing direct input and by validating or correcting the recommendations provided by DocIntel.Classify your documents in the Classify panel.
locale: en-US
release: xanadu
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Complete a document task, Using Document Intelligence, Document Intelligence, Enable AI experiences]
---

# Classify documents using the Document Intelligence workspace

Use the Document Intelligence workspace to label your documents. The workspace enables you to train the AI model by providing direct input and by validating or correcting the recommendations provided by DocIntel.

## Overview of the Document Intelligence workspace

The Document Intelligence \(DocIntel\) workspace provides features that enable you to quickly apply classes or categories to the attached documents and each of their pages.

To get started with the Document Intelligence workspace, complete the following:

-   [Create a document task](../task/upload-documents-for-extraction.md) for a document classification use case, upload a document, and process the task.
-   After DocIntel has processed the task, you can begin using the workspace. See [Complete a document task](../task/extract-data-from-documents.md).

## Layout of the Document Intelligence workspace

The following image shows the Document Intelligence workspace for a document task. The workspace includes the following areas:

-   1 - Thumbnail panel
-   2 - Document image panel
-   3 - Document controls
-   4 - Classify panel

**Note:** In this view, the documents in the Classify panel are expanded so that the categories are visible.

![Areas of the Document Intelligence workspace for document classification.](../image/docintel-dc-workspace-2.png)

## Thumbnail panel

In the thumbnail panel of the workspace, you can select one page from one or more multiple-page documents. The selected page is displayed in the document image panel. Selecting a page doesn’t affect what is displayed in the Classify panel.

## Document image panel

The document image panel displays the page selected in the thumbnail panel.

## Document controls

When you’re reviewing a document for classification, you can use various controls to rotate, maximize the viewing area, zoom, or focus on the areas that you need.

## Classify panel

The Classify panel enables you to open each document and page classification for review, including viewing the AI's recommendations.

The following image shows the Classify panel with a category field for each attachment in the document task, enabling you to enter or review the category.

![Category fields in the Classify panel corresponding to the documents shown in the thumbnail panel.](../image/docintel-dc-panel-2.png)

## Classify documents and document pages

Classify your documents in the Classify panel.

### Before you begin

Role required: sn\_docintel.extraction\_agent

### About this task

Use the following steps to apply categories to document attachments and each of their pages.

In this context, a document page is the individual page object of the digital document file, as displayed in the thumbnail panel of the workspace. A document file may contain multiple logical groupings of documents \(like a PDF file with several invoices, each spanning several pages\). Based on the contents, apply the categorization to the document file and the file pages.

If the categories are already auto-filled with values, you can review them to ensure they are correct or adjust them as needed.

### Procedure

1.  In the Classify panel, review any auto-filled categories for each document to ensure they’re correct.

2.  Select a category for a document by selecting the **Category** field.

3.  Select an appropriate recommendation for the document using the recommendation list.

    -   Begin typing in the **Category** field and select a recommendation from the list.

        The recommendation with the highest [confidence score](docintel-confidence-scores.md) displays at the top of the list.

    -   Select **Mixed categories** for a multi-page document that includes more than one document type.

        Otherwise, if you select a category for a multi-page document, that category is applied to all of the document's pages.

    -   Select **Blank Page** for a blank page in a document.

    -   Select **No category found** if you can’t find a correct match.

        The document will be marked as complete when you move to the next **Category** field.

4.  Select a recommendation for each page of a Mixed categories document.

    The page will be marked as complete when you move to the next page.

5.  If needed, flag the documents or pages for later attention by selecting **Flag for follow-up** in the options menu from the options icon \( ![Options icon.](../image/icon-docintel-field-options-menu.png)\).


