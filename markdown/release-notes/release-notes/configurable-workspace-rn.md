---
title: Configurable Workspace release notes
description: The ServiceNow Configurable Workspace application provides tools to agents, case managers, help desk professionals, and managers for answering customer questions and resolving customer problems. Configurable Workspace was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Configurable Workspace release notes

The ServiceNow® Configurable Workspace application provides tools to agents, case managers, help desk professionals, and managers for answering customer questions and resolving customer problems. Configurable Workspace was enhanced and updated in the Australia release.

## Configurable Workspace highlights for the Australia release

-   Add a background color to fields including unsaved fields and fields with highlighted values.
-   Apply commands with keyboard shortcuts for journal fields.
-   Set conditions and use the email composer within form templates.
-   Edit or delete Activity stream posts, and add knowledge base links from recommended actions.
-   Implement declarative actions without assuming page ownership, and override attributes without altering the base action.

See [Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) for more information.

## New in the Australia release

-   **[UI interactions for declarative actions](https://www.servicenow.com/docs/access?context=configure-da-ui-interactions&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Combine logic, script, and configurable UI with a UI interaction, and apply it from any page event or declarative action. When you use a declarative action to apply a UI interaction, you can extend a page without taking ownership.


## UI changes

-   **Session tabs**

    The following UI changes have been made to session tabs:

    -   The icon to close a tab displays on hover only.
    -   Overflow text on a tab is blurred instead of displaying an ellipsis.
    -   Overflow tabs are displayed as a **More** tab with a split button.
-   **Lists for mobile devices**

    List design and behavior adapt to mobile devices to help improve usability.

-   **Forms**

    The following UI changes have been made to forms:

    -   Annotation fields provide rich text markup to enhance contextual form information.
    -   The HTML editor toolbar displays a modern design.
-   **Form templates**

    The following UI changes have been made to form templates:

    -   The button to add a form template field has been updated to be more discoverable.
    -   View selected conditions as a card below a field.
-   **Activity stream**

    The following UI changes have been made to the Activity stream:

    -   Filter Activity stream posts by user.
    -   The Activity stream features a responsive design for stacking content, typography styles, and spacing.
    -   System tokens for Activity stream components provide a consistent look and feel without needing to manually update style properties for every component.
-   **Email composer**

    The following UI changes have been made to the email composer:

    -   All email layouts display a minimized recipient field and borderless rich text editor.
    -   A message displays in the header when an email is saved as a draft.
    -   Copy and apply text formatting for emails using the format painter.

## Changed in this release

-   **Record List component bundle enhancements in UI Builder**

    Configure these enhancements to the Record List component bundle in UI Builder:

    -   Pin columns to keep them visible while scrolling horizontally.
    -   Change the medium default size for highlighted values.
    -   View list data as a data visualization.
    -   Show a filter overview in the list header for a summary of the filters currently applied to the list.
    -   Catalog variables and questions are supported as list columns.
    -   Open lists in multiple session tabs from the list menu.
    -   Customize gallery list card layouts including images, icons, text placement, and sizing.
-   **[AI filter assist](https://www.servicenow.com/docs/access?context=use-ai-filter-assist&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Convert everyday language into an encoded query with AI filter assist.

-   **[Track record list changes](https://www.servicenow.com/docs/access?context=use-ai-list-tracker&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Get an AI-generated summary of recent changes made to a list without manually reviewing each record.

-   **[Grouping for related lists](https://www.servicenow.com/docs/access?context=configure-related-list-grouping&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Configure related lists to persist selections for the Group by filter.

-   **[Predicate Builder component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/now-predicate-builder/uib-setup):**

    Configure these enhancements to the Predicate Builder component in UI Builder:

    -   Customize condition rows.
    -   Configure a simple filtering mechanism.
    -   Use a search term for filtering panel definitions.
    -   Configure fixed queries.
-   **[Hierarchical queries](https://www.servicenow.com/docs/access?context=data-hierarchies&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    Configure a record hierarchy to create filter queries that traverse levels of hierarchy.

-   **[Dynamic queries](https://www.servicenow.com/docs/access?context=working-with-dynamic-schema&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    Configure dynamic attributes and dynamic categories to create filter queries that use the dynamic schema field type.

-   **[Form component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/form%20record%20page/uib-setup):**

    Configure these enhancements to the Form component in UI Builder:

    -   Wrap field labels on mobile devices.
    -   Display an indicator dot on unsaved fields.
    -   Add a background color to unsaved fields to make them more noticeable.
    -   Add an address field to forms that searches, validates, and automatically fills an address.
-   **[AI indicator](https://www.servicenow.com/docs/access?context=c_FormFields&version=australia&pubname=australia-platform-user-interface&section=ai-indicator&ft:locale=en-US)**

    The AI indicator is a visual cue that identifies form fields in configurable workspace and Core UI that have been updated with AI-generated content, providing a consistent and clear indication of AI involvement across the platform.

-   **[Unsaved field indicator](https://www.servicenow.com/docs/access?context=configure-unsaved-field-indicator&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Configure the unsaved field indicator for your entire workspace experience instead of individual pages.

-   **[Background color for unsaved fields](https://www.servicenow.com/docs/access?context=configure-background-color-unsaved-indicator&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Configure a background color to display on unsaved fields for your entire workspace experience instead of individual pages.

-   **[Background color for highlighted values](https://www.servicenow.com/docs/access?context=configure-background-color-highlighted-values&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Configure a background color for fields with highlighted values.

-   **[Text commands for journal fields](https://www.servicenow.com/docs/access?context=configure-journal-fields-keyboard-shortcuts&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Configure text commands that can be applied by keyboard shortcuts within journal fields.

-   **[HTML editor toolbar](https://www.servicenow.com/docs/access?context=configure-html-editor-toolbar&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Configure toolbar options for the HTML editor within journal input fields.

-   **[Inline validation for string fields](https://www.servicenow.com/docs/access?context=format-regex-pattern-string-fields&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Configure inline validation for string fields that formats inputs automatically, persists guidance text as a placeholder, and restricts unsupported characters.

-   **[Watch lists](https://www.servicenow.com/docs/access?context=configure-watch-list&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Add and remove yourself and multiple records from a watch list.

-   **[Form Templates component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/now-record-common-templates-connected/uib-setup)**

    Configure these enhancements to the Form Templates component in UI Builder:

    -   Preview form templates before applying them to the record page.
    -   Display an alert message and confirm reuse when a selected form template is already applied to that record.
-   **[Activity Stream component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/now-activity-stream-connected/uib-setup)**

    Configure these enhancements to the Activity Stream component in UI Builder:

    -   Edit and delete Activity stream posts after submitting.
    -   Add knowledge base links from recommended actions to Activity stream posts.
-   **[Keyboard shortcuts for emails](https://www.servicenow.com/docs/access?context=add-response-templates-shortcut&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Use keyboard shortcuts to open drafts, email templates, and response templates.

-   **[Attachments component enhancements in UI Builder](https://developer.servicenow.com/dev.do#!/reference/next-experience/australia/now-components/now-record-common-attachments-connected/uib-setup)**

    Configure these enhancements to the Attachments component in UI Builder:

    -   Open the file viewer as a modeless dialog.
    -   Customize the attachment header, upload instructions, and menu actions in both the full and compact modes.
    -   Display the loading skeleton as a spinner or as three cards.
    -   Enable a visible drop zone for file uploads in the compact mode.
-   **[Form action layout groups for declarative actions](https://www.servicenow.com/docs/access?context=configure-da-layout-group&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Upgrade form action layout groups to customize the order, label, and icons for declarative actions without altering the base action.

-   **[Declarative actions and UI actions on public pages](https://www.servicenow.com/docs/access?context=using-web-embeddables&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

    Non-logged in users may access specified declarative actions and UI actions on embedded web pages while maintaining integrity with security guidance and access control list permissions.


## Activation information

Configurable Workspace is a ServiceNow AI Platform feature that is active by default.

## Plugin information

-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release:

    Agent Workspace - Ribbon \(com.snc.agent\_workspace.ribbon\): Planned for deprecation in the C release. Beginning with the Australia release this plugin will be migrated to a store application. Upgrade your instance to Australia or later release versions and the store applications will be automatically installed.


## Browser requirements

Configurable Workspace doesn’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge, Chromium or one of the other supported browsers that are listed in [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Accessibility information

-   **[Screen Summarization](https://www.servicenow.com/docs/access?context=use-screen-summarization&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

    Screen Summarization is a feature that supports visually impaired and low-vision users by providing AI-generated summaries of workspace pages and their sections. The summaries can be read aloud with a screen reader to help reduce navigation and comprehension time.

    Install Screen Summarization by requesting it from the ServiceNow® Store. Visit the [ServiceNow® Store](https://store.servicenow.com/store) to view all the available apps and information about submitting requests to the store.


## Related ServiceNow applications and features

-   **[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Use UI Builder to build your Configurable Workspace experience.


**Parent Topic:**[ServiceNow AI Platform user interface release notes](now-platform-ui-rn-landing.md)

