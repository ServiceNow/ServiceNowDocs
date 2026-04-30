---
title: Collaborate using Docs in EAP
description: Store and manage all kinds of documentation for Agile teams and their planning items \(Epics, Capabilities, and Features\) from a centralized location of Enterprise Agile Planning workspace.
locale: en-US
release: yokohama
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Collaborate using Docs in EAP

Store and manage all kinds of documentation for Agile teams and their planning items \(Epics, Capabilities, and Features\) from a centralized location of Enterprise Agile Planning workspace.

Overview of Docs for Enterprise Agile Planning. 

## Docs overview

Product managers, team leads, and team members associated with EAP teams can store and manage information at the Agile Structure level and work level \(Epic, Capabilities, and Features\).

-   Each planning item or team in EAP can have a separate doc to capture the information related to it.

    For example, for an Epic, you create Docs for high-level business objectives or technical product requirements. Similarly at the team level, you can use Docs to capture the information related to team details, Scrum calls, iteration summaries, and so on.

-   Each planning item or Agile Structure level can have multiple Docs associated with it and each Doc can have multiple pages to help you effectively organize key artifacts. Also, the Agile Structure can organize these pages into multiple documents.
-   Predefined templates such as Iteration Retrospective, Marketing Plan, Meeting notes are available. Create pages for your Doc using one of these templates or start with an empty page. You can also create or modify the templates according to your requirements.

## Features of Docs

The following are the key features of Docs:

-   Auto-save content.
-   See who is viewing or working on a Doc using the feature of live user presence.
-   Create documents using pre-defined templates. You can edit the templates to suit your team's requirements.
-   Use rich text paragraph formatting, which includes headings, lists, alignment, and others.
-   Move text blocks to change their placement using block-level editing.
-   Tag team members inline or insert tables using the **/** command.
-   Add reference to other ServiceNow AI Platform tables to connect work across teams.
-   Insert images by uploading files or using web URLs.

    **Note:** The experience of inserting Google Images links might not work.


## Dynamic data linking in Docs

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records.

For example, if you add a reference to an Incident record, the reference will show the latest field information of the incident in Docs without requiring manual edits. Clicking the incident reference opens up the incident form so that you can view the full details of the incident and make any necessary changes.

A hover popover displays the details of the mentioned record, providing quick access to additional information without leaving the current context.

![Dynamic linking an incident record in EAP Docs.](../../collab-work-mgmt/images/cwm-docs-dynamic-record.png)

Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

![Dynamic linking the Assigned to field of an incident record in EAP Docs.](../../collab-work-mgmt/images/cwm-docs-dynamic-field.png)

You can add references from any ServiceNow table you have access to, with no setup or configuration needed.

This feature reduces the need to switch between multiple ServiceNow applications within your instance and helps maintain a single, reliable source of truth for collaborative work, making it easier for teams to stay aligned and informed.

## Draft content using Now Assist for SPM

Generate content with Now Assist for SPM directly in your Docs using custom prompts. In addition, summarize existing sections, elaborate where needed, and refine drafts to help improve your productivity.

You can interact with Now Assist directly in your Doc to create new content, add context, or improve existing sections. This helps you draft faster, refine ideas, and keep your work relevant without leaving the page.

-   **Work with content of the whole page**

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

-   **Take assistance on a blank page**

    Some examples are:

    1.  **Generate 5 icebreaker questions for a virtual team-building session.**
    2.  **Write a 3-paragraph blog post explaining why \[industry trend\] is changing how businesses operate.**
    3.  **Generate an outline for the Instagram campaign tasks for a Hackathon initiative.**

        ![Creating first draft for a page using Now Assist.](../../now-assist-cwm/images/na-blank-page-nacm.png)

-   **Answer questions in the context of this Doc**

    Whether the content in the Doc is added manually or generated using Now Assist, you can ask questions to find anything in the page's context.

    For example, if you have a project charter document, you can try asking **What is the total budget of this project and which part is the most expensive?**

    ![Ask questions in the context of the document. Here, user asks questions on project budget, in the context of a Project Charter document.](../../now-assist-cwm/images/cwm-nacm-ask-questions.png)


## Real-time collaboration within EAP Docs

With the feature of real-time collaboration, edit a Doc page concurrently with multiple other editors. Colored cursors denote the current location of each editor on the page. You can choose to show or hide these live presence indicators based on your preference while working on or reviewing the content of the page.![Real-time collaboration in EAP Docs.](../images/eap-docs-rtc.png)

**Note:** Application performance may degrade with a large number of concurrent editors.

