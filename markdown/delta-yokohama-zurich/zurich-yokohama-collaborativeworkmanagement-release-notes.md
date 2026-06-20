---
title: Combined Collaborative Work Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Collaborative Work Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-collaborativeworkmanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined Collaborative Work Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Collaborative Work Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Collaborative Work Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Collaborative Work Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Collaborative Work Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Keyboard shortcuts for workspace actions](https://servicenow-staging.fluidtopics.net/access?context=cwm-spaces&family=yokohama&ft:locale=en-US)**

Use the keyboard shortcut to quickly search for and go to a Space, Board, or Doc.

    -   Mac OS: Option + F
    -   Windows OS: Alt + F
Also, the Search bar displays all the recent Spaces, Boards, and Docs that you've navigated to within the CWM workspace so that you can quickly select from the recent items without having to search for them again.

-   **[Real-time collaboration in Docs](https://servicenow-staging.fluidtopics.net/access?context=cwm-docs&family=yokohama&ft:locale=en-US)**

Edit a Doc page concurrently with multiple other editors. Colored cursors denote the current location of editors on the page. You can choose to show or hide these indicators.

**Note:** To use the full functionality of Docs when using Docs v6.0.0 within CWM workspace, ensure that you upgrade Collaborative Work Management to v5.0.0. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).

-   **[Requesting access to a Space or Board from its URL](https://servicenow-staging.fluidtopics.net/access?context=cwm-spaces&family=yokohama&ft:locale=en-US)**
    -   CWM users can quickly request access to a Space or Board through the **Request access** button, which sends an actionable email request to Space owners and editors.
    -   Space owners can approve or reject the request directly from the email without having to open the CWM workspace.
-   **[Requesting to elevate user access role to Editor](https://servicenow-staging.fluidtopics.net/access?context=share-space-in-cwm&family=yokohama&ft:locale=en-US)**

Easily send a request to Space owners and editors to request elevating your role to Editor by selecting the Viewing mode indicator in the Board header that indicates that you have only the Viewer role.

-   **[Managing access in the Share permissions modal](https://servicenow-staging.fluidtopics.net/access?context=share-space-in-cwm&family=yokohama&ft:locale=en-US)**

Easily identify users who already have access to your Space and the users who requested access using the following two sections in the Share permissions modal.

    -   **People with Access** section: Manage the access level of existing collaborators to Editor, Viewer, or Owner, or remove them from the Space.
    -   **Pending Access** section: Review requests from users and choose to grant or deny them access to your Space.
-   **[Managing Space permissions for task assignees and other users](https://servicenow-staging.fluidtopics.net/access?context=share-space-in-cwm&family=yokohama&ft:locale=en-US)**

Identify task assignees who don’t have access to the workspace through a lock icon next to the user name. This icon is visible in the List view of the Board in the columns of type People such as **Assigned to**, **Additional Assignee**, and **Assignment group**.

You can either use the workspace prompt to grant assignees Viewer access or choose to manage their access level later from the Share permissions modal.

-   **[Share task details with Task URLs](https://servicenow-staging.fluidtopics.net/access?context=add-tasks-to-board-in-cwm&family=yokohama&ft:locale=en-US)**

Provide direct access to a specific CWM Task record to share with team members and stakeholders by copying its URL. The task opens in the side panel in the context of the Board that it belongs to, eliminating the need to search through multiple items on the Board.

-   **[Improved user experience for Board views](https://servicenow-staging.fluidtopics.net/access?context=update-a-cwm-board-view&family=yokohama&ft:locale=en-US)**

Avoid accidentally losing unsaved Board view edits when you try to navigate away from the Board or refresh the browser tab by responding to a displayed workspace prompt.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Enterprise Agile Planning \(EAP\) integration with CWM](https://servicenow-staging.fluidtopics.net/access?context=integrate-eap-with-collaborative-work-management&family=zurich&ft:locale=en-US)**

Enhance visibility and streamline planning for your teams with EAP integration into CWM.

For Agile teams managing non-agile work items like incidents and change tasks, this integration bridges the gap by automatically creating a dedicated Space and Board in CWM. Agile work is seamlessly brought over via Connected Work, while EAP sprints are reflected directly in CWM’s Sprint planning view, thus enabling unified planning across all work types. Teams can plan work for their sprints and update work status directly from the CWM Board, with performance reports in EAP dynamically reflecting these changes. This integration enables teams to manage their full scope of work from a single, connected workspace.

-   **[Board preferences](https://servicenow-staging.fluidtopics.net/access?context=cwm-boards&family=zurich&ft:locale=en-US)**

Reduce cognitive load and focus on the most relevant and actionable tasks by filtering work items on CWM boards based on their last updated date and hiding those items marked as Closed complete. From the Board preferences menu on the Board header, you can choose to show items last updated within 7 days, 30 days, 90 days, 120 days, or 1 year.

-   **[Kanban card layout settings](https://servicenow-staging.fluidtopics.net/access?context=cwm-board-views&family=zurich&ft:locale=en-US)**

Surface the information that's most relevant to you using Card Layout settings for Kanban view of a CWM Board. You can now personalize Kanban cards by selecting up to five fields to display on them. For a cleaner, distraction-free view, you can enable the Compact layout, which shows only the work item name on the card. Alternatively, the Full view shows all selected fields, offering better context directly on the card. Based on your workflow needs, tailor your workspace to enhance the way you track tasks.

-   **[Dynamic data linking in CWM Docs](https://servicenow-staging.fluidtopics.net/access?context=cwm-docs&family=zurich&ft:locale=en-US)**

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Agile sprint planning in CWM](https://servicenow-staging.fluidtopics.net/access?context=agile-sprint-planning-in-cwm&family=zurich&ft:locale=en-US)**

Plan, track, and manage work for your teams by using Agile sprint planning in the CWM workspace. You can use CWM to manage tasks in multiple methodologies including ad hoc, waterfall, and Agile practices.

    -   View such details as the backlog, current sprint, and future sprints at a glance from the Sprint planning view of the CWM Board.
    -   Add Agile item types, such as stories, with other CWM tasks to the backlog.
    -   Create sprints with a custom duration and sprint capacity.
-   **[Connect work](https://servicenow-staging.fluidtopics.net/access?context=unified-boards-for-connected-work-in-cwm&family=zurich&ft:locale=en-US)**

Streamline team collaboration and planning by enabling your teams to view and plan all their work in one place by connecting work across multiple ServiceNow applications. By defining the type of work you want to connect to CWM, you can bring in records from other applications into CWM Boards.

After the records are added to a CWM Board, your teams can update their status and other details from within CWM, or perform sprint planning for all the work on the Board. This unified experience improves efficiency because your teams don't have to switch between multiple workspaces.

-   **[Navigation panel enhancements](https://servicenow-staging.fluidtopics.net/access?context=cwm-spaces&family=zurich&ft:locale=en-US)**

Move Spaces, Boards, and Docs around in the navigation panel of the workspace by using the drag and drop functionality.

-   **[Enhancements to Kanban view](https://servicenow-staging.fluidtopics.net/access?context=cwm-board-views&family=zurich&ft:locale=en-US)**
    -   Quick filters: Filter the tasks based on the work type that you would like to see in the Kanban view of a CWM Board. You can select single or multiple work item types based on the swim lanes selected. Any filters that you apply to the Kanban view are specific to this view and aren't applied to List or Gantt views.
    -   Horizontal lanes: Group the cards on the Kanban view by using a vertical and horizontal lane for improved visibility into the type and progress of work. You can save horizontal lane preference into Board views and templates.
-   **[Copying and pasting content within Docs](https://servicenow-staging.fluidtopics.net/access?context=cwm-docs&family=zurich&ft:locale=en-US)**

Copy and paste the content such as text, images, lists, and tables from one Doc page to another. The following content is supported for the copy and paste action:

    -   Text blocks with existing formatting
    -   Bulleted and numbered lists
    -   Tables
    -   Images
    -   Single and multiple paragraph blocks into a table cell
    -   Lists into a table cell
    -   Images into a table cell
-   **[New keyboard shortcuts](https://servicenow-staging.fluidtopics.net/access?context=cwm-spaces&family=zurich&ft:locale=en-US)**
    -   Create Space:
        -   macOS: Option + S
        -   Windows OS: Alt + S
    -   Create Board:
        -   macOS: Option + B
        -   Windows OS: Alt + B
    -   Create Doc:
        -   macOS: Option + D
        -   Windows OS: Alt + D
-   **[Keyboard shortcut enhancements within CWM Docs](https://servicenow-staging.fluidtopics.net/access?context=cwm-docs&family=zurich&ft:locale=en-US)**
    -   Insert a URL in the Doc:
        -   macOS: Cmd + K
        -   Windows OS: Ctrl + K
    -   Insert a new row in a table after the last row: Enter
    -   Move to adjacent cells within a table: Arrow keys
    -   Create a new list item within an existing list in a table or paragraph: Enter
    -   Create a new line in the same bullet point: Shift + Enter
    -   Indent a list item: Tab

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Collaborative Work Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Improved user experience for adding hyperlinks in Docs](https://servicenow-staging.fluidtopics.net/access?context=cwm-docs&family=yokohama&ft:locale=en-US)**

Insert hyperlinks in a Doc easily and quickly through the formatting toolbar, inline commands, or by pasting a copied link. The pasted URL can be converted into a hyperlink by pressing the Space or Enter key and edited using the inline edit modal.

-   **[Improved user experience for copying links of Boards](https://servicenow-staging.fluidtopics.net/access?context=board-views-in-cwm&family=yokohama&ft:locale=en-US)**

Ensure that your team sees the same data as you while sharing links of your Boards through the **Copy link** action, which now accesses the linked workspace showing the view in which the Board is displayed to you regardless of the user's view settings.

-   **[Redirection to the CWM task from notification emails](https://servicenow-staging.fluidtopics.net/access?context=cwm-boards&family=yokohama&ft:locale=en-US)**

Access task details when you open a task from an assignment email from CWM in a new browser tab in the context of its Board rather than being directed to the workspace home page.

-   **[Redirection to the specific doc pages from notification emails](https://servicenow-staging.fluidtopics.net/access?context=cwm-docs&family=yokohama&ft:locale=en-US)**

Access the specific Doc page that you are @-mentioned in by selecting **View Doc** in the notification email, eliminating the need to look through multiple pages in the Doc.

-   **[Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=yokohama&ft:locale=en-US)**

The CWM workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Zurich

</td><td>

-   **[My Work enhancements](https://servicenow-staging.fluidtopics.net/access?context=my-work-in-cwm&family=zurich&ft:locale=en-US)**

Track all your work from one place using the enhanced My Work in CWM. My Work now supports all ServiceNow task records-such as incidents, changes, and requests-whether they originate in CWM or outside, giving you a unified view of everything assigned to you. This helps you stay on top of overdue or open tasks and improves on-time delivery.

Additionally, the Item type filter has been refined to show all CWM tasks \(including custom ones\) grouped under a single category, instead of listing every CWM task type individually. You’ll also only see task types in the filter that you’re actually assigned to, reducing clutter and making it easier to filter what matters.

-   **[Enhancements to tables in Docs](https://servicenow-staging.fluidtopics.net/access?context=cwm-docs&family=zurich&ft:locale=en-US)**
    -   Resize the column width of a table per your preference.
    -   Add color to single or multiple table cells.
    -   Select multiple cells of a table using the mouse device or by pressing **Shift+ one of the arrow keys** on the keyboard.
    -   Delete content from multiple cells using the **Backspace** or **Delete** keys.
    -   Copy and paste cell content:
        -   Copy content from one cell and paste it to multiple cells.
        -   Copy content from n number of cells and paste it to another set of n number of cells.
        -   Copy content from multiple cells and paste it as a new table in an empty block on the page.
-   **[Enhancements to CWM Board templates](https://servicenow-staging.fluidtopics.net/access?context=templates-in-cwm-for-spaces-boards-and-docs&family=zurich&ft:locale=en-US)**
    -   Save template: While saving a Board as a template, choose between saving the current view or all shared views. You can see the number of Board views and custom task types that are included in this template.

These details are displayed in the Template Center, where you can select a template that best meets your team's needs.

    -   Apply template: While applying a Board template, you can see the number of Board views and custom task types that you get if you apply this template. The Board views drop-down list lets you switch between views and provides information on the type of views that are enabled in this template.

Only those custom columns that are part of these views are brought over when you apply this template.

-   **[Collaborate with Spaces](https://servicenow-staging.fluidtopics.net/access?context=cwm-spaces&family=zurich&ft:locale=en-US)**

When a user is added to the **Assigned to** field of a CWM task but doesn't yet have access to the Space, the email notification requesting access is sent only to the Space owners. This way, there's less email clutter for all the Space users because notifications are sent to only those users who need to know this information.

-   **[New columns for CWM tasks](https://servicenow-staging.fluidtopics.net/access?context=agile-sprint-planning-in-cwm&family=zurich&ft:locale=en-US)**

Every task within a CWM Board has new columns called Sprint and Story points. You can use these columns if you choose to plan any task into Sprints. These columns are available on every type of work item, including the items that are brought into the Board through Connected work.

-   **[Changes within CWM Docs](https://servicenow-staging.fluidtopics.net/access?context=cwm-docs&family=zurich&ft:locale=en-US)**
    -   Open the keyboard shortcut panel:
        -   macOS: Cmd + Option + K
        -   Windows OS: Ctrl + Alt + K
    -   Images can be resized after inserting them within a table cell.
    -   The page name can be updated by editing the name and clicking anywhere on the Doc.
    -   Moving content blocks to within a numbered list or deleting a list item from a list automatically adjusts the list numbering.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Collaborative Work Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Collaborative Work Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Collaborative Work Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Collaborative Work Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Collaborative Work Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Collaborative Work Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Collaborative Work Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Collaborative Work Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The CWM Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.

See [Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for details.


</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Collaborative Work Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Collaborative Work Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Improve focus on your working area through a simplified, distraction-free navigation experience.
-   Quickly identify task assignees without access to your Space and manage sharing permissions accordingly.
-   Improve collaboration efficiency by sharing the exact view of your Board or specific page of your Doc when sharing a URL with others.
-   Collaborate in real-time on Docs with multiple editors.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Collaborative Work Management](https://servicenow-staging.fluidtopics.net/access?context=cwm-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Plan, track, and manage team work in Agile methodology with sprint planning in the CWM workspace.
-   Streamline task management for teams by integrating various work items across ServiceNow applications into CWM Boards.
-   Filter and group work by vertical and horizontal swimlanes in the Kanban view for a specific work item type.

 See [Collaborative Work Management](https://servicenow-staging.fluidtopics.net/access?context=cwm-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

