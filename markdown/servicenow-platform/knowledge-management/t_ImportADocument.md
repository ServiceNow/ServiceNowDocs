---
title: Import a Word document to a knowledge base using Knowledge Management v3
description: Import a Microsoft Word document using Knowledge Management v3 homepage to create a knowledge article.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using the homepage of Knowledge Management v3, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Import a Word document to a knowledge base using Knowledge Management v3

Import a Microsoft Word document using Knowledge Management v3 homepage to create a knowledge article.

## Before you begin

You must have contribute access for at least one active knowledge base.

**Note:**

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in the future Y release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers on Madrid and later releases. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

The **Import Articles** button does not appear in the following conditions:

-   The Import Articles module is available in the application navigator.

    **Note:** Beginning with Madrid, the Import a Word document feature is enabled by default and the Import Articles module is displayed in the application navigator. The Import a Word document feature isn’t enabled automatically for the existing customers who can continue using the **Import Articles** option on the Knowledge Management v3 page. For more information, see [Import a Word document to a knowledge base](import-word-platform.md).

-   You cannot contribute to any knowledge base.

**Note:** An administrator can control the visibility of the **Import Articles** button by setting the other knowledge property **Hide the 'Import' functionality \(button and drag-n-drop\) for all users** \(**glide.knowman.import.hide\_import\_functionality**\) to true.

Role required: None

## About this task

You can import Microsoft Word documents in the .doc and .docx file formats.

**Note:** The file extension must be lowercase.

When you import a document, text content from the document is used to create the knowledge article. The articles support all editing functions [supported by the TinyMCE editor](https://www.servicenow.com/docs/access?context=r_EditingFunctions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). All HTML supported by TinyMCE such as tables, lists, and links, as well as styling such as bold and italics, are preserved. Images from the document are added as attachments to the knowledge article and embedded in the article body.

**Note:**

You can import multiple files at a time. Closing the browser or navigating away cancels any in-progress uploads but does not delete articles created from completed imports.

You cannot import documents to knowledge from mobile devices.

The following styles and elements are preserved when importing a .doc or .docx file into a knowledge base. Styles and elements not included in this list may not be preserved when importing a document.

-   Titles
-   Headings

    **Note:** Only default heading settings are supported. For any headings and subheadings with numbers, the numbers are not imported.

-   Images

    **Note:** Images may not be aligned exactly as in the Word document you import.

-   Links

    **Note:** Links are preserved for documents with .docx format only.

-   Bold text
-   Italic text
-   Underlined text
-   Ordered and unordered lists

    **Note:** After import, the bullets in an unordered list are replaced with dots.

-   Tables

    **Note:** Only default heading settings are supported. Custom heading styles are imported using the default settings for those styles. Table styling and borders are not supported.


## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Knowledge**.

2.  Select one or more document files and drag onto the knowledge homepage.

3.  Select the **Knowledge base** to add the new article to.

    You can select only knowledge bases you can contribute to.

4.  Select a **Category** from within that knowledge base.

    **Note:** Use the category picker to add a category. The picker does not differentiate between the different category levels. You can select a category or sub category and add it to the **Category** field.

5.  Select the **Publish** check box to start the publishing workflow for each imported article immediately after the import finishes.

    This check box applies only when importing to v3 knowledge bases and only if the **Show publish checkbox on the knowledge import pop-up** property is set to **Yes** on the Knowledge Management properties form. You cannot automatically publish articles imported to v2 knowledge bases.

    Knowledge v2 articles go into **Draft** state. Knowledge v3 articles go into **Review** or **Published** state, depending on the workflow attached to the knowledge base \(Approval Publish or Instant Publish\).

6.  Select **Import**.

    A new article is created in the selected knowledge base and category using the content from the uploaded document. If you uploaded multiple documents, one article is created for each. If you use knowledge internationalization, the language of the new article is set to the currently selected system language.

    After the upload completes, a popup window appears displaying the number and short description of the newly-created articles. Click an article to view the full record.

    If any errors occur during the upload, a popup window appears to display the error.


**Parent Topic:**[Using the homepage of Knowledge Management v3](../concept/c_KnowledgeHomepage.md)

**Related topics**  


[Import a Word document to a knowledge base](import-word-platform.md)

