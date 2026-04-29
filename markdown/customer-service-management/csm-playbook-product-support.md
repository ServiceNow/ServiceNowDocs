---
title: Case Playbook for Product Support
description: Use the Case Playbook for Product Support to guide agents through the steps that are needed to resolve product issues.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Playbook applications, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Case Playbook for Product Support

Use the Case Playbook for Product Support to guide agents through the steps that are needed to resolve product issues.

A product support case captures the information about the customer, the product, and the reported issue. The product support playbook provides the activities and tasks that agents can perform to research and resolve the issue. Agents can also create and assign tasks as needed and use the playbook to communicate with the customer.

The Case Playbook for Product Support is available for both CSM Configurable Workspace and CSM Agent Workspace. In the CSM Workspaces, the playbook appears in the **Playbook** tab on the case record.

**Note:** If you have the admin role, you can configure a playbook to use the compact mode in CSM Configurable Workspace. Use the compact mode to move the playbook from a tab in the Workspace to a tab in the contextual side panel.

## Case Playbook for Product Support application

The Case Playbook for Product Support 3.0 application \(com.sn\_csm\_product\_caseflow\) is available from the ServiceNow® Store. For more information, see [Playbook plugins](setting-up-csm-playbooks.md#section_qgq_ylk_llb).

## Case Playbook for Product Support PAD process definition

The Case Playbook for Product Support 3.0 includes a new Process Automation Designer \(PAD\) process definition called **product\_playbook\_v1**. This process definition contains the optimized stages and activities for the product support playbook.

The process definitions are stored in the Process Definitions table \(sys\_pd\_process\_definition\). To view a list of processes, you can do the following task:

1.  In the application navigator, enter **sys\_pd\_process\_definition.list**.
2.  [Configure the list](https://www.servicenow.com/docs/access?context=c_PersonalLists&version=australia&pubname=australia-platform-user-interface&section=t_PersonalizeAList&ft:locale=en-US) to show the **Name** field.

Only one PAD process per playbook can be active at a time.

## Case Playbook for Product Support features

The Case Playbook for Product Support 3.0 includes the case features and enhancements that are listed in the following table.

<table id="table_csx_knc_bqb"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Focused activity view

</td><td>

Feature that determines how the stages and activities appear in the playbook.

 The Case Playbook for Product Support uses the [Focused activity view](csm-playbook-layout.md#section_oq5_3yw_5pb), which enables agents to see

-   The end-to-end life cycle of the product support workflow in the playbook life-cycle panel.
-   The current stage is expanded and the current activity is highlighted within the playbook life-cycle panel.
-   Details of the current activity that is displayed in the playbook work area.

</td></tr><tr><td>

Contextual side panel

</td><td>

Feature that displays the following information in the contextual side panel:

-   Activity stream
-   Ribbon information, such as the case overview, customer details, timeline, and SLAs
-   Dynamic related records

**Note:** The activity stream and ribbon information are available in CSM Configurable Workspace only.

 For more information about using the contextual side panel, see

-   [Using activity stream in the contextual side panel](csm-playbooks-using-activity-stream.md)
-   [Viewing the ribbon information in the contextual side panel](csm-playbooks-viewing-ribbon-info.md)
-   [Viewing dynamic related records in the contextual side panel](csm-playbooks-viewing-rel-records.md)

 For more information about configuring this feature, see [Configure playbook stage and activity visibility](../task/playbook-config-activity-visibility.md).

</td></tr><tr><td>

Activity visibility

</td><td>

Feature that uses the following settings to control the activity visibility:

-   Hide the activities in a stage that the logged-in user can't access.
-   Hide the pending activities in a stage.

</td></tr><tr><td>

Compact mode

</td><td>

Mode that moves the playbook from a tab in the Workspace to the contextual side panel. Agents can complete the playbook activities in the side panel while they’re viewing the other tabs in the record page. **Note:** This mode is available in CSM Configurable Workspace only.

 Users with the admin role can configure a playbook to use the compact mode in the playbook component configuration in UI Builder.

</td></tr><tr><td>

Dynamic related records

</td><td>

Feature that displays the records in the contextual side panel. These records dynamically change based on the context of the current record or playbook activity.

 From the **Related Records** tab in the contextual side panel, agents can

-   Filter the list of related records
-   Open the list in a new tab
-   Create new records

**Note:** The dynamic related records feature is available in CSM Configurable Workspace only.

 For more information, see [Viewing related records in the contextual side panel](csm-playbooks-viewing-rel-records.md).

</td></tr><tr><td>

SLA widget

</td><td>

Activity cards in the playbook work area can display an SLA widget. The widget appears on the activity card when the playbook activity has an SLA.

 The color of the widget indicates the time remaining for the SLA:

-   Green: 0–50%
-   Yellow: 50–75%
-   Orange: 75–99%
-   Red: 100% or breached

</td></tr></tbody>
</table>## Using the playbook stage and activity pickers to navigate stages and activities

The playbook stage picker enables agents to see the entire product support workflow. Agents can navigate the playbook stages and activities by doing the following tasks:

-   Expand and collapse the stages to show or hide activities.
-   Use the filter in the stage picker to filter activities by the assigned user or the activity state.
-   Select an activity to display the details in the playbook work area.

The following example shows the different stages and activities in a playbook. ![Focused view of the various stages and activities in the product case playbook lifecycle, along with the case details.](../image/playbook-product-support.png)

## Using the Playbook Actions menu

The Playbook Actions menu in the playbook header includes the actions that agents can perform at the playbook level. The agents can select the Playbook Actions icon \(![Playbook actions menu icon.](../image/playbook-ellipses.png)\) to access this menu.

The Playbook Actions menu includes the following playbook-level actions:

-   **Expand All Stages**: Expands all the stages in the playbook.
-   **Collapse All Stages**: Collapses all the stages in the playbook.
-   **Request Info**: Displays a pop-up window that the agent can use to communicate with the customer. This action also saves the details to the case activity stream. By using this action, the state of the case changes to Awaiting Info and pauses the SLAs and any timers on the case.
-   **Info Received**: Returns the case to the previous state and restarts the SLAs and any timers on the case.

The activity-level actions can also appear in the Playbook Actions menu. These actions vary depending on the type of activity and in which stage it appears. For example, actions are available to accept cases, create related cases, create case tasks, and propose solutions.

## Case Playbook for Product Support stages and activities

The following table lists the Case Playbook for Product Support stages and activities that agents can use to resolve customer issues.

<table id="table_nrj_z2s_llb"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Details

</th></tr></thead><tbody><tr><td>

**Investigate** Guides the agent in collecting customer information and performing some initial research about the product issue.

</td><td>

Review case details

</td><td>

A case is in the Investigate stage when the case state is New or Open.

 This activity displays information about the case, including the customer and product details and any contracts or entitlements.

 The agent can add details about the issue and review the information and related search results, such as knowledge articles or similar cases.

 Agent actions:

-   **Assign to me**: Assigns the case to the current agent.
-   **Accept**: Enables the agent to accept the case.
-   **Save**: Saves any changes made to the case details.
-   **Mark Complete**: Saves the information, marks the activity as complete, and moves to the next activity or stage.

</td></tr><tr><td>

**Work in progress** Create case tasks as needed and assign tasks to users.

</td><td>

Create case tasks

</td><td>

A case is in the Work in progress stage when the agent completes the initial research and begins working on the issue.

 This activity includes a list of case tasks. Agents can create tasks as needed to complete the work for a case.

 Agent actions:

-   **Add New**: Creates a case task. Add information to the task and select **Save** to add the task to the Case Tasks list.
-   **Mark Complete**: Marks the activity as complete and moves to the next activity or stage.

</td></tr><tr><td>

**Resolve and close** Case tasks are complete and the agent is ready to propose a solution to the customer.

</td><td>

Resolve

</td><td>

Add details to the **Resolution code** and **Resolution notes** fields on the activity card and select **Save**. This information is added to the case record. Agent actions:

-   **Propose Solution**: Notifies the customer of the proposed solution.
-   **Change Solution**: Appears after the agent proposes a solution. Use this action to add information to the case resolution fields.

</td></tr><tr><td>

 

</td><td>

Close case

</td><td>

This activity shows the following read-only fields:-   **Closed by**: the agent who closed the case.
-   **Closed**: the date and time that the case was closed.

 The system closes the case when the customer accepts the resolution or when the agent selects **Close Case**.

</td></tr></tbody>
</table>## Process-based page variant for cases

The Case Playbook for Product Support v5.0 application includes a process-based page variant that you can activate and use with cases in CSM Configurable Workspace. This page includes the following features:

-   A horizontal stage picker at the top of the record that provides an end-to-end view of the complaint process. Activities within each stage are stacked in the activity viewer.
-   Displays the related list tabs in the Dynamic Related Records component in the contextual side panel.
-   Displays persistent account and contact information in the left side panel.
-   Displays **Email** tab in the **Activity Stream**.
-   Displays the email templates in the contextual side panel.
-   Supports case summarization card on the left panel.

Agents can create tasks as needed as well as view and update case details. For more information, see [Playbook pages](csm-playbook-pages.md).

