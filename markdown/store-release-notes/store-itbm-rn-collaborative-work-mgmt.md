---
title: Collaborative Work Management release notes
description: Version history for the Collaborative Work Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-collaborative-work-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Collaborative Work Management release notes

Version history for the Collaborative Work Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.0.2 - June 2026**
    -   New:
        -   Team Member Role for SPM Project Workspace - Enables team members with a cwm license to access and modify project workspace actions. Users can perform CRUD operations on project tasks, demand, and idea tables, and have calendar access. Role assignments and permissions are managed to enhance collaboration within the workspace.
        -   AI-powered import of Tasks and Stories into CWM Boards from spreadsheets, documents, and images using Now Assist.
        -   Comments in CWM Docs i.e. add inline comments on selected text, links, records. The portion of content with a comment is highlighted in yellow.
-   **Version 9.0.1 - April 2026**

    No updates.

-   **Version 9.0.0 - March 2026**
    -   New:
        -   Formula columns: Create custom columns of the type Formula in CWM Boards.
            -   Calculations on custom columns: Add formula type custom columns directly to list view of a CWM Board to automatically compute values across tasks. E.g. Calculate date differences or derive custom metrics from existing columns, without leaving your board.
            -   Formula Builder Panel: Build formulas with a guided panel that offers searching appropriate function and columns as you type. No need to memorize syntax, the builder surfaces available options contextually.
            -   Real-Time Validation &amp; Error Messages: Formulas are validated instantly as you write them in the editor. Clear, actionable error messages surface immediately so you can correct issues before saving thus reducing trial and error. There also error guard rails in place for any kind of column level or cell level error.
        -   Scrum tasks: Create Scrum tasks for an Agile story in CWM Boards
        -   Task relationships: Increase visibility into how work is connected by linking related items directly in CWM and avoid switching context to track dependencies.
        -   Open completed sprints in platform list view from sprint planning view in CWM
        -   Filters in Kanban view
    -   Changed: Side panel for the task details is now changed to a Full length height to provide more space for the task information
    -   Fixed: Security fix and minor fixes related to CWM Space access sharing
-   **Version 8.0.2 - December 2025**
    -   New:
        -   Expanded Task types Support in CWM My Work
            -   Tracks all ServiceNow tasks types, not just CWM, Project, or Risk tasks
            -   The My Work only displays those tasks that have been assigned to the user
            -   Sort work by priority, due date, or state for better visibility in the list tab
            -   Click the source link on any task to open its associated workspace or UI16 form in a new browser modal
        -   Scalable Auto-Bucketing &amp; Work type Filters in My Work
            -   Task states are now automatically grouped into three standard state buckets, and priorities into five priority buckets, based on their native state/priority values
            -   States &amp; Priority buckets are for visualization only- These are not new fields for any tasks types
            -   Enhanced work filter surfaces other record types like Epic, Story, Incidents, Change Requests, CatalogTasks etc in My Work
            -   Work type filter also groups all custom CWM task types together as one task type i.e. CWM Tasks
        -   Board preference for hide completed task records
        -   Kanban card enhancements to configure the required fields displayed in each cards
    -   Fixed: Improved CWM workspace loading time
-   **Version 7.0.2 - October 2025**

    Changed: Adjusted task import process to exclude child tasks unless explicitly required.

    Fixed:

    -   Newly created tasks now appear immediately in List view without requiring a refresh.
    -   Board Stability: Resolved an issue where boards failed to load for some users.
    -   Connected Work: Fixed issue where connected work columns were not visible in column configuration, even after list view updates.
    -   Addressed issue where rm\_story records records were not visible in Kanban view.
    -   Improved performance when searching tables in the Connect Work modal.
    -   Restored the sys\_updated\_on column that was missing after upgrading CWM from version 6.0.3 to 7.0.0.
    -   Fixed issue with saving Docs templates from the left navigation.
