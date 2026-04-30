---
title: Global domain configurations
description: Administrators in the global domain can select configuration settings that determine how Field Service Management handles daily operations.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Planning your Field Service Management implementation, Configuring Field Service Management, Field Service Management]
---

# Global domain configurations

Administrators in the global domain can select configuration settings that determine how Field Service Management handles daily operations.

## Before you begin

Role required: wm\_admin

## About this task

Administrators in the global domain can set Field Service Management configurations to:

-   Include or exclude portions of the request process. For example, you can require a work order to be approved before continuing to the next stage.
-   Automatically assign tasks using SM Auto-Assignment, a custom-defined workflow, or leave it up to dispatchers to manually assign tasks. You can manually assign using Central Dispatch, or from the work order task form.
-   Track agent travel time.

The Field Service Configuration screen contains many configuration options. An option is enabled when the switch appears green and is toggled to the right. All configuration options listed in the **Dependency** must be enabled in order for the option to be displayed.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Configuration**.

    **Note:** Administrators in domains lower than the global domain can view the Field Service Configuration screen, but cannot modify the settings.

    The options on the Field Service Configuration screen are arranged in a multiple-tabbed layout, as follows:

    -   The **Business Process** tab contains options for setting up the request life cycle, creating catalogs and requests, and configuring notifications.
    -   The **Assignment** tab contains options for setting up manual and auto-assignment.
    -   The **Add-ons** tab contains options for enabling the knowledge base, managed documents, and task activities.
2.  Fill in the fields on the **Business Process** tab.

    The field **Agent must accept or reject the assigned task** applies to both internal and external Field Service agents.

<table id="BusinessProcess"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Dependency

</th></tr><tr><th class="sub-head" id="LifecycleOptions" colspan="2">

Lifecycle

</th><th>

 

</th></tr></thead><tbody><tr><td>

Process life cycle

</td><td>

By default, the process life cycle is set to task-driven which supports workflows on work order tasks for Dispatcher Workspace, FSM Mobile, and Schedule Optimization.

 Starting with the Xanadu release, the request driven process life cycle is no longer supported. Only users with the maint role have the option to change the Process life cycle to **request driven \(subtasks are optional\)**. Request driven doesn't require tasks to fulfill requests. When the process life cycle is request driven, requests can be directly assigned to users in an assignment group. Users can still add tasks to requests. However, closing all tasks does not automatically close the request.

**Note:** If the **Enable state flows** option is not selected, the process life cycle becomes **request-driven** and this field is not displayed.

</td><td>

 

</td></tr><tr><td>

Approval for new request required

</td><td>

When disabled, all requests in the **Awaiting Approval** state are automatically approved.

</td><td>

**Enable state flows** is turned on.

</td></tr><tr><td id="QualificationRequired">

Qualification is required for new requests

</td><td>

Enable to require work orders to be qualified before moving to the next state. If this option is not enabled, any work orders in the Awaiting Qualification state are automatically qualified.

</td><td>

-   **Enable state flows** is turned on.
-   **Process life cycle: task driven \(subtasks are optional\)**.


</td></tr><tr><td>

Agent must accept or reject the assigned task

</td><td>

Enable to require the assigned agent to accept or reject the task.

</td><td>

**Enable state flows** is turned on.

</td></tr><tr><td>

Track agent travel time

</td><td>

Enable to use time cards for agent travel for a task.

</td><td>

 

</td></tr><tr><td>

Enable/Disable Onsite Arrival Check-in for Agents

</td><td>

Enable to capture agent location at on-site check-in using the **Onsite arrival** substate. The feature also uses geofencing to verify agent's mobile location and allows them to bypass check-in when they are in offline mode or for other reasons.

</td><td>

 

</td></tr><tr><td>

Work notes are required to close or cancel a request or task

</td><td>

Enable if work notes are required when closing, completing, or canceling requests and tasks. If it is disabled, work notes are not needed when closing, completing, or canceling.

</td><td>

 

</td></tr><tr><td>

Copy task work notes to request

</td><td>

Enable to synchronize task work notes with the work notes on the order or request. When work notes are added in the task, the same work notes appear in the order or request.

</td><td>

**Enable state flows** is turned on.

</td></tr><tr><td>

Auto close case on work order closure

</td><td>

Enable to automatically close the case when all its related work orders are closed or canceled. Auto closure of a case updates the following fields in the case form with the given status.-   **resolution code**: Solved- Fixed by closing related issue
-   **additional notes**: Auto Closed Case- Related work orders are closed


</td><td>

 

</td></tr><tr><td>

Update work order states to case

</td><td>

Enable to automatically update the **Additional comments** field in the case form whenever the state of each work order that is related to that case gets updated.

</td><td>

 

</td></tr><tr><td>

Apply Work Order template in draft status

</td><td>

Enable this option to create tasks for the work order based on the applied work order template without the qualification of the work order, even when the work order is in the draft state.

</td><td>

 

</td></tr><tr class="sub-head"><td class="sub-head" colspan="3">

