---
title: Page components
description: Page components are the modular building blocks of a playbook record page, including the stage picker, activity picker, activity viewer, and contextual side panel that agents use to work through a case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-playbook-templates.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Workspace, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Page components

Page components are the modular building blocks of a playbook record page, including the stage picker, activity picker, activity viewer, and contextual side panel that agents use to work through a case.

Playbook page templates include modular components that make up the playbook record pages and enable administrators to build playbook pages in [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md). The following components are available on the playbook workspace page.

<table id="table_rvn_hs3_1xb"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page header

</td><td>

The page header includes record information that is displayed in the primary and secondary fields:-   The primary field displays the short description of the record.
-   The secondary fields display the additional record information such as the priority, state, and contact or consumer details.

You can configure the fields that appear in the page header. For more information, see [Customize the page header for a playbook page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customize-process-form-header.md).

</td></tr><tr><td>

Action bar

</td><td>

The action bar contains the actions that are available to users while working on case records. The available actions are determined by factors such as the user role, case state, and other attributes.-   **Record Details**: Displays the record details.
-   **Playbook Details**: Displays the playbook details.
-   **In-progress actions**: Provides a list of minimized [modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-modeless-dialog.md) and includes a badge that displays the number of items in the list. From this list, an agent can select an item to open the minimized comment, work note, or email.
-   **Create**: Create records such as requests, incidents, and work orders.
-   **Compose**: Compose comments, work notes, and emails in modeless dialogs.
-   **Save**: Save changes to the case record.
-   **More Actions**: Perform additional actions such as proposing a major case or reporting a knowledge gap.

You can configure the actions that are included in the action bar. For more information, see [Customize UI actions for a playbook page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customize-process-ui-actions-bar.md).

</td></tr><tr><td>

Playbook name

</td><td>

In the Case playbook: horizontal stages template, the playbook name appears in the form header above the horizontal stage picker.In the Case playbook: vertical stages template, the playbook name appears at the top of the vertical stage picker.

</td></tr><tr><td>

Playbook picker

</td><td>

A playbook picker can be used to select a playbook in the user interface. A playbook picker is available if there are multiple playbooks on a record.

</td></tr><tr><td>

Stage picker

</td><td>

A stage picker displays the stages in a playbook and gives the user a complete view of the playbook and where they are within it. A stage picker can be oriented horizontally or vertically. The horizontal stage picker displays the playbook stages across the top of the record page below the page header. The vertical stage picker displays the playbook stages and activities on the side of the record page. The stages include icons that indicate the stage status:-   A check mark \[Omitted image "circle-check-outline-24.svg"\] Alt text: Check mark image. indicates that the stage is complete.
-   A pen icon \[Omitted image "icon-pencil-ac.png"\] Alt text: Pen image. indicates the current stage.
-   A lock icon \[Omitted image "lock-icon.png"\] Alt text: Lock image. indicates that a stage is locked and can’t be started until the previous stage is complete.

</td></tr><tr><td>

Activity picker

</td><td>

The activity picker displays the activities for the current stage. Each activity has an indicator that shows the activity state:-   Complete \(\[Omitted image "icon-circle-green-check.png"\] Alt text: circle icon with green check mark symbol\)
-   In Progress \(\[Omitted image "icon-circle-filled--purple-pencil.png"\] Alt text: purple filled circle icon with white pencil symbol\)
-   Pending \(\[Omitted image "icon-circle-purple-lock.png"\] Alt text: circle icon with purple lock symbol\)
-   Skipped

The list of activities for the current stage can be expanded or collapsed. Selecting an activity displays its details in the activity viewer.

Selecting an activity displays the details in the activity viewer.

</td></tr><tr><td>

Activity viewer

</td><td>

The activity viewer displays the selected activity. This is the main work area where an agent performs the work necessary to complete the current activity.

</td></tr><tr><td>

Activity cards

</td><td>

Activity cards display the details about the current activity in the activity viewer. Depending on the type of activity, the activity cards can display information such as form data, task status, SLA timers, or attachments.Agents use the cards to complete the work for each activity, such as filling in forms, completing checklists, completing tasks, or adding attachments.

