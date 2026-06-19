---
title: Collaborative documentation using CWM
description: Manage all kinds of documentation for work such as meeting notes, project requirements, or technical specifications using rich text Docs with real-time collaboration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/collaborative-work-management/cwm-docs.html
release: zurich
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Collaborative documentation using CWM

Manage all kinds of documentation for work such as meeting notes, project requirements, or technical specifications using rich text Docs with real-time collaboration.

Overview of collaboration within Docs for CWM workspace. Approximately two minutes long.

Docs can be created within a Space, and organized into folders. Within a Space, you can create multiple Docs and within each Doc, you can create unlimited pages to help you effectively organize your information.

## Key features of Docs

-   Auto-save content.
-   Live user presence: See who is viewing or editing the document in real time.
-   Inline comments: Leave comments on text in a document. Supported text types include plain text, hyperlinks, dynamic data, and text inside table cells.
-   Comment notifications: Get notified via email when someone @-mentions you in a comment or when a reply is added to a comment you created in a document.
-   Templates: Create and apply document templates.
-   Rich text formatting: Headings, lists, alignment, and other paragraph styles.
-   Block-level editing: Move text blocks to change placement.
-   Cross-references: Add references to other ServiceNow AI Platform tables to connect work across teams.
-   Slash command \(**/**\) for more options:
    -   Insert tables quickly
    -   Mention a record. See [Dynamic data linking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/cwm-docs.md).
    -   Insert a list.
    -   Choose formatting options.
-   Copy and paste within Docs: Transfer text, images, lists, and tables between Docs pages. Comments on text are retained when you copy or cut and paste within the same document but aren't carried over when pasting into a different document.
-   Table features:
    -   Resize column width
    -   Add color to single or multiple cells
    -   Select multiple cells using mouse or **Shift + arrow** keys
    -   Delete content from multiple cells using **Backspace** or **Delete** keys.
    -   Copy and paste cell content:
        -   Copy from one cell and paste into multiple cells.
        -   Copy from multiple cells and paste into another set of cells.
        -   Copy multiple cells and paste as a new table in an empty block.

## Images in Docs

Insert images into your Docs by uploading a file from your device or adding a web URL. Note that inserting Google Images links might not work.

Save images from your CWM documents directly to your device, making it easier to share or use them outside of the Docs environment. Click an image to access the download icon \(\[Omitted image "cwm-icon-docs-image-download.png"\] Alt text:\), then click the icon to save it to your device. Alternatively, right-click the image and use your browser's built-in save option.

\[Omitted image "cwm-docs-image-download.png"\] Alt text: Options to align and download an image in a Doc page.

## Inline comments

Add comments to specific text in documents to collaborate with other users, provide feedback, or track discussions without modifying the document content.

-   **Visual indication**

    Commented text displays with a yellow highlight and underline. Selecting the text darkens the highlight and opens a comment popover showing the comment thread. The popover closes when you click outside of it.

-   **Add a comment**

    Select text and select the Add comments icon from the inline toolbar. You can include hyperlinks by typing or pasting URLs directly into your comment. These links are automatically converted to a clickable format when you post the comment.

-   **Mention users**

    Type `@` followed by a name to mention someone in your comment. Select the user from the lookup that appears. Only users can be mentioned in a comment. Mentions are highlighted in the posted comment, and the mentioned users are notified by email.

-   **Edit your comments**

    If you're the owner of the comment, you can modify your comment text. Edited comments display an **Edited** indicator to show they have been updated.

-   **Comments on dynamic data**

    Add comments to dynamic data elements, such as references, links, and blocks of text that contain dynamic data. Click once to open the comment popover and click again to navigate to the referenced content.

-   **Comment restrictions**

    Overlapping comments on the same text are not supported—reply to existing threads instead. Comments cannot be added to non-text elements such as images and table cells.

-   **Show or hide highlights**

    Turn comment highlights on or off using the **Hide comment highlights** option in the three-dot menu. Switch between a marked-up view and a clean reading view.

-   **Export or duplication behavior**

    Comments and highlights are excluded when you export a document to PDF or duplicate it.

-   **Read-only access**

    You can add and manage comments on a document if you have read-only access to the document.

-   **Email notifications**

    Users are notified via email about the following comment activity on a document they are associated with.

    -   When a reply is added to your comment by another user.
    -   When a user is @-mentioned in a comment. Each mentioned user receives a separate notification. If you edit a comment to add @mention, only the newly mentioned user is notified.
    The notification includes up to 140 characters of the comment text and include the document name, workspace name, and the document path in the workspace hierarchy. Each notification includes a **View** button, selecting which takes you to the respective comment in the document.


## Dynamic data linking in Docs

Keep record information in your documentation current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records.

For example, if you add a reference to an Incident record, the reference shows the latest field information of the incident in Docs without requiring manual edits. Selecting the incident reference opens up the incident form so that you can view the full details of the incident and make any necessary changes.

A hover popover displays the details of the mentioned record, providing quick access to additional information without leaving the current context. Dynamic data without a comment opens on the first click. Keyboard navigation is supported.

\[Omitted image "cwm-docs-dynamic-record.png"\] Alt text: Dynamic linking an incident record in CWM Docs.

Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

\[Omitted image "cwm-docs-dynamic-field.png"\] Alt text: Dynamic linking the Assigned to field of an incident record in CWM Docs.

You can add references from any ServiceNow table you have access to, with no setup or configuration needed.

This feature reduces the need to switch between multiple ServiceNow applications within your instance. It maintains a single, reliable source of truth for collaborative work, keeping teams aligned and informed.

## Real-time collaboration within CWM Docs

With the feature of real-time collaboration, edit a Doc page concurrently with multiple other editors. Colored cursors denote the current location of each editor on the page. You can choose to show or hide these live presence indicators based on your preference while working on or reviewing the content of the page.

\[Omitted image "cwm-docs-rtc.png"\] Alt text: Doc real-time collaboration.

**Note:** Application performance may degrade with a large number of concurrent editors.

## Draft content using Now Assist for CWM

Generate content with Now Assist for CWM directly in your Docs using custom prompts. In addition, summarize existing sections, elaborate where needed, and refine drafts to help improve your productivity.

You can interact with Now Assist directly in your Doc to create content, add context, or improve existing sections. This helps you draft faster, refine ideas, and keep your work relevant without leaving the page.

-   **Work with the content of the whole page**

    Some examples are:

    -   For Marketing teams: **Create a compelling product launch announcement highlighting the key benefits and emotional appeal for our target audience.**
    -   For Legal teams: **Write a plain-language summary of the privacy policy in this doc, that customers can easily understand.**
    -   For product teams: **Analyze the customer feedback comments in this Doc, group into top 5 themes, and suggest top 3 enhancements for highest impact.**
    Now Assist uses the context from your Doc page to generate a response.

-   **Refine, elaborate, or improve the existing content within the page**

    Some examples are:

    -   If you have a list of stakeholders, you can ask **Elaborate on the scope of these roles.**
    -   **Rewrite this in a casual tone.**
    \[Omitted image "na-inline-open-text.png"\] Alt text: Now Assist inline prompt for selected content on the page.

-   **Take assistance on a empty page**

    Some examples are:

    1.  **Generate 5 icebreaker questions for a virtual team-building session.**
    2.  **Write a 3-paragraph blog post explaining why \[industry trend\] is changing how businesses operate.**
    3.  **Generate an outline for the Instagram campaign tasks for a Hackathon initiative.**

        \[Omitted image "na-blank-page-nacm.png"\] Alt text: Creating first draft for a page using Now Assist.

-   **Answer questions in the context of this Doc**

    Whether the content in the Doc is added manually or generated using Now Assist, you can ask questions to find anything in the page's context.

    For example, if you have a project charter document, you can try asking **What is the total budget of this project and which part is the most expensive?**

    \[Omitted image "cwm-nacm-ask-questions.png"\] Alt text: Ask questions in the context of the document. Here, user asks questions on project budget, in the context of a Project Charter document.


## Generate tasks from Docs and add them to Board using Now Assist for CWM

Use the generative AI capabilities of Now Assist to create tasks from the context of your Docs. From the Doc header, select **Create Tasks** and Now Assist generates task recommendations for you and walks you through to add them to the required Board in CWM workspace.

\[Omitted image "cwm-task-generation-now-assist.png"\] Alt text: Automatic task generation from CWM Docs using Now Assist for CWM.

-   **[Create a Doc in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/create-a-doc-in-cwm.md)**  
Store information related to your tasks, reference users and task records, and collaborate in real-time using Docs in Collaborative Work Management workspace.
-   **[Add comments to Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/add-comments-to-docs-in-cwm.md)**  
Add a comment to specific text in a Doc to share feedback or start a discussion without modifying the Doc content.
-   **[Manage comments in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/manage-comments-in-cwm-docs.md)**  
Edit, reply to, or delete comments in Docs to maintain relevant discussions and keep your documentation organized.
-   **[Hide or show comment highlights in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/hide-comment-highlights-cwm-docs.md)**  
Toggle comment highlight visibility in Docs to switch between a clean reading view and a markup view.
-   **[Disable comment notifications in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/disable-comment-notifications-cwm.md)**  
Turn off email notifications for comment activities in Docs to manage which comment events you're notified about.
-   **[Manage pages and subpages in CWM Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/manage-pages-and-subpages-in-cwm-docs.md)**  
Flexibly organize information for your teams and work items by creating, duplicating, and deleting pages and subpages within a Doc in Collaborative Work Management \(CWM\) workspace.
-   **[Duplicate a Doc in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/duplicate-doc-in-cwm.md)**  
Save time by duplicate an existing Doc to copy all its pages and content without having to copy the information manually in the Collaborative Work Management workspace.
-   **[Export a Doc in CWM to a PDF file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/export-a-doc-in-cwm-to-a-pdf-file.md)**  
Use the Docs offline, and share with teams or stakeholders outside Collaborative Work Management \(CWM\) by exporting Docs as PDF.

**Parent Topic:**[Using Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/collaborative-work-management/using-collaborative-work-management.md)

