---
title: Collaborative Work Management release notes
description: The ServiceNow Collaborative Work Management \(CWM\) application provides a central hub to plan, visualize, and collaborate on work with team members across your organization. CWM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# Collaborative Work Management release notes

The ServiceNow® Collaborative Work Management \(CWM\) application provides a central hub to plan, visualize, and collaborate on work with team members across your organization. CWM was enhanced and updated in the Yokohama release.

## Collaborative Work Management highlights for the Yokohama release

-   Improve focus on your working area through a simplified, distraction-free navigation experience.
-   Quickly identify task assignees without access to your Space and manage sharing permissions accordingly.
-   Improve collaboration efficiency by sharing the exact view of your Board or specific page of your Doc when sharing a URL with others.
-   Collaborate in real-time on Docs with multiple editors.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Collaborative Work Management](https://www.servicenow.com/docs/access?context=cwm-landing&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

**Important:** Collaborative Work Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Keyboard shortcuts for workspace actions](https://www.servicenow.com/docs/access?context=cwm-spaces&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Use the keyboard shortcut to quickly search for and go to a Space, Board, or Doc.

    -   Mac OS: Option + F
    -   Windows OS: Alt + F
    Also, the Search bar displays all the recent Spaces, Boards, and Docs that you've navigated to within the CWM workspace so that you can quickly select from the recent items without having to search for them again.

-   **[Real-time collaboration in Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Edit a Doc page concurrently with multiple other editors. Colored cursors denote the current location of editors on the page. You can choose to show or hide these indicators.

    **Note:** To use the full functionality of Docs when using Docs v6.0.0 within CWM workspace, ensure that you upgrade Collaborative Work Management to v5.0.0. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).

-   **[Requesting access to a Space or Board from its URL](https://www.servicenow.com/docs/access?context=cwm-spaces&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   CWM users can quickly request access to a Space or Board through the **Request access** button, which sends an actionable email request to Space owners and editors.
    -   Space owners can approve or reject the request directly from the email without having to open the CWM workspace.
-   **[Requesting to elevate user access role to Editor](https://www.servicenow.com/docs/access?context=share-space-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Easily send a request to Space owners and editors to request elevating your role to Editor by selecting the Viewing mode indicator in the Board header that indicates that you have only the Viewer role.

-   **[Managing access in the Share permissions modal](https://www.servicenow.com/docs/access?context=share-space-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Easily identify users who already have access to your Space and the users who requested access using the following two sections in the Share permissions modal.

    -   **People with Access** section: Manage the access level of existing collaborators to Editor, Viewer, or Owner, or remove them from the Space.
    -   **Pending Access** section: Review requests from users and choose to grant or deny them access to your Space.
-   **[Managing Space permissions for task assignees and other users](https://www.servicenow.com/docs/access?context=share-space-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Identify task assignees who don’t have access to the workspace through a lock icon next to the user name. This icon is visible in the List view of the Board in the columns of type People such as **Assigned to**, **Additional Assignee**, and **Assignment group**.

    You can either use the workspace prompt to grant assignees Viewer access or choose to manage their access level later from the Share permissions modal.

-   **[Share task details with Task URLs](https://www.servicenow.com/docs/access?context=add-tasks-to-board-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Provide direct access to a specific CWM Task record to share with team members and stakeholders by copying its URL. The task opens in the side panel in the context of the Board that it belongs to, eliminating the need to search through multiple items on the Board.

-   **[Improved user experience for Board views](https://www.servicenow.com/docs/access?context=update-a-cwm-board-view&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Avoid accidentally losing unsaved Board view edits when you try to navigate away from the Board or refresh the browser tab by responding to a displayed workspace prompt.


## UI changes

-   **[Improved navigation in the workspace](https://www.servicenow.com/docs/access?context=cwm-spaces&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    The improved navigation panel provides a simpler and cleaner user interface. At a given time, the navigation panel shows the contents of just one Space to provide a distraction-free experience while you work.

    Use the Spaces menu to choose a different Space or use the Search option to quickly find and open any Space, Board or Doc.

    Additionally, you can also choose to resize the navigation panel or collapse it altogether to increase the working area for your Boards or Docs.

-   **[Verify content through browser spell checks](https://www.servicenow.com/docs/access?context=cwm-docs&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Identify and manage incorrect spellings in typed or pasted content in a Doc. The incorrect spellings are highlighted automatically, and you can correct them using the right-click menu options on the highlighted word.

-   **[Numbering on automation cards](https://www.servicenow.com/docs/access?context=manage-or-delete-automations-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Instead of record numbers, Board automation cards show a sequential list numbering of 1, 2, 3, and so on. Error messages use these list numbers so you can easily identify an existing automation from the list of available automations for the Board.


## Changed in this release

-   **[Improved user experience for adding hyperlinks in Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Insert hyperlinks in a Doc easily and quickly through the formatting toolbar, inline commands, or by pasting a copied link. The pasted URL can be converted into a hyperlink by pressing the Space or Enter key and edited using the inline edit modal.

-   **[Improved user experience for copying links of Boards](https://www.servicenow.com/docs/access?context=board-views-in-cwm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Ensure that your team sees the same data as you while sharing links of your Boards through the **Copy link** action, which now accesses the linked workspace showing the view in which the Board is displayed to you regardless of the user's view settings.

-   **[Redirection to the CWM task from notification emails](https://www.servicenow.com/docs/access?context=cwm-boards&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Access task details when you open a task from an assignment email from CWM in a new browser tab in the context of its Board rather than being directed to the workspace home page.

-   **[Redirection to the specific doc pages from notification emails](https://www.servicenow.com/docs/access?context=cwm-docs&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Access the specific Doc page that you are @-mentioned in by selecting **View Doc** in the notification email, eliminating the need to look through multiple pages in the Doc.

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    The CWM workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


## Activation information

Install Collaborative Work Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

    The CWM Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.

    See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for details.


## Related ServiceNow applications and features

-   **[Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Now Assist for CWM application uses generative AI skills to save time and improve efficiency for the actions you perform within the CWM workspace.

-   **[Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Prioritize, roadmap, and track work when using traditional, Agile, or hybrid methodologies with ServiceNow® Strategic Planning. Align strategy to execution by defining and tracking goals across your organization. Strategic Planning is available with an SPM Professional license.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

