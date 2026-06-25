---
title: Collaborative Work Management release notes
description: The ServiceNow Collaborative Work Management \(CWM\) application provides a central hub to plan, visualize, and collaborate on work with team members across your organization. CWM was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Collaborative Work Management release notes

The ServiceNow® Collaborative Work Management \(CWM\) application provides a central hub to plan, visualize, and collaborate on work with team members across your organization. CWM was enhanced and updated in the Australia release.

## Collaborative Work Management highlights for the Australia release

-   Save time and effort by importing existing tasks and stories into CWM.
-   Find relevant work easily by using filters in the Kanban view.
-   Generate scrum tasks for user stories using AI and improve visibility into sprint work.
-   Spot bottlenecks early by linking work items as blocking or related, with visual cues that surface dependencies across Kanban, List, and Gantt views.
-   Add inline comments and @mention colleagues in Docs and receive email notifications for replies and mentions.

See [Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/cwm-landing.md) for more information.

**Important:** Collaborative Work Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Import tasks into CWM Boards using Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/importing-tasks-cwm-boards.md)**

    Reduce manual effort when onboarding existing work to CWM by importing tasks or stories from spreadsheets, documents, or images. Upload a file and Now Assist analyzes the data and proposes how each source column maps to a column on your Board.

    Review and adjust the AI-proposed mapping, add source columns as new custom columns if needed, and preview the full task list before confirming. The import runs in the background and a workspace notification reports the outcome when it completes.

-   **[Inline comments and email notifications in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/add-comments-to-docs-in-cwm.md)**

    Streamline collaboration by enabling inline comments in Docs. Select text to add a comment, mention colleagues using @, and include hyperlinks by pasting URLs. You can comment on plain text, hyperlinks, dynamic data, and text inside table cells, and track discussions through threads, all without leaving the page or switching applications.

    Email notifications with comment details, document name, workspace name, and document path are sent when a reply is added to your comment or when you're @-mentioned. Each notification includes a button that opens the document and navigates directly to the comment. Edit or delete your comments and choose to show or hide comment highlights. Users with read-only access can add comments and participate in comment threads.

-   **[Team member roles for project work](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/cwm-team-member-roles.md)**

    View and update project and demand tasks directly in CWM using team member roles, installed alongside Collaborative Work Management.

    The team member read role lets users view project and demand tasks and leave comments. The team member read-write role also lets users edit those tasks. Team members can view and manage the work assigned to them and their team through **My Work** and **Connected Work** in CWM.

-   **[Formula columns in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/add-formula-column-cwm-boards.md)**

    Gain deeper insights into your work by adding formula columns to your List view in CWM Boards. Create calculations that automatically compute values across your tasks, such as summing hours, calculating date differences, or deriving metrics from existing fields.

    Build formulas manually using the Formula Builder panel, which guides you through selecting functions and referencing columns with inline suggestions. As you type, the builder validates your formula in real-time and displays clear error messages if corrections are needed.

    You can accelerate formula creation with AI by describing your calculation in natural language. AI generates a valid formula that you can insert directly into the editor, saving you the time to manually build a valid formula.

-   **[Kanban board filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/cwm-board-views.md)**

    Save time finding the work that matters most by applying quick filters directly on your Kanban board.

    As you adjust filter conditions in the header, the quick filter panel stays in sync, and vice versa. Your filter choices automatically apply to saved views and CWM Board templates, so the next time you open the board, your preferences are readily available.

-   **[Scrum tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/managing-scrum-tasks-for-stories-cwm.md)**

    Improve sprint execution by breaking user stories into scrum tasks that make estimation easier and daily progress visible. These tasks appear as nested children in the List, Kanban, and Sprint planning views, so that your team sees how individual efforts roll up into the larger story.

    Using AI to generate an initial set of scrum tasks based on your story descriptions, you can reduce the overhead of task creation. Trigger scrum task generation from the story form or from the Sprint planning view. The result is a relevant set of tasks to use as a starting point. You can then review, edit, and add the generated tasks to fit your team's workflow.

-   **[Task dependencies and relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/managing-task-dependencies-relationships-cwm.md)**

    Increase visibility into how work is connected by linking related items directly in CWM and avoid switching context to track dependencies.

    As these relationships surface across Kanban, List, and Gantt views with clear visual cues, you can improve planning confidence for your teams. Blocked items stand out at a glance, helping teams spot bottlenecks early, communicate delays quickly, and plan tasks in the right sequence.

-   **[Image download from docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/cwm-docs.md)**

    Save images from your CWM documents directly to your device, making it easier to share or use them outside of the Docs environment.


## UI changes

-   **[Inline comments changes in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/cwm-docs.md)**
    -   The Add comments icon appears in the inline toolbar.
    -   Commented text displays a yellow highlight and underline. Selecting commented text darkens the highlight and opens a comment popover showing the full thread, including reply count, user avatars, names, and relative timestamps.
    -   The comment popover provides options to edit or delete comments. Edited comments display an **Edited** indicator.
    -   Users can turn highlights on or off using the **Show comment highlights** or **Hide comment highlights** options in the More actions menu of the document.
-   **[Formatting toolbar changes in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/cwm-docs.md)**

    Quickly confirm which text formatting is active for your text selection. A green checkmark now appears next to the currently applied format in the formatting toolbar, giving you a clear visual indicator of the active formatting.

-   **[Sprint section footer changes in Sprint planning view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-sprint-planning-in-cwm.md)**

    For sprints that are not started yet, the footer of the sprint section in the Sprint planning view now shows only the % of capacity utilized, and the story points remaining for the sprint.


## Activation information

Install Collaborative Work Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

    Docs in CWM Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.


## Related ServiceNow applications and features

-   **[Now Assist for Collaborative Work Management \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-cwm-landing.md)**

    The ServiceNow®Now Assist for CWM application uses generative AI skills to save time and improve efficiency for the actions you perform within the CWM workspace.

-   **[Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/alignment-planner-workspace-landing-page.md)**

    Prioritize, roadmap, and track work when using traditional, Agile, or hybrid methodologies with the ServiceNow® Strategic Planning application. Align strategy to execution by defining and tracking goals across your organization. Strategic Planning is available with an SPM Professional license.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-business-management-rn-landing.md)