</td></tr><tr><td>

Contact/consumer lookup

</td><td>

The lookup component enables agents to look up contact or consumer information and display that information in a record card. These cards display customer information and provide quick access to details such name, email, and phone. The contact record card also includes account information.Agents can use the lookup component to do the following:

-   Search for a contact or consumer.
-   Link or unlink a contact or consumer record.
-   Edit and save the information in a linked contact or consumer record.
-   Select a reference field on a record card, such as a contact or consumer name, to open the reference in a sub-tab.
-   Select an email address on a lookup card to open a draft email in the email composer in a sub-tab.
-   Select a phone number on a lookup card to make a call.

For more information, see [Playbook lookup component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-lookup-component.md).

</td></tr><tr><td>

Case summarization

</td><td>

The case summarization component appears below the lookup component. When an agent opens a case record, the component is collapsed and in the default state.Agents can use this component to do the following:

-   Summarize case details.
-   Post the summary to the activity stream.
-   Refresh the summary.

The case summarization component requires the Now Assist for Customer Service Management \(CSM\) application to be activated and configured. For more information, see [Playbook case summarization component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-case-summary-component.md).

</td></tr><tr><td>

Record details

</td><td>

The case details component includes collapsible sections for:-   Case
-   Notes
-   Closure Information
-   Related Records

This component also includes a menu with additional form actions, such as personalizing the form, exporting data, and copying the URL.

Agents can view case details by selecting the **Record Details** button in the action bar.

</td></tr><tr><td>

Contextual side panel

</td><td>

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Case playbook: horizontal stages page includes the following tabs.-   [Activity Stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-activity-stream-component.md)
-   Agent Assist
-   Search
-   [Related Items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-related-items-component.md)
-   Attachments
-   Response Templates
-   [Email Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-email-templates.md)
-   Templates
-   Record Information

For more information about the tabs in the contextual side panel, see [Playbook contextual side panel component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-side-panel-component.md).

</td></tr><tr><td>

Activity stream

</td><td>

The activity stream component displays a list of activities occurring on a case record. This list can be collapsed to provide a quick view of case activities or expanded to provide more detail about individual activities.For more information, see [Playbook activity stream component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-activity-stream-component.md).

**Note:** The Case playbook: horizontal stages page uses [modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-modeless-dialog.md) for composing comments, work notes, and emails.

</td></tr><tr><td>

Related items

</td><td>

The related items component provides access to record-related lists in an expandable format. Each list shows item cards and supports actions such as Create, View all, and Show more. For more information, see [Playbook related items component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-related-items-component.md).

</td></tr><tr><td>

Compose email and Compose comments modeless dialogs

</td><td>

A modeless dialog is a window that overlays the main window content. You can use modeless dialogs to create and post comments and work notes to the activity stream and to compose and send emails as you work through the stages and activities in a playbook. For more information, see [Playbook modeless dialogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-modeless-dialog.md).

</td></tr></tbody>
</table>The components shown above come with the playbook page templates by default. They are a starting point, not a fixed layout. Using UI Builder, administrators can remove components, rearrange them, add custom ones, or create a different page layout for a specific use case or persona.

For the full set of customization tasks — including activating page variants, configuring the page header, customizing UI actions, adjusting the left panel, and configuring contextual side panel tabs — see [Configure templates and pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-pages.md).

## Using multiple form controllers

The multiple form controller feature enables page authors to add multiple form components to UI Builder templates. This feature is available with the following playbook page templates:

-   Case playbook: horizontal stages
-   Case playbook: vertical stages

With this feature, page authors can:

-   Integrate inline tabs with forms that use dedicated form controller instances, eliminating the need for page collections and enhancing UI Builder usability and runtime performance.
-   Enhance record pages with custom component bundles that include a form controller.
-   Incorporate modals containing forms into record pages, facilitating the transmission of notifications and form updates back to the main page.

For more information about using multiple form controllers, see [Add forms to UI Builder pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/add-forms-to-ui-builder-pages.md).