-   **Version 7.0.0 - August 2025**
    -   New:
        -   Connected work in CWM: Bring any task type work item across the ServiceNow platform into a CWM Board
        -   Sprint planning in CWM: Support Agile methodology of planning work and executing them in sprints for a CWM Board
        -   Kanban view supports filtering work items based on their types
    -   Enhancements:
        -   Only Space Owners will receive the email to approve/reject the CWM permission request
        -   CWM Content tree now supports drag and drop
        -   CWM templates for Boards:
            -   While applying a Board template, in template preview you can see the number of Board views, and custom task types that is included in the template. There is Board views dropdown in the preview along with an info icon suggesting which views\(list/Gantt/Kanban/Sprint planning\) are enabled
            -   While saving a Board as a template, choose between saving the current view or all shared views. You can see the number of Board views, CWM custom task types that will be included into this template.
        -   Keyboard shortcuts to Create Space, Board, and Doc
-   **Version 6.0.3 - June 2025**

    Minor fixes and improvements.

-   **Version 6.0.0 - May 2025**
    -   New:
        -   Improved focus and navigation
            -   Single Space view in navigation panel: To minimize distractions and help improve focus, the left navigation panel now displays only the currently active space. Switch between spaces using a newly introduced dropdown menu, offering a cleaner and more focused experience.
            -   Resizable and collapsible navigation panel: The left panel is now resizable and can also be collapsed entirely which allows customization of the workspace layout according to your preferences and screen size.
        -   Workspace-level search: Search across Spaces, Boards, and Documents within the CWM workspace. Search results provide direct navigation, allowing quick access to the required item.
        -   Visual feedback for task Completion in the List view
            -   When an individual task is completed, a brief visual effect is shown at the cell level.
            -   When all tasks in a board are marked complete, a board-level animation provides visual confirmation of full completion.
    -   Changed:
        -   Reordering of child tasks: Child tasks in the List view can now be reorderd, improving readability and simplifying error identification.
        -   Automation step numbering: Automations now include step-wise numbering, making it easier to identify errors and detect cycles. This improvement simplifies troubleshooting and improves clarity when configuring complex automation flows.
    -   Removed: Data Model Simplification: The sn\_cwm\_task\_custom table is deprecated. All its columns are merged into the sn\_cwm\_task table.
-   **Version 5.0.0 - February 2025**
    -   Requesting access to a Space or Board from its URL
        -   CWM users can quickly request access to a Space or Board through the Request access button which sends an actionable email request to the Space owner
        -   Space owners can approve or reject the request directly from the email without having to open the CWM workspace
    -   Requesting to elevate user access role to Editor
        -   Understand if your access to the Board is limited to the Viewer role using the Viewing mode indicator on the Board header. Selecting the indicator enables you to send a request to the Space owner to elevate your role to Editor. Managing access in the Share permissions modal Easily identify users who already have access to your Space and the users who requested access, using the following two sections in the Share permissions modal.
            -   People with Access section: Manage the access level of existing collaborators to Editor, Viewer, or Owner, or remove them from the Space
            -   Pending Access section: Review requests from users and choose to grant or deny them access to your Space
    -   Managing Space permissions for task assignees and other users
    -   Identify task assignees who don't have access to the workspace through a lock icon next to the user name. This icon is visible in the columns of the type People, such as Assigned to, Additional Assignee, and Assignment group, in the List view of the Board.
    -   You can either use the workspace prompt to grant them Viewer access or choose to manage their access level later from the Share permissions modal. Share task details with Task URLs
    -   Copy a link to the specific CWM Task record to share with team members and stakeholders. The task opens in the side panel in the context of the Board that it belongs to, eliminating the need to search through multiple items on the Board. Real-time collaboration in Docs
    -   Edit a Doc page concurrently with multiple other editors. Colored cursors denote the current location of editors on the page. You can choose to show or hide these indicators. UI changes Numbering on automation cards
    -   Instead of record numbers, Board automation cards show a sequential list numbering of 1, 2, 3, and so on. Error messages use these list numbers so you can easily identify an existing automation from the list of available automations for the Board. Changed in this release: Improved user experience for Board views
    -   Avoid accidentally losing your Board view edits with the help of a workspace prompt that indicates you have unsaved changes. This prompt is displayed when you try to navigate away from the Board or refresh the browser tab. Improved user experience for copying links of Boards
    -   Improve collaboration by ensuring that your team sees the same data as you while sharing links of your Boards through a Copy link action. The linked workspace shows the view in which the Board is displayed to you regardless of the user's view settings. Redirection to the CWM task from notification emails Access task details directly when you open a task from an assignment email from CWM. The task opens in a new browser tab in the context of its Board, eliminating the need to search for the assigned task through multiple Spaces and Boards. Redirection to the specific doc pages from notification emails Access the specific Doc page that you are @-mentioned in by selecting View Doc in the notification email, eliminating the need to look through multiple pages in the Doc.
