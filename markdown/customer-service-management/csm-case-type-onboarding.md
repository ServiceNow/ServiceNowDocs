---
title: Case Playbook for Onboarding
description: Use the Case Playbook for Onboarding to manage the process for taking on new customers or enrolling customers for new products.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 14
breadcrumb: [Playbook applications, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Case Playbook for Onboarding

Use the Case Playbook for Onboarding to manage the process for taking on new customers or enrolling customers for new products.

The onboarding playbook provides the activities and tasks that agents can perform during the onboarding process. Agents can also create and assign tasks as needed and use the playbook to communicate with the customer.

Use the Case Playbook for Onboarding for cases that were created by using the onboarding case type. This playbook is available for both CSM Configurable Workspace and CSM Agent Workspace. In the CSM Workspaces, the playbook appears in the **Playbook** tab on the case record.

**Note:** If you have the admin role, you can configure a playbook to use compact mode in CSM Configurable Workspace. Use the compact mode to move the playbook from a tab in the Workspace to a tab in the contextual side panel.

## Case Playbook for Onboarding application

The Case Playbook for Onboarding application \(com.sn\_csm\_onboarding\_caseflow\) is available from the ServiceNow® Store. For more information, see [Playbook plugins](setting-up-csm-playbooks.md#section_qgq_ylk_llb).

## Case Playbook for onboarding a PAD process definition

The Case Playbook for Onboarding 3.0 includes a new Process Automation Designer \(PAD\) process definition called **onboarding\_playbook\_v1**. This process definition contains the optimized stages and activities for the onboarding playbook.

Process definitions are stored in the Process Definitions table \(sys\_pd\_process\_definition\). As an admin, you can view a list of processes by doing the following task:

1.  In the application navigator, enter **sys\_pd\_process\_definition.list**.
2.  [Configure the list](https://www.servicenow.com/docs/access?context=c_PersonalLists&version=yokohama&pubname=yokohama-platform-user-interface&section=t_PersonalizeAList&ft:locale=en-US) to show the **Name** field.

Only one PAD process per playbook can be active at a time. For more information, see [Process definitions](https://www.servicenow.com/docs/access?context=process-definitions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Case Playbook for Onboarding features

The Case Playbook for Onboarding 3.0 includes the case features and workspace enhancements that are listed in the following table.

<table id="table_csx_knc_bqb"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create an onboarding case using the Case Playbook for Onboarding

</td><td>

Feature that opens the onboarding playbook and initiates the first activity in the Initiate stage, which is gathering the customer information. The agent can complete and save this activity to create the record.

 For more information, see [Create a record using a playbook](../task/csm-playbook-create-record.md).

</td></tr><tr><td>

Focused activity view

</td><td>

Feature that determines how the stages and activities appear in the playbook.

 The Case Playbook for Onboarding uses the [Focused activity view](csm-playbook-layout.md#section_oq5_3yw_5pb), which enables agents to see

-   The end-to-end life cycle of the onboarding workflow in the playbook life-cycle panel.
-   The current stage is expanded and the current activity is highlighted within the playbook life-cycle panel.
-   The current activity that is displayed in the playbook work area.

</td></tr><tr><td>

Contextual side panel

</td><td>

Feature that displays the following information:

-   Activity stream
-   Ribbon information, such as the case overview, customer details, timeline, and SLAs
-   Dynamic related records

 The activity stream and ribbon information are available in CSM Configurable Workspace only.

 For more information about using the contextual side panel, see the following topics:

-   [Using activity stream in the contextual side panel](csm-playbooks-using-activity-stream.md)
-   [Viewing the ribbon information in the contextual side panel](csm-playbooks-viewing-ribbon-info.md)
-   [Viewing dynamic related records in the contextual side panel](csm-playbooks-viewing-rel-records.md)

</td></tr><tr><td>

Activity visibility

</td><td>

Feature that enables you to control the activity visibility:

-   Hide the activities in a stage that the logged-in user can't access.
-   Hide the pending activities in a stage.

 For more information about configuring this feature, see [Configure playbook stage and activity visibility](../task/playbook-config-activity-visibility.md).

</td></tr><tr><td>

Compact mode

</td><td>

Mode that moves the playbook from a tab in the Workspace to the contextual side panel. Agents can complete the playbook activities in the side panel while they are viewing the other tabs in the record page. This mode is available in CSM Configurable Workspace only.

Users with the admin role can configure a playbook to use compact mode in the playbook component configuration in UI Builder. For more information about configuring this feature, see Integrate Playbook with Workspace.

</td></tr><tr><td>

Dynamic related records

</td><td>

Feature that displays the records in the contextual side panel. These records dynamically change based on the context of the current record or playbook activity.

 From the **Related Records** tab in the contextual side panel, agents can

-   Filter the list of related records
-   Open the list in a new tab
-   Create new records

 The dynamic related records feature is available in CSM Configurable Workspace only.

 For more information, see [Viewing related records in the contextual side panel](csm-playbooks-viewing-rel-records.md).

</td></tr><tr><td>

SLA widget

</td><td>

Activity cards in the playbook work area that can display an SLA widget. The widget appears on the activity card when the playbook activity has an SLA. The widget includes the activities in the following stages:

-   Pre-approval \(duration is 3 days\)
-   Data capture \(duration is 5 days\)
-   Due diligence \(duration is 15 days\)
-   Resolution \(duration is 20 days\)

 The color of the widget indicates the time remaining for the SLA:

-   Green: 0–50%
-   Yellow: 50–75%
-   Orange: 75–99%
-   Red: 100% or breached

</td></tr></tbody>
</table>## Using the playbook stage and activity pickers to navigate the stages and activities

The playbook stage picker enables agents to see the entire onboarding workflow. Agents can navigate the playbook stages and activities by doing the following tasks:

-   Expand and collapse the stages to show or hide the activities.
-   Use the filter in the stage picker to filter activities by the assigned user or the activity state.
-   Click an activity to display the details in the playbook work area.

## Using the Playbook Actions menu

The Playbook Actions menu in the playbook header includes the actions that agents can perform at the playbook and activity levels. The agents can select the Playbook Actions icon \(![Playbook actions menu icon.](../image/playbook-ellipses.png)\) to access this menu.

The Playbook Actions menu includes the following playbook-level actions:

-   **Expand All Stages**: Expands all the stages in the playbook.
-   **Collapse All Stages**: Collapses all the stages in the playbook.
-   **Request Info**: Displays a pop-up window that the agent can use to communicate with the customer and to request information about a case or case task. This action also saves the details to the case or case task activity stream. By using this action, the state of the case or case task changes to Awaiting Info and pauses the SLAs and any timers.
-   **Info Received**: Returns the case or case task to the previous state and restarts the SLAs and any timers.

**Note:** The **Request Info** and **Info Received** actions can also be configured to appear on the case task activity cards.

The activity-level actions can vary depending on the type of activity and in which stage it appears. For example, actions are available to accept cases, create related cases, create case tasks, and propose solutions.

## Onboarding playbook stages and activities

The following table lists the Case Playbook for Onboarding stages and activities that agents can use to onboard new customers or products.

<table id="table_onboarding_case_playbook"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

**Initiate** Guides the agent in collecting customer and case information and sending a case for pre-approval.

</td><td>

Collect customer information

</td><td>

When an agent creates an onboarding case, the workspace opens the Create New Onboarding Case form, launches the onboarding playbook, and uses the first activity to gather customer information.

 The agent enters the information about the channel, account, contact, consumer, product, and service.

 For more information about the products and services, see [Service definitions](csm-service-definitions.md).

 Agent actions:

 **Continue**: Creates the onboarding case and adds the case number to the record tab. It also marks the first activity as complete and moves to the second activity.

</td></tr><tr><td>

 

</td><td>

Add additional members

</td><td>

Activity that agents can use to add additional members to the onboarding case:

1.  Select **Add new** to open the Create New Related Party form in a new tab.
2.  In the **Type** field, select the related party with the correct entity type, such as a beneficiary who is a customer contact.
3.  Select the **User**.
4.  Select **Save** to add the user to the Member Information list on the activity card.

 Agent actions:

-   **Assign to me**: Available if the case is not yet assigned. Assigns the case to the logged-in user.
-   **Add new**: Adds a user to the Member Information list.
-   **Send for Pre Approval**: Completes the Initiate stage and moves to the Pre-approval stage.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

Activity that displays the details of the email that was automatically sent to the customer at the completion of the Initiate stage.

</td></tr><tr><td>

**Pre approval** Automates the pre-approval process for the customer.

</td><td>

Check approval status

</td><td>

Activity that includes a list of approvals and approvers. **Note:** This activity shows the list of approvals if an approval workflow is manually configured for an onboarding case. The approval workflow configuration is not provided in the base system. If no approval workflow is configured, this activity completes automatically.

</td></tr><tr><td>

 

</td><td>

Update customer information

</td><td>

Agents can use this activity to verify the account, contact, or consumer information for the onboarding case.

 Agent actions:

 **Save**: Saves any changes made to the customer information.

</td></tr><tr><td>

 

</td><td>

Complete pre approval

</td><td>

Agents can use this activity to provide additional information and add notes or attachments.

 Agent actions:

-   **Request info**: Requests additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Initiate Data Capture**: Marks the activity and the Pre approval stage as complete.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

This activity displays the details of the email that was automatically sent to the customer at the completion of the Pre approval stage.

</td></tr><tr><td>

**Data capture** Organizes the collection of customer information.

</td><td>

Verify document checklist

</td><td>

This activity displays a document checklist. Agents can check off the necessary documents and provide comments or work notes.

 If the customer type changes after the case is created, a new checklist of the appropriate type replaces the original checklist.

 Agent actions:

-   **Request info**: Request additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Submit for Review**: Marks the activity and the Data capture stage as complete.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

This activity displays the details of the email that was automatically sent to the customer at the completion of the Data capture stage.

</td></tr><tr><td>

**Due diligence** Displays case tasks for completing due diligence.

</td><td>

Perform background check

</td><td>

Agents can use this activity to perform background checks on the customer.

 Agent actions:

-   **Request info**: Request additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Review Complete**: Marks the activity as complete.

</td></tr><tr><td>

 

</td><td>

Initiate legal verification

</td><td>

Agents can use this activity to initiate the legal verification process for a customer. Agent actions:

-   **Request info**: Request additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Review Complete**: Marks the activity as complete.

</td></tr><tr><td>

 

</td><td>

Review credit history

</td><td>

Activity that the agents can use to review a customer's credit history. Agent actions:

-   **Request info**: Request additional information from the customer. This action changes the state of the case task to Awaiting Info.
-   **Post**: Posts the comment or the work note to the case task record activity stream.
-   **Review Complete**: Marks the activity and the Due Diligence stage as complete.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

This activity displays the details of the email that was automatically sent to the customer at the completion of the Due Diligence stage.

</td></tr><tr><td>

**Resolve** Manages the case resolution activities.

</td><td>

Propose resolution

</td><td>

Activity that displays the fields from the Resolution Notes section on the Case form. Agents can add the resolution details and select **Propose solution**.If the customer rejects the resolution, the agent can return to the Resolve stage and propose another solution.

 Agent actions:

-   **Propose solution**: Propose the solution to the customer and mark the Resolve stage as complete.
-   **Change solution**: This action appears after the agent proposes a solution.

</td></tr><tr><td>

 

</td><td>

Notify customer

</td><td>

This activity displays the details of the email that was automatically sent to the customer at the completion of the Resolve stage.

</td></tr><tr><td>

**Close** Manages the case close activities.

</td><td>

Notify customer

</td><td>

Activity that displays the details of the email that was automatically sent to the customer at the completion of the Close stage.

</td></tr><tr><td>

 

</td><td>

Close case

</td><td>

When the customer accepts the resolution, the Resolve stage completes and the Close stage is also marked as complete.

</td></tr></tbody>
</table>## Process-based page variant for onboarding case type

The Case Playbook for Onboarding v5.0 application includes a process-based page variant that you can activate and use with the onboarding case type in CSM Configurable Workspace. This page includes the following features:

-   Horizontal stage picker in the record that provides an end-to-end view of the onboarding process.
-   Related list tabs that are displayed in the Dynamic Related Records component in the contextual side panel.
-   Persistent account and contact information that display in the panel.
-   Displays **Email** tab in the **Activity Stream**.
-   Email templates that are displayed in the contextual side panel.
-   Customization of the start and end states of the approval flow as fields in the Approval request activity.

Agents can create tasks as needed and view and update the case details. For more information, see [Playbook pages](csm-playbook-pages.md).

## Guided Playbook for Onboarding Request

The Case Playbook for onboarding has undergone modifications in Playbooks for Portals to expose the initiate stage for self-service. This change will provide the guided playbook intake process to end customers as well, previously available only to agents. The experience is initially shipped as inactive to customers.

End customers now have visibility into the entire lifecycle of the onboarding application when viewing the case application. They can perform various tasks based on the specific stage of the case lifecycle. This includes submitting new cases, checking the status of existing cases, and taking actions on tasks that require customer input as the case progresses.

Contributor users, on the other hand, have the ability to submit cases and act on tasks on behalf of the customer. During the initiate stage of the onboarding case type, end customers have the option to save their progress. Additionally, they can view the case process on the case ticket page specifically designed for onboarding cases. The flows within the system guide users through the step-by-step completion of both simple and complex processes, ensuring a smooth and efficient experience.

![Stages and activities in guided onboarding flow](../image/playbook-guided-onboarding-flow.png "Guided Playbook for Onboarding Request")

As customer, you can:

-   Locate the catalog content item 'New Guided Onboarding Request' under the 'Support' category in the service catalog.
-   Launch the playbook record generator associated with the selected content item.
-   Monitor your progress in the submission process, including the number of remaining steps and the ability to navigate back to previous steps when viewing a playbook.
-   Easily populate the required fields with the options provided and input controls.
-   Save an application or form before it is ready for submission and resume working on it at a later time.
-   Locate the draft case from the case list view to continue where you left off.
-   Click **Submit** to complete the initiation stage during the **Review Application**step.
-   Receive a notification if there are any pending tasks due to missing documents.
-   Access the case ticket page directly from the email notification, with the process tab open, displaying the **Data Capture** stage and the **Upload Documents** activity.

Known limitations:

-   If you switch to the new Process Automation Designer \(PAD\) with the existing service definition and the old record generator, you may encounter a configuration error page when attempting to create onboarding from the case type selector. You need to update the service definition's references as well to the new record generator.
-   The Portal playbook experience only supports the New PAD. Customers may encounter issues if they attempt to use the old PAD, so it is recommended not to use it. Ensure that only one PAD is active at a given time.

