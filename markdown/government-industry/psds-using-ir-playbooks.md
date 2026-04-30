---
title: Using Information Request Playbook
description: If you're an information request case agent or manager, you can use the Information Request Playbook for Public Sector Digital Services to manage and resolve requests for information and public records.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Playbooks and solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Using Information Request Playbook

If you're an information request case agent or manager, you can use the Information Request Playbook for Public Sector Digital Services to manage and resolve requests for information and public records.

A playbook provides you with step-by-step guidance through the life cycle of an information request case.

The Information Request Playbook automatically appears in the **Playbook** tab when you create an information request case by using the CSM Configurable Workspace.

A playbook takes a workflow and breaks it into multiple stages or lanes. Each stage in a playbook includes one or more activities, or steps, for you to complete. Stages can also include automated activities, such as auto-sending an email to a customer when a stage or activity is complete. When using a playbook, you can:

-   View the playbook stages and activities.
-   Select an activity and perform the work to complete that activity.
-   Mark an activity as complete and move to the next activity or stage.
-   Complete the stages and activities to resolve the case.

The workflows for a type of case and the activities that you need to resolve these cases are in the playbook. By using a playbook, you can visualize the entire life cycle of the information request workflow.

## Playbook stages

The Information Request Playbook stages are listed in the following table.

|Task|Description|
|----|-----------|
|Intake|Guides you through the record creation process by capturing the details of the information request and assigning it to the right agent.|
|Review|Acts as a checkpoint for duplicate cases and provides you with an opportunity to review the case details to verify that the issue is valid and needs to be resolved.|
|Process|Guides you through the activities for the information request fulfillment.|
|Decision|Captures and communicates the documents and information to the constituent and any other agents or involved parties.|

## Playbook layout

A playbook is made up of several areas, including the playbook life cycle, the playbook work area, and the contextual side panel. The activity view determines how the stages and activities appear in the playbook.

The default activity view for the Information Request Playbook is the Process-based experience view. This view, which is shown in the following example, shows constituent or business information and case task information at the forefront of the playbook work area as you work on it.

The process-based playbook layout shows the following features:

-   A horizontal stage picker that gives the agent a complete view of the entire process and where they currently are in that process. Agents can use the stage picker to track their overall progress as they work on cases.
-   Record information on the left side of the page, such as the contact information that is always available.

-   Related records in the contextual side panel supported by the dynamic related records component.

![Playbook layout, shown in process-based experience view. For the text description, refer to the table in Playbook components.](../image/information-request-process-based-layout.png.png "Playbook layout with the Process-based experience view")

The following table shows the components that you can see in the Information Request Playbook workspace.

<table id="table_j4r_cww_5pb"><thead><tr><th>

Playbook area

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Playbook header

</td><td>

-   Appears at the top of the playbook.
-   Shows the title of the playbook and a horizontal stage picker that displays progress through the playbook stages.
-   Includes a filter that you can use to filter the activities by the assigned user or the activity status.
-   Includes the Playbook Actions menu that you can use to select the playbook-level and activity-level actions.

</td></tr><tr><td>

Playbook Lifecycle

</td><td>

-   Appears in a panel on the left side of the playbook.
-   Displays a list of the activities for each stage.
-   With the horizontal stage layout, you can expand or collapse the entire list of activities for the current stage.

</td></tr><tr><td>

Playbook work area

</td><td>

-   Appears in the middle of the playbook.
-   Displays the card for the current activity.

</td></tr><tr><td>

Contextual side panel

</td><td>

-   Appears on the right side of the playbook.
-   Includes the tabs that you can use to display the following types of information:
    -   Case or case task activity stream.
    -   Ribbon information such as the case overview, customer details, timeline, and service level agreements \(SLAs\).
    -   Dynamic related records. For more information, see [Dynamic related records](psds-playbook-viewing-rel-records.md).

</td></tr><tr><td>

Constituent or Business Card

</td><td>

-   Contact information for the constituent or business that submitted the request.
-   Appears in a panel on the left side of the playbook.

</td></tr></tbody>
</table>**Note:** Verify that the Information Request Playbook application, which is separate from the Public Sector Digital Services Core application, has been installed and configured. For instructions, see [Install and configure the Information Request Playbook application](configuring-information-request-playbook.md).

By default, the following stages are available to you as an information request case agent in the Information Request Playbook in the CSM Configurable Workspace.

-   Intake
-   Review
-   Processing
-   Decision

## Stages in an Information Request Playbook

The Information Request Playbook experience starts with the Intake stage. This stage is the default playbook stage for a new information request case. Use this playbook stage to gather information about the requester, the documents being requested, and any exemption categories that the request falls into. You can also request additional information from the requester.

The playbook continues with the Review stage. In this stage, you can do the initial troubleshooting on the case, evaluate similar or duplicate requests, and determine whether the information requested can be released and if a fee needs to be charged. You can move the case to the next stage when the requester accepts the fee, or if a fee waiver is submitted and approved.

The playbook continues with the Process stage. In this stage, you can assess resources, request a fee approval, create case tasks, and add or request new information before the case resolution begins. The case status changes to Work in Progress once the fee payment is processed or waived. The case is then sent for legal review. After legal review is complete, the case is moved to the Decision stage. You may solicit additional information from the requester at any time during this stage.

The final stage of the Information Request Playbook is the Decision stage. At the Decision stage, the status of the case is updated from Review in Progress to Ready for Decision after the case has passed legal review. A notification is sent to the requester that lets them know that case approval has been has obtained and the requested documents have been uploaded. The requester can then either accept or reject the document. If the requester accepts the documents, the case is automatically closed. If the requester rejects the solution, the case is reopened, and the agent must propose another outcome.

