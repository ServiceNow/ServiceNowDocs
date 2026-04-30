---
title: Configurable Workspace release notes
description: The ServiceNow Configurable Workspace application provides tools to agents, case managers, help desk professionals, and managers for answering customer questions and resolving customer problems. Configurable Workspace was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [Workspace, Workspace UI]
---

# Configurable Workspace release notes

The ServiceNow® Configurable Workspace application provides tools to agents, case managers, help desk professionals, and managers for answering customer questions and resolving customer problems. Configurable Workspace was enhanced and updated in the Zurich release.

## Configurable Workspace highlights for the Zurich release

-   See who is active within a form with live presence and user avatars that display a contact card.
-   Use the Record List component bundle to create lists for all list types and the Predicate Builder component to create conditional statements.
-   Create emails, work notes, and comments while working on other tasks with a pop-out, modeless dialog in the Compose editor.
-   Rename and reorder the **Emails**, **Work notes**, and **Comments** tabs in the Compose editor.
-   Send emails with a digital signature that verifies you as an authentic sender and an email encryption that certifies authentic recipients.

See [Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

## New in the Zurich release

-   **Activity stream compose with modeless dialog component bundle**

    Open the Compose editor as a pop-out, modeless dialog to draft comments, work notes, and emails while working on other tasks.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **Lists**

    The following UI changes have been made to lists:

    -   Change list header organization for responsive experiences.
    -   Access the filter from the list header.
    -   Use HTML fields in lists that are scrollable and display formatted text.
-   **Forms**

    The following UI changes have been made to forms:

    -   Live presence displays who is viewing the form. Access a user's contact card by selecting their avatar.
    -   Currency fields display a menu with a search field and currency descriptions.
-   **Activity stream**

    The following UI changes have been made to the Activity stream:

    -   The Compose header is hidden when you're not using the stacked view.
    -   Text area inputs are displayed as a single line.
    -   Text area and rich text editor resize automatically.
    -   The line height was set to display the scrollbar.
    -   In the Activity stream, a post indicates when field changes were made by an AI agent instead of a human agent. When the AI agent updates the fields, the post also displays a message that field changes were made by Now Assist.
    -   Translate emails in the Activity stream to your system language using the translate button.
-   **Email composer**

    Email recipient pills display whether the user is online. Select an email recipient pill to view the user's contact card.

-   **Attachments panel**

    The following UI changes have been made to the Attachments panel:

    -   Preview files, change file names, select an encryption module, and remove files individually with a preview modal for attachments. After you select attachments to upload, the modal displays the selected files in a list view. For mobile experiences, the preview modal displays as a carousel with thumbnails.
    -   Delete selected attachments from the Attachments panel by using the More Actions menu.

## Changed in this release

-   **[Browser warning for unsaved changes](https://www.servicenow.com/docs/access?context=config-browser-warning-unsaved-changes&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Configure a browser warning to alert you of unsaved changes when you navigate away from a page using the back or forward buttons.

-   **[Record List component bundle enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/record%20list/overview)**

    Configure these enhancements to the Record List component bundle in UI Builder:

    -   Select **Related** list as a list type option.
    -   Switch between the standard view and gallery list, which displays list items as cards.
-   **[Export lists to Google Sheets](https://www.servicenow.com/docs/access?context=exporting-lists-google-spreadsheets&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Export your lists to Google Sheets directly from the Export menu.

-   **[Live updates for lists](https://www.servicenow.com/docs/access?context=live-list-updates-configurable-workspace&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Configure live updates at the list page level without affecting other lists in your Configurable Workspace.

-   **[AI filter assist](https://www.servicenow.com/docs/access?context=use-ai-filter-assist&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Convert everyday language into an encoded query with AI filter assist.

-   **[Predicate Builder component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-predicate-builder/uib-setup)**

    Configure these enhancements to the Predicate Builder component in UI Builder:

    -   Use the Predicate Builder for all list types.
    -   Set up a read-only version of the Predicate Builder to display all conditions without users editing them.
-   **[Form component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/form%20record%20page/uib-setup)**

    Configure these enhancements to the Form component in UI Builder:

    -   Display Boolean fields as a toggle.
    -   Add an indicator that marks unsaved fields after any changes.
    -   Wrap field labels instead of truncating them.
    -   Change field-level configurations from field context menus displayed as a gear icon beside every field label.
    -   Choose whether related lists load with the form, after the form, or on demand.
    -   Hide the related list header when the last record is removed.
    -   Choose to display field labels beside its value or stacked vertically.
    -   Suppress special handling notes and notifications from secondary forms on a page.
-   **[Personalize Form menu](https://www.servicenow.com/docs/access?context=hide-personalize-form-menu&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Customize which fields display on a form with the Personalize Form menu \(![image.icon-personalize-form]\) in the form header. Use system properties to hide the Personalize Form menu or change the roles with access to the menu.

-   **[Format string fields with guidance text and inline validation](https://www.servicenow.com/docs/access?context=format-regex-pattern-string-fields&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Set up guidance text to display in string fields with format requirements such as account ID, SSN, or SIN. Use regular expression inline validation to display an error message if input values are incorrect.

-   **[Advanced view rules configuration](https://www.servicenow.com/docs/access?context=configure-advanced-view-rules-forms&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Use client scripts to set up view rules configurations.

-   **[Activity Stream Compose component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-activity-stream-compose-connected/uib-setup)**

    Configure these enhancements to the Activity Stream Compose component in UI Builder:

    -   Hide the rich text editor toggle for your workspace without affecting other experiences.
    -   Rename and reorder Emails, Work notes, and Comments tabs.
    -   Annotate new activities to make it easier for you to find unread emails and messages.
-   **[@mentions for the email composer](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/shared-components/now-email-client-composer-connected/overview)**

    Configure @mentions in UI Builder for the Email composer and Email composer \(mini\) components, enabling you to add an email recipient by using an @mention in the email body.

-   **[Digital signature and encryption in the email composer](https://www.servicenow.com/docs/access?context=config-email-digital-signature-encryption&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Send emails with a digital signature that verifies you as an authentic sender and an email encryption that certifies authentic recipients.

-   **[Custom attachment layout](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-record-common-attachments-connected/uib-setup)**

    Configure a custom layout mode for the Attachments component in UI Builder. Customize the maximum file size, file types, multiple file uploads, and preview modal.

-   **[Adding the Now Assist icon to action buttons](https://www.servicenow.com/docs/access?context=create-da-buttons-now-assist-icon&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Use declarative actions to create buttons with the Now Assist \(![](../../common/image/icon-ai-sparkle.png)\) icon and hover animation.


## Removed in this release

-   The List, List - Simple, and List - Related components are no longer available in UI Builder are replaced by the Record List component bundle.
-   The Condition Builder component is no longer available in UI Builder and is replaced by the Predicate Builder component for all list types.

## Activation information

Configurable Workspace is a ServiceNow AI Platform feature that is active by default.

## Browser requirements

Configurable Workspace doesn’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge, Chromium or one of the other supported browsers that are listed in [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Accessibility information

-   **[Screen Summarization](https://www.servicenow.com/docs/access?context=use-screen-summarization&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Screen Summarization is a feature that supports visually impaired and low-vision users by providing AI-generated summaries of workspace pages and their sections. The summaries can be read aloud with a screen reader to help reduce navigation and comprehension time.

    Install Screen Summarization by requesting it from the ServiceNow® Store. Visit the [ServiceNow® Store](https://store.servicenow.com/store) to view all the available apps and information about submitting requests to the store.


## Related ServiceNow applications and features

-   **[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use UI Builder to build your Configurable Workspace experience.


**Parent Topic:**[ServiceNow AI Platform user interface release notes](now-platform-ui-rn-landing.md)

