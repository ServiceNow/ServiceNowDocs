---
title: Playbook page templates
description: Use playbook page templates to create pages and page variants for use in CSM Configurable Workspace. These pages and page variants provide agents with either horizontal or vertical playbooks that they can use to complete tasks and resolve cases.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Playbook page templates

Use playbook page templates to create pages and page variants for use in CSM Configurable Workspace. These pages and page variants provide agents with either horizontal or vertical playbooks that they can use to complete tasks and resolve cases.

The following page templates are available with the Playbooks for Customer Service Management application \[com.sn\_csm\_playbook\]. For more information, see [Playbook plugins](setting-up-csm-playbooks.md#section_qgq_ylk_llb).

|Page template|Description|
|-------------|-----------|
|[Case playbook: horizontal stages](csm-playbook-templates.md#section_uyk_sp3_cxb)|Includes a horizontal stage picker that displays across the top of the UI and shows persistent information in the left panel.|
|[Case playbook: vertical stages](csm-playbook-templates.md#section_ert_1vw_cxb)|Includes a vertical stage picker that displays in the left panel. This stage picker can track overall progress on the UI in a vertical view.|

Considerations for using these page templates include the number of stages that appear in the picker and the length of the stage names. For example, longer stage names in the horizontal playbook can be truncated.

**Note:** By default, the playbook page templates are not active. To activate a page template, see [Activate a playbook page or page variant](../task/activate-process-based-page.md).

## Case playbook: horizontal stages page template

The Case playbook: horizontal stages page template includes a horizontal stage picker across the top of the page and an activity picker on the left side. For details about the components included in this template, see [Playbook template components](csm-playbook-templates.md#section_sjc_xxz_rbc).

![Case playbook: horizontal stages page template with a stage picker that displays across the top of the user interface](../image/case-playbook-template-horizontal-stages.png "Case playbook: horizontal stages page template")

## Case playbook: vertical stages page template

The Case playbook: vertical stages page template includes a vertical stage picker on the left side of the page. For details about the components included in this template, see [Playbook template components](csm-playbook-templates.md#section_sjc_xxz_rbc).

![Case playbook: vertical stages page template with a stage picker that displays on the side of the user interface](../image/case-playbook-template-vertical-stages.png "Case playbook: vertical stages page template")

## Playbook page template components

The playbook page templates include modular components that enable you to quickly build playbook pages in [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

<table id="table_rvn_hs3_1xb"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page header

</td><td>

The page header includes record information that is displayed in the primary and secondary fields:-   The primary field displays the short description of the record.
-   The secondary fields display the additional record information such as the priority, state, and contact or consumer details.

You can configure the fields that appear in the page header. For more information, see [Customize the page header for a playbook page](../task/customize-process-form-header.md).

</td></tr><tr><td>

Action bar

</td><td>

The action bar contains the actions that are available to users while working on case records. The available actions are determined by factors such as the user role, case state, and other attributes.-   **Record Details**: Displays the record details.
-   **Playbook Details**: Displays the playbook details.
-   **In-progress actions**: Provides a list of minimized [modeless dialogs](csm-playbook-modeless-dialog.md) and includes a badge that displays the number of items in the list. From this list, an agent can select an item to open the minimized comment, work note, or email.
-   **Create**: Create records such as requests, incidents, and work orders.
-   **Compose**: Compose comments, work notes, and emails in modeless dialogs.
-   **Save**: Save changes to the case record.
-   **More Actions**: Perform additional actions such as proposing a major case or reporting a knowledge gap.

You can configure the actions that are included in the action bar. For more information, see [Customize UI actions for a playbook page](../task/customize-process-ui-actions-bar.md).

</td></tr><tr><td>

Playbook name

</td><td>

In the Case playbook: horizontal stages template, the playbook name appears in the form header above the horizontal stage picker.In the Case playbook: vertical stages template, the playbook name appears at the top of the vertical stage picker.

</td></tr><tr><td>

Stage picker

</td><td>

The playbook templates include either a horizontal or vertical stage picker, which gives the agent a complete view of the playbook and where they are within the playbook.-   The horizontal stage picker displays the playbook stages across the top of the record page below the page header. Select a stage to see the activities in the activity picker.
-   The vertical stage picker displays the playbook stages and activities on the side of the record page. Select a stage to expand the stage and display the included activities.

The stages in the stage picker include icons that indicate the stage status:

-   A check mark ![Check mark image.](../../../reuse/icons/product-icons/circle-check-outline-24.svg) indicates that the stage is complete.
-   A pen icon ![Pen image.](../image/icon-pencil-ac.png) indicates the current stage.
-   A lock icon ![Lock image.](../image/lock-icon.png) indicates that a stage is locked and can’t be started until the previous stage is complete.

</td></tr><tr><td>

Activity picker

</td><td>

The activity picker displays the activities for the current stage. Each activity has an indicator that shows the activity state:-   Completed
-   In progress
-   Remaining

With the horizontal stage picker, you can expand or collapse the list of activities for the current stage.

With the vertical stage picker, you can expand each stage to see the activities within that stage.

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

Contact or consumer lookup

</td><td>

The lookup component enables agents to look up contact or consumer information and display that information in a record card. These cards display customer information and provide quick access to details such name, email, and phone. The contact record card also includes account information.Agents can use the lookup component to do the following:

-   Search for a contact or consumer.
-   Link or unlink a contact or consumer record.
-   Edit and save the information in a linked contact or consumer record.
-   Select a reference field on a record card, such as a contact or consumer name, to open the reference in a sub-tab.
-   Select an email address on a lookup card to open a draft email in the email composer in a sub-tab.
-   Select a phone number on a lookup card to make a call.

For more information, see [Playbook lookup component](csm-playbook-lookup-component.md).

</td></tr><tr><td>

Case summarization

</td><td>

The case summarization component appears below the lookup component. When an agent opens a case record, the component is collapsed and in the default state.Agents can use this component to do the following:

-   Summarize case details.
-   Post the summary to the activity stream.
-   Refresh the summary.

The case summarization component requires the Now Assist for Customer Service Management \(CSM\) application to be activated and configured. For more information, see [Playbook case summarization component](csm-playbook-case-summary-component.md).

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

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Case playbook: horizontal stages page includes the following tabs.-   [Activity Stream](csm-playbook-activity-stream-component.md)
-   Agent Assist
-   Search
-   [Related Items](csm-playbook-related-items-component.md)
-   Attachments
-   Response Templates
-   [Email Templates](https://www.servicenow.com/docs/access?context=configure-email-templates&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)
-   Templates
-   Record Information

For more information about the tabs in the contextual side panel, see [Playbook contextual side panel component](csm-playbook-side-panel-component.md).

</td></tr><tr><td>

Activity stream

</td><td>

The activity stream component displays a list of activities occurring on a case record. This list can be collapsed to provide a quick view of case activities or expanded to provide more detail about individual activities.For more information, see [Playbook activity stream component](csm-playbook-activity-stream-component.md).

**Note:** The Case playbook: horizontal stages page uses [modeless dialogs](csm-playbook-modeless-dialog.md) for composing comments, work notes, and emails.

</td></tr><tr><td>

Compose email and Compose comments modeless dialogs

</td><td>

A modeless dialog is a window that overlays the main window content. You can use modeless dialogs to create and post comments and work notes to the activity stream and to compose and send emails as you work through the stages and activities in a playbook. For more information, see [Playbook modeless dialogs](csm-playbook-modeless-dialog.md).

</td></tr></tbody>
</table>## Using multiple form controllers

The multiple form controller feature enables page authors to add multiple form components to UI Builder templates. This feature is available with the following playbook page templates:

-   Case playbook: horizontal stages
-   Case playbook: vertical stages

With this feature, page authors can:

-   Integrate inline tabs with forms that utilize dedicated form controller instances, eliminating the need for page collections and enhancing UI Builder usability and runtime performance.
-   Enhance record pages with custom component bundles that include a form controller.
-   Incorporate modals containing forms into record pages, facilitating the transmission of notifications and form updates back to the main page.

For more information about using multiple form controllers, see [Add forms to UI Builder pages](https://www.servicenow.com/docs/access?context=add-forms-to-ui-builder-pages&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