**Catalog and Request Creation**

</td></tr><tr><td>

Create or update requests by inbound email.

</td><td>

Enable this option to allow inbound email messages to create or update requests. This option must be enabled to allow requests to be marked as spam.

</td><td>

 

</td></tr><tr><td>

Requests are created using

</td><td>

Select **catalog or regular form** to install the catalog and enable automatic publishing of request templates to the catalog.Select **regular form only** to uninstall the catalog and disable automatic publishing of request templates to the catalog.

</td><td>

 

</td></tr><tr><td>

Templates create a dedicated catalog item

</td><td>

Enable this option to allow automatic publishing of catalog items for the application.

</td><td>

 

</td></tr><tr class="sub-head"><td colspan="3">

**Notification**

</td></tr><tr><td>

Send a notification when a field changes for a task or request.

</td><td>

Configure notifications to be sent to specific recipients when selected fields in requests and/or tasks change. 1.  From **Table**, select **Request** or **Task**.
2.  From **Field**, select the field to use for generating notifications. When a change is made to the selected field, a notification is sent to the recipients identified.
3.  From **Recipients**, select one or more recipients
4.  If **a specific user** or **a specific group**, is selected, the user is prompted to select a user or group.
5.  To define more notifications using other fields or recipients, repeat the steps on the next line.
6.  To remove a notification, click the ![delete notification symbol](../image/DeleteNotification.png) symbol to the right of the notification.


</td><td>

 

</td></tr></tbody>
</table>3.  Click the **Assignment** tab and fill in the fields.

<table id="AssignmentOptions"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Dependency

</th></tr></thead><tbody><tr><td>

Assignment method for tasks

</td><td>

Select one of the following task assignment options:-   Select **using auto-assignment** to automatically assign work order tasks to field service agents.
-   Select **using a workflow** to assign work order tasks using a custom-designed workflow.
-   Select **manually** to allow dispatchers to manually assign work order tasks.
-   Select **using dynamic scheduling** to use the dynamic scheduling feature.


</td><td>

 

</td></tr><tr><td>

Use scheduled state

</td><td>

Enable this option to use the **Scheduled** state in between **Ready for Dispatch** and **Assigned** states in work orders and work order tasks.

</td><td>

 

</td></tr><tr><td>

Use dispatch queue

</td><td>

Enable this option to use the dispatch group for manual assignment.

</td><td>

-   **Enable state flows** is turned on.
-   **Process life cycle: Life cycle is task driven**.


</td></tr><tr><td>

Restrict vendor groups

</td><td>

Enable this option to limit the selection of external vendor groups from the **Assignment group** field based on the selected dispatch group in the work order task form.

</td><td>

**Use dispatch queue** is turned on.

</td></tr><tr><td>

Preferred assignment group

</td><td>

Select one of the following task assignment options:-   Select Internal group to prioritize assigning the work order tasks to internal agents.
-   Select External group to prioritize assigning the work order tasks to external agents or vendors.
 **Note:** This configuration field displays only if the Field Service Contractor Management plugin \(com.snc.fsm\_contractor\_management\) is activated.

</td><td>

 

</td></tr><tr><td>

Assign requests or tasks based on assignment group coverage areas

</td><td>

Enable this option to limit the selection of groups from the **Dispatch group** and **Assignment group** fields to groups that cover the location of the task.

</td><td>

 

</td></tr><tr><td>

Assign tasks based on assignment group product models

</td><td>

Enable this option to limit the selection of groups from the **Dispatch group** and **Assignment group** fields to groups that cover the necessary product model requirement of the task.

</td><td>

 

</td></tr><tr><td>

Assign tasks based on assignment group skills

</td><td>

Enable this option to limit the selection of groups from the **Dispatch group** and **Assignment group** fields to groups that cover the skills that are required to perform the task.

</td><td>

 

</td></tr><tr class="sub-head"><td colspan="3">

**Scheduling**

</td></tr><tr><td>

Use agent or task scheduling

</td><td>

Enable this option to allow agent auto-assignment and agent auto-selection.

</td><td>

 

</td></tr><tr><td>

Auto-selection of agents will consider time zone for tasks

</td><td>

Enable this option to consider the time zone of the agent when assigning a task.

</td><td>

**Enable state flows** is turned on.

</td></tr><tr><td>

Enable Shift Scheduling for FSM to determine availability

</td><td>

Enable this option to consider agent's schedules, skills, teams, and coaching to optimize your Field Service workforce accordingly.

</td><td>

[Activate Workforce Optimization for Field Service](../../field-service-management/task/activate-wfo-fsm.md).

</td></tr><tr><td>

Enable priority assignment

</td><td>

Enable this option to use priority assignment for auto-assigning agents.

</td><td>

-   **Enable state flows** is turned on.
-   **Process life cycle: Life cycle is task driven**.
-   **Auto-selection of agents will consider agent or task schedules**.
 **Note:** The **Process life cycle** option is not available in all service management applications.

</td></tr><tr class="sub-head"><td colspan="3">

