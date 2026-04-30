---
title: Case playbook: horizontal stages record page
description: The Case playbook: horizontal stages page is a record page that you can use in CSM Configurable Workspace. This page includes a playbook with a horizontal stage picker that displays across the top of the user interface and persistent information in the left panel.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Playbook pages, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Case playbook: horizontal stages record page

The Case playbook: horizontal stages page is a record page that you can use in CSM Configurable Workspace. This page includes a playbook with a horizontal stage picker that displays across the top of the user interface and persistent information in the left panel.

The Case playbook: horizontal stages record page is created from the [Case playbook: horizontal stages template](csm-playbook-templates.md#section_uyk_sp3_cxb).

The Case playbook: horizontal stages record page is available with the Playbooks for Customer Service Management v6.0 store application. For more information, see [Playbook plugins](setting-up-csm-playbooks.md#section_qgq_ylk_llb).

## Case playbook: horizontal stages page variant

The Case playbook: horizontal stages page variant is included with the Playbooks for Customer Service Management v6.0 store application. This variant includes the following settings.

<table id="table_f5m_bhx_qbc"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

The Case playbook: horizontal stages page variant is not active by default. Enabling the **Active** check box makes the page variant available to the selected audience.The **Active** setting combined with the page order determines the page that CSM Configurable Workspace uses to display record information. For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

</td></tr><tr><td>

Order

</td><td>

Each record page has an order which indicates the page priority. The lower the number, the higher the priority.The default order for the Case playbook: horizontal stages page variant is -1.

</td></tr><tr><td>

Conditions

</td><td>

Conditions determine when a page variant is displayed. The Case playbook: horizontal stages page variant has the following condition: **table=sn\_customerservice\_case**This condition limits the use of the Case playbook: horizontal stages page variant to records from the Case \[sn\_customerservice\_case\] table and tables that extend the Case table.

</td></tr><tr><td>

Audience

</td><td>

The audience determines who can see the page variant. The Case playbook: horizontal stages page variant does not have an audience. This means everyone with access to the experience can see this page variant.For more information, see [Learn about audiences](https://www.servicenow.com/docs/access?context=add-audiences&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr></tbody>
</table>To access the settings for this page variant:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  In the Record section of the Pages and variants list, select **Case playbook: horizontal stages**.
4.  Select **Settings** at the top of the page.

## Case playbook: horizontal stages page components

The Case playbook: horizontal stages page includes the following components.

<table id="table_pk2_g1w_q1c"><thead><tr><th>

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

Record tags

</td><td>

Agents can create multiple tags for a record and then use the tags to group and organize records.For more information, see [Group and find records using tags in workspace](https://www.servicenow.com/docs/access?context=setting-record-tags-agent-workspace&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Action bar

</td><td>

The action bar contains the actions available to users while working on case records. The specific actions are determined by factors such as the user role, case state, and other attributes.-   **Record details**: Displays the record details.
-   **Playbook details**: Displays the playbook details.
-   **In-progress Actions**: Provides a list of minimized [modeless dialogs](csm-playbook-modeless-dialog.md) and includes a badge that displays the number of items in the list. From this list, an agent can select an item to open the minimized comment, work note, or email.
-   **Create**: Create records such as work orders, incidents, and requests.
-   **Compose**: Compose comments, work notes, and emails in modeless dialogs.
-   **Save**: Save changes to the case record.
-   **More Actions**: Perform additional actions such as proposing a major case or reporting a knowledge gap.

You can configure the actions that are included in the action bar. For more information, see [Customize UI actions for a playbook page](../task/customize-process-ui-actions-bar.md).

</td></tr><tr><td>

Playbook name

</td><td>

In the Case playbook: horizontal stages page variant, the playbook name appears in the form header above the horizontal stage picker.

</td></tr><tr><td>

Stage picker

</td><td>

The Case playbook: horizontal stages page variant includes a horizontal stage picker, which gives the agent a complete view of the playbook and where they are within the playbook.The horizontal stage picker displays the playbook stages across the top of the record page below the page header. Select a stage to see the activities in the activity picker.

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

Selecting an activity in a stage displays the details in the activity viewer.

</td></tr><tr><td>

Activity viewer

</td><td>

The activity viewer displays the selected activity. This is the main work area where an agent performs the work necessary to complete the current activity.Activity cards display the details about the current activity in the activity viewer. Depending on the type of activity, the activity cards can display information such as form data, task status, SLA timers, or attachments.

Agents use the cards to complete the work for each activity, such as filling in forms, completing checklists, completing tasks, or adding attachments.

</td></tr><tr><td>

Contact or consumer lookup

</td><td>

The lookup component enables agents to look up contact or consumer information and display that information in a record card. These cards display customer information and provide quick access to details such name, email, and phone. The contact record card also includes account information.Agents can use the contact lookup component to do the following:

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
-   Recommended Actions
-   [Related Items](csm-playbook-related-items-component.md)
-   Attachments
-   Response Templates
-   [Email Templates](https://www.servicenow.com/docs/access?context=configure-email-templates&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)
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
</table>