-   **Version 4.0.7 - December 2024**

    Minor bug fixes and improvements.

-   **Version 4.0.1 - November 2024**
    -   New:
        -   Templates for Boards and Docs
            -   Apply templates to ensure consistent formats
            -   Save and manage templates in the Template Center
            -   Share templates or keep them private
        -   Board Views
            -   Save display preferences as personal or shared views
            -   Create multiple views to fit different audiences
            -   Switch between views quickly
        -   Export Board to CSV/Excel Export task data to CSV or Excel for analysis and reporting \(Note: Hierarchy of tasks is not retained in exports.\)
        -   Export Docs to PDF : export Doc pages as PDF for easy sharing
    -   Changed:
        -   Add new item
            -   Press "Enter" to create subsequent tasks in List view without clicking "Add new item"
            -   Press "ESC" to end the task creation flow
-   **Version 3.1.1 - September 2024**

    Minor improvements and bug fixes.

-   **Version 3.0.3 - August 2024**
    -   New:
        -   Track and manage all your assigned work from a single view called My Work.
        -   Create automations on the Assigned to column or other custom columns ofPeopletype.
        -   Personalize Boards using 3 new columns \(Assignment group, Assigned to, Created by\). These are hidden on the Board by default.
        -   Save time and avoid manual copying of information with the ability to duplicate CWM Boards and Docs
        -   @-mentioning a user in Docs triggers an email to the user
    -   Changed:
        -   Improvements to sharing Spaces: While sharing a space with other collaborators,you can now search users and groups by email along with their names. This feature helps you choose the right collaborator in cases where individual users or groups have the same name
        -   Activation information:Install Collaborative Work Management by requesting it from the ServiceNow Store
        -   Performance improvements
-   **Version 2.0.6 - June 2024**
    -   Fixed:
        -   Error when adding new task
        -   Bug when updating gantt bar timelines
-   **Version 2.0.4 - May 2024**
    -   Fixed: Bug fixes and general improvements
    -   New:
        -   Boost efficiency by creating automations to reduce manual task updates and alert team members when changes are made to tasks or important dates arrive.
        -   Improved UI/UX &amp; performance of Docs
        -   Notifications when a user is mentioned in a Doc
        -   New "reference" type custom column which enables the ability to reference any record in ServiceNow
        -   Selection of multiple labels when using the "label" type custom column
-   **Version 2.0.3 - May 2024**
    -   Collaborative Work Management is a central hub for team members to plan, manage, visualize and collaborate on work.
    -   Use personal spaces to plan your own work or shared spaces to collaborate on work with team members. Within spaces, create boards to manage tasks for your teams. Create custom columns and custom work types to be able to manage any type of work. View tasks in List, Gantt, or Kanban to support flexible types of workflow. Autonomously configure columns, work types, and access to your spaces without support from a system administrator.
    -   Boost efficiency by creating automations to reduce manual task updates and alert team members when changes are made to tasks or important dates arrive.
    -   Create docs to manage documentation or content for your work. See who is online and collaborate in real time to create docs.
    -   Connect boards to Strategic Planning Workspace for prioritization, roadmap, and goals.

**Parent Topic:**[ServiceNow Store - Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itbm-highlight.md)

