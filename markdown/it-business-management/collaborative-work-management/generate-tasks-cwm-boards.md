---
title: Create CWM tasks or stories from files or open prompts
description: Generate tasks or stories for a Board by describing the work in a natural language prompt or by uploading a document. AI analyzes the input to propose a list of actionable tasks or stories for you to review and select, saving time and manual effort.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/generate-tasks-cwm-boards.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 3
keywords: [generate tasks, Collaborative Work Management, ServiceNow Otto, document intelligence]
breadcrumb: [Add tasks to a CWM Board, Manage work using Boards, Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Create CWM tasks or stories from files or open prompts

Generate tasks or stories for a Board by describing the work in a natural language prompt or by uploading a document. AI analyzes the input to propose a list of actionable tasks or stories for you to review and select, saving time and manual effort.

## Before you begin

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

-   Verify that ServiceNow Otto for CWM is active on your instance.
-   A reference file in one of these formats: .doc, .docx, .pdf, .xls, .xlsx, .png, .jpg, or .jpeg. Maximum file size: 50 MB.

Role required: sn\_cwm\_ai.cwm\_ai\_user

## About this task

Turn narrative or semi-structured content, such as meeting notes, brainstorming planning docs, or epic PRDs documents, into a list of actionable tasks or stories on a Board. The actionable work items are identified by AI and mapped to the appropriate CWM fields. The tasks are created with a short description, description, and predefined columns. If the context is sufficient, it can create custom columns and map the fields accordingly.

**Note:** AI-generated tasks are proposals based on the context you provide. Review each task for accuracy and completeness before adding it to the Board.

## Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  From a Space, select a Board to generate tasks for.

3.  From the Board header, select **Create with Otto**.

4.  Select **Generate tasks**.

    \[Omitted image "cwm-generate-tasks-option.png"\] Alt text: Board header showing the Create with Otto menu with the Generate tasks option.

    The **Generate tasks** dialog opens with two steps: **Provide Context** and **Review Tasks**.

    \[Omitted image "cwm-generate-contextual-tasks.png"\] Alt text: Generate tasks using context or uploaded reference files.

5.  From the **Work item type** list, select the type of record to generate tasks as.

    You can choose **CWM Tasks** or **Stories**. The context to CWM column mapping in the next step depends on this choice.

6.  In the **Context** field, describe the tasks you want to generate.

    For example: `6-month digital transformation to modernize legacy systems, migrate data to the cloud, and redesign the customer portal. Include tasks for change management and stakeholder communication.`

7.  Select **Add file** to attach one or more reference documents for AI to analyze.

    **Note:** If a document can't be processed, an error message indicates the issue. Common causes include files that are too large, too complex, or corrupted.

8.  Select **Proceed**.

    AI analyzes your context and any attached documents, and the dialog advances to the **Review Tasks** step.

9.  On the **Review Tasks** step, review the tasks to add.

    A banner displays the number of tasks generated. No tasks are selected by default.

10. Select the tasks to add.

    \[Omitted image "cwm-generate-contextual-tasks-review.png"\] Alt text: Review the generated tasks and select the ones you want to add to your board.

11. Select **Back** to return to the **Provide Context** step.

    Your context text, attached files, and selected documents are retained. You can select another work item type and proceed to generate them.

12. Select **Confirm and add**.

    The dialog closes. A banner confirms that task creation is underway in the background and that you will be notified when it's complete.


## Result

A workspace notification confirms the outcome:

-   If all tasks are added successfully, the notification shows the count of records added to your Board.
-   If some tasks are added, the notification shows the count of records imported and indicates that some items were not processed.
-   If task creation fails completely, the notification states that tasks could not be added to the Board.

## What to do next

Open the Board to review the added tasks. Edit individual tasks from the side panel or by inline editing in the grid.

**Parent Topic:**[Add tasks to a CWM Board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/add-tasks-to-board-in-cwm.md)

