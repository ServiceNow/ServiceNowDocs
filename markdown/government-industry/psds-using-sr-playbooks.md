---
title: Using Service Request Playbooks
description: If you're a government service agent or manager, you can use the Service Request Playbook for Public Sector Digital Services to manage and resolve requests for services like park maintenance, broken stop signs, or other types of community issues.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Playbooks, Use, Public Sector Digital Services \(PSDS\)]
---

# Using Service Request Playbooks

If you're a government service agent or manager, you can use the Service Request Playbook for Public Sector Digital Services to manage and resolve requests for services like park maintenance, broken stop signs, or other types of community issues.

A playbook provides a step-by-step guidance through the life cycle of a government service case.

The Service Request Playbook automatically appears in the **Playbook** tab when you open or create a service request case in the CSM Configurable Workspace.

A playbook takes a workflow and breaks it into multiple stages or lanes. Each stage in a playbook includes one or more activities, or steps, for you to complete. Stages can also include automated activities, such as auto-sending an email to a constituent when a stage or activity is complete, or auto-sending a work order to a field service agent. When using a playbook, you can:

-   View the playbook stages and activities.
-   Select an activity and perform the work to complete that activity.
-   Mark an activity as complete and move to the next activity or stage.
-   Complete the stages and activities to resolve the case.

The workflows that are associated with a specific type of case and the activities that need to be completed to resolve this type of case are detailed in the playbook. Playbooks also help you to visualize the entire lifecycle of the service request workflows by displaying your progress through the playbook in the header.

## Playbook stages

The Service Request Playbook has four stages, listed in the following table.

|Task|Description|
|----|-----------|
|Intake|Guides you through the record creation process by capturing the details of the service request and assigning it to the right agent.|
|Review|Acts as a checkpoint for duplicate cases and provides you with an opportunity to review the case details to verify that the issue is valid and needs to be resolved.|
|Process|Guides you through the activities for case resolution.|
|Decision|Captures and communicates the decision that you made on the service request to the constituent and any other agents or involved parties.|

## Playbook layout

A playbook is made up of several areas, including the playbook life cycle, the playbook work area, and the contextual side panel. The activity view determines how the stages and activities appear in the playbook.

The default activity view for the Service Request Playbook is the Process-based experience view. This view, which is shown in the following example, shows constituent or business information and case task information at the forefront of the playbook work area as you work on it.

The process-based playbook layout shows the following features:

-   A horizontal stage picker that gives the agent a complete view of the entire process and where they currently are in that process. Agents can use the stage picker to track their overall progress as they work on cases.
-   Record information on the left side of the page, such as the contact information that is always available.

-   Related records in the contextual side panel supported by the dynamic related records component.

![Agent workspace view of the playbook lifecycle, case record information, and service request details, shown in process-based activity view. For the text description, refer to the Playbook components table.](../image/service-request-process-based-layout.png "Playbook layout with the Process-based experience view")

The following table shows the components that you can see in the Service Request Playbook process-based workspace.

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

</td></tr><tr><td>

Service Request Map Card

</td><td>

-   New component of the process-based playbook layout.
-   Appears after the intake stage, if the sn-geo-map plugin is installed, and Google API key is configured.

</td></tr></tbody>
</table>