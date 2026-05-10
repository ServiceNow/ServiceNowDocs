---
title: Case Playbook for Complaints
description: Use the Case Playbook for Complaints to guide agents through the steps that are needed to resolve customer complaints.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Playbook applications, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Case Playbook for Complaints

Use the Case Playbook for Complaints to guide agents through the steps that are needed to resolve customer complaints.

A complaint case captures the information about the customer, the product, and the details about the complaint. The complaint playbook provides the activities and tasks that agents can perform to research and resolve the complaint. Agents can also create and assign tasks as needed and use the playbook to communicate with the customer.

The Case Playbook for Complaints can be used with cases that are created using the complaint case type. This playbook is available for both CSM Configurable Workspace and CSM Agent Workspace. In the CSM Workspaces, the playbook appears in the **Playbook** tab on the case record.

**Note:** If you have the admin role, you can configure a playbook to use the compact mode in CSM Configurable Workspace. Use the compact mode to move the playbook from a tab in the Workspace to a tab in the contextual side panel.

## Case Playbook for Complaints application

The Case Playbook for Complaints 3.0 application \(com.sn\_csm\_complaint\_caseflow\) is available from the ServiceNow® Store. For more information, see [Playbook plugins](setting-up-csm-playbooks.md#section_qgq_ylk_llb).

## Case Playbook for Complaints PAD process definition

The Case Playbook for Complaints 3.0 includes a new Process Automation Designer \(PAD\) process definition called **complaint\_playbook\_v1**. This process definition contains the optimized stages and activities for the complaint playbook.

The process definitions are stored in the Process Definitions table \(sys\_pd\_process\_definition\). To view a list of processes, do the following task:

1.  In the application navigator, enter **sys\_pd\_process\_definition.list** in the application navigator.
2.  [Configure the list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_PersonalLists.md) to show the **Name** field.

Only one PAD process per playbook can be active at a time. .

## Case Playbook for Complaints features

The Case Playbook for Complaints 3.0 includes the case features and enhancements that are listed in the following table.

<table id="table_csx_knc_bqb"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create a complaint case using the Case Playbook for Complaints

</td><td>

Feature that opens the complaint playbook and initiates the first activity in the Intake stage, which is gathering complaint details. The agent can complete and save this activity to create the record.

 For more information, see [Create a record using a playbook](../task/csm-playbook-create-record.md).

</td></tr><tr><td>

Focused activity view

</td><td>

Feature that determines how the stages and activities appear in the playbook.

 The Case Playbook for Complaints uses the [Focused activity view](csm-playbook-layout.md#section_oq5_3yw_5pb), which enables agents to see

-   The end-to-end life cycle of the complaint workflow in the playbook life-cycle panel.
-   The current stage is expanded and the current activity is highlighted within the playbook life-cycle panel.
-   The details of the current activity that is displayed in the playbook work area.

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

</td></tr><tr><td>

Activity visibility

</td><td>

Feature that uses the following settings to control activity visibility:

-   Hide the activities in a stage that the logged-in user can't access.
-   Hide the pending activities in a stage.

 For more information about configuring this feature, see [Configure playbook stage and activity visibility](../task/playbook-config-activity-visibility.md).

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
-   Create records

**Note:** The dynamic related records feature is available in CSM Configurable Workspace only.

 For more information, see [Viewing related records in the contextual side panel](csm-playbooks-viewing-rel-records.md).

</td></tr><tr><td>

SLA widget

</td><td>

Activity cards in the playbook work area that can display an SLA widget. The widget appears on the activity card when the playbook activity has an SLA. This widget includes the activities in the following stages:

-   Triage
-   Research
-   Respond

 The color of the widget indicates the time remaining for the SLA:

-   Green: 0–50%
-   Yellow: 50–75%
-   Orange: 75–99%
-   Red: 100% or breached

</td></tr></tbody>
</table>## Using the playbook stage and activity pickers to navigate stages and activities

The playbook stage picker enables agents to see the entire complaint workflow. Agents can navigate the playbook stages and activities by doing the following tasks:

-   Expand and collapse stages to show or hide activities.
-   Use the filter in the stage picker to filter activities by the assigned user or the activity state.
-   Select an activity to display the details in the activity viewer.

## Using the Playbook Actions menu

The Playbook Actions menu in the playbook header includes the actions that agents can perform at the playbook and activity levels. The agents can select the Playbook Actions icon \(![Playbook actions menu icon.](../image/playbook-ellipses.png)\) to access this menu.

The Playbook Actions menu includes the following playbook-level actions:

-   **Expand All Stages**: Expands all the stages in the playbook.
-   **Collapse All Stages**: Collapses all the stages in the playbook.
-   **Request Info**: Displays a pop-up window that the agent can use to communicate with the customer and to request information about a case or case task. This action also saves the details to the case or case task activity stream. By using this action, the state of the case or case task changes to Awaiting Info and pauses the SLAs and any timers.
-   **Info Received**: Returns the case or case task to the previous state and restarts the SLAs and any timers.

**Note:** The **Request Info** and **Info Received** actions can also be configured to appear on case task activity cards.

The activity-level actions can vary depending on the type of activity and in which stage it appears. For example, actions are available to accept cases, create related cases, create case tasks, and propose solutions.

## Complaint playbook stages and activities

The following table lists the Case Playbook for Complaints stages and activities that agents can use to resolve customer issues.

<table id="table_nrj_z2s_llb"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

**Intake** Guides the agent to collect the information needed to create the complaint case.

</td><td>

Gather complaint details

</td><td>

When an agent creates a complaint case, the workspace opens the Create New Complaint Case form, launches the complaint playbook, and uses the first activity to gather complaint details.

 The agent can enter the information about the customer, the service, the complaint, and the expected outcome for the case. As the agent enters the complaint details, additional fields appear on the activity card such as the **Category** and **Subcategory** fields.

**Note:** For more information about the service, see [Service definitions](csm-service-definitions.md).

 Agent actions:

 **Continue**: Creates the complaint case and adds the case number to the **Record** tab. It also marks the first activity as complete and moves to the second activity.

</td></tr><tr><td>

 

</td><td>

Add involved parties

</td><td>

Activity that the agent can use to add involved parties to the complaint case:

1.  Select **Add new** to open the Create New Related Party form in a new tab.
2.  In the **Type** field, select the related party with the correct entity type, such as a co-complainant who is a customer contact.
3.  Select **User**.
4.  Select **Save** to add the user to the Involved Parties list on the activity card.

 Agent actions:

-   **Assign to me**: Available if the case isn’t yet assigned. Assigns the case to the logged-in user.
-   **Add new**: Adds a user to the Involved Parties list \(see the previous steps\).

</td></tr><tr><td>

 

</td><td>

Verify primary address

</td><td>

Activity that shows the fields from the Primary Correspondence Address form section on the **Details** tab. Agents can accept this address or select a different address. Agent actions:

-   **Save**: Saves the updates to the Primary Correspondence Address fields.
-   **Move to triage**: Completes the Intake stage, marks the activities in the stage as complete, and moves to the next stage in the complaint playbook.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

Activity that displays the details of the email that was automatically sent to the customer at the completion of the Intake stage.

</td></tr><tr><td>

**Triage** Enables the agent to do the initial troubleshooting on the case.

</td><td>

Verify complaint

</td><td>

Case task that agents can use to review any available related search results in the contextual side panel and add notes or attachments.

 Agent actions:

-   **Request info**: Requests additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Submit for review**: Marks the case task and the Triage stage as complete.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

Activity that displays the details of the email that was automatically sent to the customer at the completion of the Triage stage.

</td></tr><tr><td>

**Research** Orchestrates sending the case to different back-office teams for follow-up.

</td><td>

Review legal implications

</td><td>

Case task that agents can assign to a different user for legal review.

 To assign the task:

1.  Select the View Task icon in the activity card. This action opens the case task in a new tab.
2.  Select the user in the **Assigned to** field.
3.  Add information to the other fields on the Case Task form as needed and select **Save**.

 Agent actions:

-   **Request info**: Requests additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Review complete**: Marks the case task as complete.

</td></tr><tr><td>

 

</td><td>

Product owner review for other similar issues

</td><td>

Case task that an agent can assign to a different user for a review of similar issues.

 To assign the task:

1.  Select the View Task icon ![View task.](../image/pop-out-icon.png) in the activity card to open the case task in a new tab.
2.  Select the user in the **Assigned to** field.
3.  Add information to the other fields on the Case Task form as needed and click **Save**.

 Agent actions:

-   **Request info**: Requests additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Review complete**: Marks the case task as complete.

</td></tr><tr><td>

 

</td><td>

Verify check entitlement

</td><td>

Case task that an agent can assign to a different user for an entitlement review.

 To assign the task:

1.  Select the View Task icon ![View task.](../image/pop-out-icon.png) in the activity card to open the case task in a new tab.
2.  Select the user in the **Assigned to** field.
3.  Add information to the other fields on the Case Task form as needed and select **Save**.

 Agent actions:

-   **Request info**: Requests additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Review complete**: Marks the case task as complete.

</td></tr><tr><td>

 

</td><td>

Billing review for any refunds

</td><td>

Case task that an agent can assign to a different user for a billing review.

 To assign the task:

1.  Select the View Task icon ![View task.](../image/pop-out-icon.png) in the activity card to open the case task in a new tab.
2.  Select the user in the **Assigned to** field.
3.  Add information to the other fields on the Case Task form as needed and select **Save**.

 Agent actions:

-   **Request info**: Requests additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Review complete**: Marks the case task and the Research stage as complete.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

Activity that displays the details of the email that was automatically sent to the customer at the completion of the Research stage.

</td></tr><tr><td>

**Respond** Guides the agent in drafting a response to the case.

</td><td>

Compose email

</td><td>

Activity that the agent can use to communicate with the customer. Agent actions:

-   **Request info**: Requests additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Review complete**: Marks the case task and the Respond stage as complete.

</td></tr><tr><td>

**Resolve** Manages the activities for case resolution.

</td><td>

Propose resolution

</td><td>

Activity that shows the fields from the Resolution Notes section on the Case form. An agent can add the resolution details and select **Propose solution**.If the customer rejects the solution, the agent can return to the Resolve stage and propose another solution.

 Agent actions:

-   **Propose solution**: Proposes the solution to the customer and marks the Resolve stage as complete.
-   **Change solution**: This action appears after the agent proposes a solution.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

Activity that displays the details of the email that was automatically sent to the customer at the completion of the Resolve stage.

</td></tr><tr><td>

**Close** Manages the activities for closing the case and sending a survey to the customer.

</td><td>

Close case

</td><td>

When the customer accepts the resolution, the Resolve stage completes and the Close stage is also marked as complete.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

Activity that displays the details of the email that was automatically sent to the customer at the completion of the Close stage.

</td></tr></tbody>
</table>## Process-based page variant for complaint case type

The Case Playbook for Complaints v5.0 application includes a process-based page variant that you can activate and use with the complaint case type in CSM Configurable Workspace. This page includes the following features:

-   Horizontal stage picker in the record that provides an end-to-end view of the complaint process.
-   Related list tabs that are displayed in the Dynamic Related Records component in the contextual side panel.
-   Persistent account and contact information that is displayed in the panel.
-   **Email** tab that is displayed in the **Activity Stream**.
-   Email templates that are displayed in the contextual side panel.
-   Customization of the start and end states of the approval flow as fields in the Approval request activity.

Agents can create tasks as needed as well as view and update case details. For more information, see [Playbook pages](csm-playbook-pages.md).