**Additional Factors**

</td></tr><tr><td>

Auto-selection of agents will consider location of agents

</td><td>

Enable this option to use the agent and location when determining who to assign the task to. Agents closer to the task location receive preference.

</td><td>

-   **Enable state flows** is turned on.
-   If using **Process life cycle: Life cycle is task driven**, then **Assignment method for tasks: using auto-assignment**.
-   If using **Process life cycle: Life cycle is request driven**, then **Assignment method for requests: using auto-assignment**.


</td></tr><tr><td>

Auto-selection of agents for tasks requires them to have skills

</td><td>

This option determines the degree to which skills must be matched to a task when determining auto-assignment. -   Select **all** to require that an assigned agent has all the skills to perform the task. An agent who lacks one skill is eliminated.
-   Select **some** if you want agents who have most of the skills to perform the task.
-   Select **none** if you want to auto-assign agents without considering skills.


</td><td>

-   **Enable state flows** is turned on.
-   If using **Process life cycle: Life cycle is task driven**, then **Assignment method for tasks: using auto-assignment**.
-   If using **Process life cycle: Life cycle is request driven**, then **Assignment method for requests: using auto-assignment**.


</td></tr></tbody>
</table>4.  Click the **Add-ons** tab and fill in the fields.

<table id="AddOns"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Dependency

</th></tr><tr><th class="sub-head" colspan="3">

Part Requirements

</th></tr></thead><tbody><tr><td>

Part requirements are needed by agents

</td><td>

Enable this option to require agents to specify parts for the task.

</td><td>

 

</td></tr><tr><td>

Reserve parts in agent stockroom

</td><td>

Enable this option to reserve required parts in the agent stockroom when scheduling and rescheduling work order tasks.

</td><td>

**Part requirements are needed by agents.**

</td></tr><tr><td>

Cancel open Transfer Orders

</td><td>

Enable this option to release the reservation of reserved parts in the agent personal stockroom when unscheduling work order tasks.

</td><td>

**Part requirements are needed by agents.**

</td></tr><tr><td>

Edit associated models

</td><td>

Click **add** and select the part model to be used for this task. Click **more** to select more part models.

</td><td>

**Part requirements are needed by agents.**

</td></tr><tr><td class="sub-head" colspan="3">

**Documentation**

</td></tr><tr><td>

Enable a dedicated knowledge base

</td><td>

Enable this option to install the knowledge base for the application.

</td><td>

 

</td></tr><tr><td>

Enable managed documents

</td><td>

Enable this option to add a related list to managed documents.

</td><td>

 

</td></tr><tr><td>

Enable task activities

</td><td>

Enable this option to log the task interactions and communications, such as phone calls and email messages.

</td><td>

 

</td></tr><tr><td class="sub-head" colspan="3">

**Associated Task Tables**

</td></tr><tr><td>

Select associated tables

</td><td>

Click **Add** to select more tables.

</td><td>

 

</td></tr><tr><td class="sub-head" colspan="3">

**Maps**

</td></tr><tr id="tablerow_maps"><td>

Enable maps

</td><td>

Enable this option to use maps.

</td><td>

 

</td></tr><tr><td class="sub-head" id="PDFSummaryOptions" colspan="3">

**Signature Capture and PDF Order Summary**

</td></tr><tr><td>

Signature Capture

</td><td>

Enable this option to include the name and electronic signature of the customer in the PDF work order summary.

</td><td>

 

</td></tr><tr><td>

PDF Order Summary

</td><td>

Enable this option to create a PDF summary for a work order that includes completed tasks, parts used and returned, incidental expenses, and the time required to complete the work.

</td><td>

 

</td></tr><tr><td>

Use Document Template to generate PDF Summary

</td><td>

Enable this option to create a PDF summary for a work order in a document template.

</td><td>

PDF Order Summary

</td></tr><tr><td class="sub-head" id="ServiceLocations" colspan="3">

**Service Locations**

</td></tr><tr><td>

Validation

</td><td>

Select either of the following configuration option to create ad-hoc locations:-   **Using Map**: Create location using a Google map interface.
-   **Without Map**: Create locations by enter the location details.

**Note:** The system validates the details using third party APIs extension points.

-   **No Validation**: Create locations by enter the location details including latitude and longitude coordinates.
 **Note:** This configuration field displays only if the Field Service with Service Locations plugin \(com.snc.fsm\_service\_locations\) is activated.

</td><td>

 

</td></tr><tr><td>

Initial rendering location

</td><td>

Select either of the default map location when **Using Map** configuration is enabled:-   **Browser Location**
-   **Asset Address**
-   **Contact/Caller Address**
-   **Company Address**


</td><td>

 

</td></tr></tbody>
</table>5.  Click **Save**.

    **Warning:** If you clicked the **Enable state flows** option to disable it, a confirmation box appears, along with a link to documentation that explains the consequences of disabling state flows. It is highly recommended that you read the documentation before proceeding. The action of disabling service management state flows cannot be reversed.


