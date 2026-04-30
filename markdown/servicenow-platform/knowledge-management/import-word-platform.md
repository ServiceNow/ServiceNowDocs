---
title: Import a Word document to a knowledge base
description: Import a Word document to create a knowledge article.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Import a Word document to a knowledge base

Import a Word document to create a knowledge article.

## Before you begin

You must have **Can Contribute** access to at least one active knowledge base.

Role required: knowledge

## About this task

Beginning with Madrid, the Import a Word document feature is enabled by default and the Import Articles module is displayed in the application navigator. All existing customers will be able to use the **Import Articles** option on the Knowledge Management v3 homepage. For customers who are in versions prior to Madrid can enable the Import a Word document feature, an administrator must first disable the **Import Articles** option on the Knowledge Management v3 homepage by setting the **glide.knowman.import.hide\_import\_functionality** property to true and adding the Import Articles module to the application navigator.

These styles and elements are preserved when importing a .doc or .docx file into a knowledge base. Styles and elements not included in this list may not be preserved when importing a document.

-   Titles
-   Headings

    **Note:** Only default heading settings are supported. For any headings and subheadings with numbers, the numbers are not imported.

-   Images

    **Note:** Images may not be aligned exactly as in the Word document you import.

-   Links
-   Bold text
-   Italic text
-   Underlined text
-   Ordered and unordered lists

    **Note:** After import, the bullets in an unordered list are replaced with dots.

-   Tables

    **Note:** Only default heading settings are supported. Custom heading styles are imported using the default settings for those styles. Table styling and borders are not supported.


**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles** &gt; **Import Articles**.

2.  Enter the knowledge base to add the article to.

3.  Select a **Category** from within the knowledge base.

    **Note:** Use the category picker to add a category. The picker does not differentiate between the different category levels. You can select a category or sub category and add it to the **Category** field.

4.  Select the **Publish** check box to start the publishing workflow for each imported article immediately after the import finishes.

    **Note:** The **Publish** check box appears only when the **Show publish checkbox on the knowledge import pop-up** property is enabled. To enable the property, navigate to **Knowledge** &gt; **Administration** &gt; **Properties** and select the check box for the **Show publish checkbox on the knowledge import pop-up** property.

5.  Select one or more Word files to import.

6.  Click **Import**.

    ![Import word document(s) to create knowledge base articles](../image/import-word-article.png)

    An article is created in the selected knowledge base and category using the content from the uploaded document.

    -   If you uploaded multiple documents, one article is created for each.
    -   If you use knowledge internationalization, the language of the article is set to the system language selected.
    -   When the upload completes, a pop-up window displays the number and short description of the articles. Click an article to view the full record.
    -   If any errors occur during the upload, a pop-up window displays the error.
    -   If the **Publish** check box is activated, knowledge articles go into **Review** or **Published** state, depending on the workflow attached to the knowledge base.
    -   If the **Publish** check box is not activated, the knowledge articles go into **Draft** state and are then reviewed before publishing.

**Related topics**  


[Import a Word document to a knowledge base using Knowledge Management V3](t_ImportADocument.md)

