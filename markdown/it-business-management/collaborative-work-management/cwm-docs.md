---
title: Collaborative documentation using CWM
description: Manage all kinds of documentation for work such as meeting notes, project requirements, or technical specifications using rich text Docs with real-time collaboration.
locale: en-US
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Collaborative documentation using CWM

Manage all kinds of documentation for work such as meeting notes, project requirements, or technical specifications using rich text Docs with real-time collaboration.

Overview of collaboration within Docs for CWM workspace. Approximately two minutes long.

Docs can be created within a Space, and organized into folders. Within a Space, you can create multiple Docs and within each Doc, you can create unlimited pages to help you effectively organize your information.

## Key features of Docs

-   Auto-save content.
-   Live user presence: See who is viewing or editing the document in real time.
-   @-mention notifications: Get notified when someone @-mentions you in a Doc.
-   Templates: Create and apply document templates.
-   Rich text formatting: Headings, lists, alignment, and other paragraph styles.
-   Block-level editing: Move text blocks to change placement.
-   Cross-references: Add references to other ServiceNow AI Platform tables to connect work across teams.
-   Slash command \(**/**\) for more options:
    -   Insert tables quickly
    -   Mention a record. See [Dynamic data linking](cwm-docs.md#section_exg_k2r_khc).
    -   Insert a list.
    -   Choose formatting options.
-   Copy and paste within Docs: Transfer text, images, lists, and tables between Docs pages.
-   Table features:
    -   Resize column width
    -   Add color to single or multiple cells
    -   Select multiple cells using mouse or **Shift + arrow** keys
    -   Delete content from multiple cells using **Backspace** or **Delete** keys.
    -   Copy and paste cell content:
        -   Copy from one cell and paste into multiple cells
        -   Copy from n number of cells and paste into another set of n number of cells
        -   Copy multiple cells and paste as a new table in an empty block

## Images in Docs

Insert images into your Docs by uploading a file from your device or adding a web URL. Note that inserting Google Images links might not work.

Save images from your CWM documents directly to your device, making it easier to share or use them outside of the Docs environment. Click an image to access the download icon \(![](../images/cwm-icon-docs-image-download.png)\), then click the icon to save it to your device. Alternatively, right-click the image and use your browser's built-in save option.

![Options to align and download an image in a Doc page.](../images/cwm-docs-image-download.png)

## Inline comments

Add comments to specific text in documents to collaborate with other users, provide feedback, or track discussions without modifying the document content.

-   **Visual indication**

    Commented text displays with a yellow highlight and underline. Clicking the text darkens the highlight and opens a popover showing the comment thread.

-   **Add a comment**

    Select text and click **Comment** from the selection toolbar. You can include hyperlinks by typing or pasting URLs directly into your comment and these links are automatically converted to a clickable format when you post the comment.

-   **Mention users**

    Type `@` followed by a name to mention someone in your comment. Select the user from the lookup that appears. Mentions are highlighted in the posted comment, and the system can trigger notifications to alert mentioned users.

-   **Edit your comments**

    If you're the owner of the comment, you can modify your comment text. Edited comments display an **Edited** indicator to show they have been updated.

-   **Comments on dynamic data**

    Add comments to dynamic data elements such as references and links. Click once to open the comment popover, or click again while the popover is open to navigate to the referenced content.

-   **Comment restrictions**

    Overlapping comments on the same text are not supported—reply to existing threads instead. Comments cannot be added to non-text elements such as images and table cells.

-   **Show or hide highlights**

    Toggle comment highlights on or off to switch between a marked-up view and a clean reading view.

-   **Export behavior**

    Comments and highlights are excluded when you export a document to PDF or duplicate it.

-   **Read-only access**

    Users with read-only document access can still add and view comments.


## Dynamic data linking in Docs

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records.

For example, if you add a reference to an Incident record, the reference shows the latest field information of the incident in Docs without requiring manual edits. Selecting the incident reference opens up the incident form so that you can view the full details of the incident and make any necessary changes.

A hover popover displays the details of the mentioned record, providing quick access to additional information without leaving the current context.

![Dynamic linking an incident record in CWM Docs.](../images/cwm-docs-dynamic-record.png)

Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

![Dynamic linking the Assigned to field of an incident record in CWM Docs.](../images/cwm-docs-dynamic-field.png)

You can add references from any ServiceNow table you have access to, with no setup or configuration needed.

This feature reduces the need to switch between multiple ServiceNow applications within your instance and helps maintain a single, reliable source of truth for collaborative work, making it easier for teams to stay aligned and informed.

## Real-time collaboration within CWM Docs

With the feature of real-time collaboration, edit a Doc page concurrently with multiple other editors. Colored cursors denote the current location of each editor on the page. You can choose to show or hide these live presence indicators based on your preference while working on or reviewing the content of the page.

![Doc real-time collaboration.](../images/cwm-docs-rtc.png)

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
    ![Now Assist inline prompt for selected content on the page.](../../now-assist-cwm/images/na-inline-open-text.png)

-   **Take assistance on a empty page**

    Some examples are:

    1.  **Generate 5 icebreaker questions for a virtual team-building session.**
    2.  **Write a 3-paragraph blog post explaining why \[industry trend\] is changing how businesses operate.**
    3.  **Generate an outline for the Instagram campaign tasks for a Hackathon initiative.**

        ![Creating first draft for a page using Now Assist.](../../now-assist-cwm/images/na-blank-page-nacm.png)

-   **Answer questions in the context of this Doc**

    Whether the content in the Doc is added manually or generated using Now Assist, you can ask questions to find anything in the page's context.

    For example, if you have a project charter document, you can try asking **What is the total budget of this project and which part is the most expensive?**

    ![Ask questions in the context of the document. Here, user asks questions on project budget, in the context of a Project Charter document.](../../now-assist-cwm/images/cwm-nacm-ask-questions.png)


## Generate tasks from Docs and add them to Board using Now Assist for CWM

Use the generative AI capabilities of Now Assist to create tasks from the context of your Docs. From the Doc header, select **Create Tasks** and Now Assist generates task recommendations for you and walks you through to add them to the required Board in CWM workspace.

![Automatic task generation from CWM Docs using Now Assist for CWM.](../../now-assist-cwm/images/cwm-task-generation-now-assist.png)

-   **[Create a Doc in CWM](../task/create-a-doc-in-cwm.md)**  
Store information related to your tasks, reference users and task records, and collaborate in real-time using Docs in Collaborative Work Management workspace.
-   **[Add comments to Docs in CWM](../task/add-comments-to-docs-in-cwm.md)**  
Streamline collaboration by turning your documents into living conversations. Highlight any passage, add a comment, and watch the discussion through threads, all without leaving the page or switching applications.
-   **[Manage pages and subpages in CWM Docs](../task/manage-pages-and-subpages-in-cwm-docs.md)**  
Flexibly organize information for your teams and work items by creating, duplicating, and deleting pages and subpages within a Doc in Collaborative Work Management \(CWM\) workspace.
-   **[Duplicate a Doc in CWM](../task/duplicate-doc-in-cwm.md)**  
Save time by duplicate an existing Doc to copy all its pages and content without having to copy the information manually in the Collaborative Work Management workspace.
-   **[Export a Doc in CWM to a PDF file](../task/export-a-doc-in-cwm-to-a-pdf-file.md)**  
Use the Docs offline, and share with teams or stakeholders outside Collaborative Work Management \(CWM\) by exporting Docs as PDF.

**Parent Topic:**[Using Collaborative Work Management](using-collaborative-work-management.md)

