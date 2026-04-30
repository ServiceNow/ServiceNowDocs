---
title: Collaborative Work Management release notes
description: The ServiceNow Collaborative Work Management \(CWM\) application provides a central hub to plan, visualize, and collaborate on work with team members across your organization. CWM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 9
---

# Collaborative Work Management release notes

The ServiceNow® Collaborative Work Management \(CWM\) application provides a central hub to plan, visualize, and collaborate on work with team members across your organization. CWM was enhanced and updated in the Zurich release.

## Collaborative Work Management highlights for the Zurich release

-   Plan, track, and manage team work in Agile methodology with sprint planning in the CWM workspace.
-   Streamline task management for teams by integrating various work items across ServiceNow applications into CWM Boards.
-   Filter and group work by vertical and horizontal swimlanes in the Kanban view for a specific work item type.

See [Collaborative Work Management](https://www.servicenow.com/docs/access?context=cwm-landing&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

**Important:** Collaborative Work Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Enterprise Agile Planning \(EAP\) integration with CWM](https://www.servicenow.com/docs/access?context=integrate-eap-with-collaborative-work-management&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Enhance visibility and streamline planning for your teams with EAP integration into CWM.

    For Agile teams managing non-agile work items like incidents and change tasks, this integration bridges the gap by automatically creating a dedicated Space and Board in CWM. Agile work is seamlessly brought over via Connected Work, while EAP sprints are reflected directly in CWM’s Sprint planning view, thus enabling unified planning across all work types. Teams can plan work for their sprints and update work status directly from the CWM Board, with performance reports in EAP dynamically reflecting these changes. This integration enables teams to manage their full scope of work from a single, connected workspace.

-   **[Board preferences](https://www.servicenow.com/docs/access?context=cwm-boards&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Reduce cognitive load and focus on the most relevant and actionable tasks by filtering work items on CWM boards based on their last updated date and hiding those items marked as Closed complete. From the Board preferences menu on the Board header, you can choose to show items last updated within 7 days, 30 days, 90 days, 120 days, or 1 year.

-   **[Kanban card layout settings](https://www.servicenow.com/docs/access?context=cwm-board-views&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Surface the information that's most relevant to you using Card Layout settings for Kanban view of a CWM Board. You can now personalize Kanban cards by selecting up to five fields to display on them. For a cleaner, distraction-free view, you can enable the Compact layout, which shows only the work item name on the card. Alternatively, the Full view shows all selected fields, offering better context directly on the card. Based on your workflow needs, tailor your workspace to enhance the way you track tasks.

-   **[Dynamic data linking in CWM Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

    You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Agile sprint planning in CWM](https://www.servicenow.com/docs/access?context=agile-sprint-planning-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Plan, track, and manage work for your teams by using Agile sprint planning in the CWM workspace. You can use CWM to manage tasks in multiple methodologies including ad hoc, waterfall, and Agile practices.

    -   View such details as the backlog, current sprint, and future sprints at a glance from the Sprint planning view of the CWM Board.
    -   Add Agile item types, such as stories, with other CWM tasks to the backlog.
    -   Create sprints with a custom duration and sprint capacity.
-   **[Connected work in CWM](https://www.servicenow.com/docs/access?context=unified-boards-for-connected-work-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Streamline team collaboration and planning by enabling your teams to view and plan all their work in one place by connecting work across multiple ServiceNow applications. By defining the type of work you want to connect to CWM, you can bring in records from other applications into CWM Boards.

    After the records are added to a CWM Board, your teams can update their status and other details from within CWM, or perform sprint planning for all the work on the Board. This unified experience improves efficiency because your teams don't have to switch between multiple workspaces.

-   **[Navigation panel enhancements](https://www.servicenow.com/docs/access?context=cwm-spaces&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Move Spaces, Boards, and Docs around in the navigation panel of the workspace by using the drag and drop functionality.

-   **[Enhancements to Kanban view](https://www.servicenow.com/docs/access?context=cwm-board-views&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Quick filters: Filter the tasks based on the work type that you would like to see in the Kanban view of a CWM Board. You can select single or multiple work item types based on the swim lanes selected. Any filters that you apply to the Kanban view are specific to this view and aren't applied to List or Gantt views.
    -   Horizontal lanes: Group the cards on the Kanban view by using a vertical and horizontal lane for improved visibility into the type and progress of work. You can save horizontal lane preference into Board views and templates.
-   **[Copying and pasting content within Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Copy and paste the content such as text, images, lists, and tables from one Doc page to another. The following content is supported for the copy and paste action:

    -   Text blocks with existing formatting
    -   Bulleted and numbered lists
    -   Tables
    -   Images
    -   Single and multiple paragraph blocks into a table cell
    -   Lists into a table cell
    -   Images into a table cell
-   **[New keyboard shortcuts](https://www.servicenow.com/docs/access?context=cwm-spaces&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Create Space:
        -   macOS: Option + S
        -   Windows OS: Alt + S
    -   Create Board:
        -   macOS: Option + B
        -   Windows OS: Alt + B
    -   Create Doc:
        -   macOS: Option + D
        -   Windows OS: Alt + D
-   **[Keyboard shortcut enhancements within CWM Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Insert a URL in the Doc:
        -   macOS: Cmd + K
        -   Windows OS: Ctrl + K
    -   Insert a new row in a table after the last row: Enter
    -   Move to adjacent cells within a table: Arrow keys
    -   Create a new list item within an existing list in a table or paragraph: Enter
    -   Create a new line in the same bullet point: Shift + Enter
    -   Indent a list item: Tab

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[My Work enhancements](https://www.servicenow.com/docs/access?context=my-work-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Track all your work from one place using the enhanced My Work in CWM. My Work now supports all ServiceNow task records-such as incidents, changes, and requests-whether they originate in CWM or outside, giving you a unified view of everything assigned to you. This helps you stay on top of overdue or open tasks and improves on-time delivery.

    Additionally, the Item type filter has been refined to show all CWM tasks \(including custom ones\) grouped under a single category, instead of listing every CWM task type individually. You’ll also only see task types in the filter that you’re actually assigned to, reducing clutter and making it easier to filter what matters.

-   **[Enhancements to tables in Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Resize the column width of a table per your preference.
    -   Add color to single or multiple table cells.
    -   Select multiple cells of a table using the mouse device or by pressing **Shift+ one of the arrow keys** on the keyboard.
    -   Delete content from multiple cells using the **Backspace** or **Delete** keys.
    -   Copy and paste cell content:
        -   Copy content from one cell and paste it to multiple cells.
        -   Copy content from n number of cells and paste it to another set of n number of cells.
        -   Copy content from multiple cells and paste it as a new table in an empty block on the page.
-   **[Enhancements to CWM Board templates](https://www.servicenow.com/docs/access?context=templates-in-cwm-for-spaces-boards-and-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Save template: While saving a Board as a template, choose between saving the current view or all shared views. You can see the number of Board views and custom task types that are included in this template.

        These details are displayed in the Template Center, where you can select a template that best meets your team's needs.

    -   Apply template: While applying a Board template, you can see the number of Board views and custom task types that you get if you apply this template. The Board views drop-down list lets you switch between views and provides information on the type of views that are enabled in this template.

        Only those custom columns that are part of these views are brought over when you apply this template.

-   **[Collaborating with Spaces in CWM](https://www.servicenow.com/docs/access?context=cwm-spaces&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    When a user is added to the **Assigned to** field of a CWM task but doesn't yet have access to the Space, the email notification requesting access is sent only to the Space owners. This way, there's less email clutter for all the Space users because notifications are sent to only those users who need to know this information.

-   **[New columns for CWM tasks](https://www.servicenow.com/docs/access?context=agile-sprint-planning-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Every task within a CWM Board has new columns called Sprint and Story points. You can use these columns if you choose to plan any task into Sprints. These columns are available on every type of work item, including the items that are brought into the Board through Connected work.

-   **[Changes within CWM Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Open the keyboard shortcut panel:
        -   macOS: Cmd + Option + K
        -   Windows OS: Ctrl + Alt + K
    -   Images can be resized after inserting them within a table cell.
    -   The page name can be updated by editing the name and clicking anywhere on the Doc.
    -   Moving content blocks to within a numbered list or deleting a list item from a list automatically adjusts the list numbering.

## Activation information

Install Collaborative Work Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    The ServiceNow®Now Assist for CWM application uses generative AI skills to save time and improve efficiency for the actions you perform within the CWM workspace.

-   **[Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Prioritize, roadmap, and track work when using traditional, Agile, or hybrid methodologies with the ServiceNow® Strategic Planning application. Align strategy to execution by defining and tracking goals across your organization. Strategic Planning is available with an SPM Professional license.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

