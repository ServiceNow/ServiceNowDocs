---
title: Create a change request
description: Create a change request to implement a controlled process for modifying approved and supported configuration items \(CIs\).
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Use, Change Management, IT Service Management]
---

# Create a change request

Create a change request to implement a controlled process for modifying approved and supported configuration items \(CIs\).

## Before you begin

Role required: itil, admin, or sn\_change\_write

## About this task

A change request records the detailed information about the change, such as the reason of the change, the priority, the risk, the type of change, and the change category.

If you use conflict detection, the planned start and end dates and the configuration item \(CI\) are required.

**Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

## Procedure

1.  Create the change request with one of these options.

<table id="choicetable_agp_ckc_3t"><tbody><tr><td id="d183194e99">

**From the Change module**

</td><td>

You can create all three types of change from the **Change** module.1.  Navigate to **All** &gt; **Change** &gt; **Create New**.
2.  Select **Normal**, **Emergency**, or **Standard** changes.
 If you're an upgrade customer and willing to use change models, you must enable the change model properties. For information on change models and its properties, see [Change models](../concept/change-models.md).

 When you enable the change model properties, you see the following tabs when you navigate to **All** &gt; **Change** &gt; **Create New**.

 -   **Models**: Shows all the available models available to select.
-   **Preapproved**: List of preapproved models to select.
-   **Pinned**: Models that you have pinned from the **Models** and **Preapproved** tabs.
-   **All**: All models are available to select.


</td></tr><tr><td id="d183194e195">

**From an incident or a problem**

</td><td>

As a user with the sn\_change\_write role, you can create a standard, normal, or an emergency change from an incident or a problem.1.  Open the incident or problem.
2.  Right-click the form header and select **Create Normal Change**, **Create Standard Change**, or **Create Emergency Change**.


</td></tr><tr><td id="d183194e222">

**From an existing change record**

</td><td>

If the administrator enabled the change request copy option, you can create a new change by copying an existing change record.1.  Open the change record that you want to copy.
2.  Select **Copy Change**.
 **Note:** If the create task workflow sets the **create\_from** field in the \[change\_task\] table to **workflow**, manually created tasks from the existing change record are copied.

</td></tr><tr><td id="d183194e252">

**From a change template**

</td><td>

1.  Navigate to **All** &gt; **Change** &gt; **Create New**.
2.  Select **Templates**.
3.  Search for and select the required template.
4.  View the new change request record created using the selected template by selecting **Continue**.
 **Note:** When you select an existing template, information in the predefined fields will be populated. Template fields are either read-only or mandatory depending on the template field policies configured while creating the template.

For more information on change templates, see [Change templates](../concept/change-templates.md).

</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_ij1_vgq_dq"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Change request number.

</td></tr><tr><td>

Requested by

</td><td>

User who requested the change. This field is available in the **Change Requests** list view, so that you can see who requested a particular change.

</td></tr><tr><td>

Category

</td><td>

Category of the change, for example, **Hardware**, **Network**, **Software**.

</td></tr><tr><td>

Service

</td><td>

Business service that you want to make available for the change request.**Note:** If you select a business service as the configuration item and that business service is also listed as the configuration item in any other active task, the active tasks icon \(![Active tasks icon.](../image/other-active-task.png)\) appears. Select this icon to view the list of all the other active tasks that are affecting the business service. You can view the BSM map \(dependency view\) of the selected business service by clicking the dependency icon \(![Dependency icon.](../image/dependency-icon.png)\).

</td></tr><tr><td>

Service Offerings

</td><td>

Consists of one or more service commitments that uniquely define the level of service in terms of availability, scope, pricing, and packaging options. You can choose to receive different levels of performance and features for a given service through service offerings. You must select a service to filter the available service offerings.

</td></tr><tr><td>

Configuration item

</td><td>

Select **Add** to add a CI for the change. You can add a CI for a change in **New** state only.

CI that the change applies to. Change requests can be associated with any type of CI, including service offerings, providing detailed access to SLA and availability requirements.When you select a dynamic CI group, all the configuration items related to the selected dynamic group will be populated in the Affected CIs related list. In the Affected CIs related list, you can also manually add and delete the dynamic CI groups. When you add a dynamic CI group, all the related CIs are added, and when you remove a dynamic CI group, the related CIs are removed.

 After selecting a CI, you can select the health dashboard icon \(![Health dashboard icon.](../image/Change_CIHealthIcon.png)\) to view the CI health details.

 **Note:** By default, Service Offering is filtered out and CIs with Principal Class are selected. The Principal Class filter functionality is applicable to new customers starting the Paris release.

 See [Refresh impacted services properties](../reference/refreshing-impacted-services-properties.md)

</td></tr><tr><td>

Priority

</td><td>

Priority is based on impact and urgency, and it identifies how quickly the service desk should address the task.

</td></tr><tr><td>

Risk

</td><td>

Risk level for the change. The Risk value is **-- None --** until you define it as **High**, **Moderate**, or **Low**. You can also use [Risk Calculation and Risk Assessment](../concept/c_RskAsmtCalc.md) to drive the risk value of the change.

</td></tr><tr><td>

Impact

</td><td>

Impact is a measure of the effect of an incident, problem, or change on business processes.

</td></tr><tr><td>

Model

</td><td>

Change model being used for the change request.For information about Change models, see [Change models](../concept/change-models.md).

</td></tr><tr><td>

Type

</td><td>

The type of change request. The field displays **Model** if the Change model has not been configured with a defined Type. This field is read-only.For information about creating Change models, see [Create a Change model](create-a-change-model.md).

</td></tr><tr><td>

State

</td><td>

State of the change request. The default state is New.

</td></tr><tr><td>

Conflict status

</td><td>

Status that indicates whether there is a conflict for this change or the conflict is not run.

</td></tr><tr><td>

Conflict last run

</td><td>

Date and the time when the conflict was last run.

</td></tr><tr><td>

Assignment group

</td><td>

Group who will work on the change request. The business rule **Populate Assignment Group based on CI/SO** populates the **Assignment group** field available for the CI or the service offering consecutively.

**Note:** The business rule is triggered when a change request is created or updated and when the **Assignment group** and the **Assigned to** fields are empty.

If you want to override the default value, you must create properties and provide the field in the property value that must be used to populate the **Assignment group** field. Create the properties in the following order of preference:

-   **com.snc.change\_request.ci\_assignment\_group.field\_name**: Identifies which CI field populates the **Assignment group** field.
-   **com.snc.change\_request.service\_offering\_assignment\_group.field\_name**: Identifies which service offering field populates the **Assignment group** field.


</td></tr><tr><td>

Assigned to

</td><td>

User that the change is assigned to. If an assignment rule applies, the change is automatically assigned to the appropriate user or group.

</td></tr><tr><td>

Short description

</td><td>

Summary of the change.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the change.

</td></tr></tbody>
</table>3.  To plan the change, select the **Planning** tab and enter information.

    This information is critical for change approvers.

4.  Select the **Schedule** tab.

    1.  Enter as much information about the scheduled dates as you have.

        Some of the fields are available for normal or emergency changes only because standard changes are preapproved.

        **Note:** For normal or emergency changes, enter the planned start and end dates and actual start and end dates manually. Populate the actual start and end date fields during the Implement state as the assignee begins and completes the work.

    2.  If the form is configured to show the **CAB required** check box, select it to indicate that CAB approval is required before implementation.

        The **CAB date** field in the change request is automatically updated with the date in the **Meeting start time** field of the CAB meeting form.

    3.  If there is an unplanned CI activity, select the **Unauthorized** check box to determine if the change is an unauthorized change.

        For more information, see [Unauthorized change request](../concept/unauthorized-change-request.md).

        **Note:** This check box is available only for emergency change requests.

    4.  If the form is configured to show the **CAB delegate** field, select the user who attends the CAB meeting to describe the change.

    5.  In the **CAB recommendation** field, enter notes or recommendations related for the CAB meeting.

5.  Select the **Conflicts** tab.

6.  To detect change conflicts, select **Check conflicts**.

7.  Right-click the form header and select **Save.**

8.  Review entries in the related lists and modify the entries as appropriate.

<table id="table_fc1_kth_5r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Affected CIs

</td><td>

List of CIs \(from the CMDB\) affected by the change. You can associate multiple affected CIs with a change.

</td></tr><tr><td>

Impacted services/CIs

</td><td>

List of CIs, such as business services or from other CI classes, that are impacted by the affected CI in the change. You can associate multiple impacted CIs with a change.

</td></tr><tr><td>

Service Offerings

</td><td>

List of service offerings affected by the change. You can associate multiple service offerings with a change. This related list is available only when a service offering is selected.If there are service offerings associated to the Impacted Services, then refresh the Impacted services/CIs related list to view the offerings.

 **Note:** If you have customized the default view of your form or related list prior to the Paris release, you cannot see the field or the related list by default. Modify the form to add them manually.

</td></tr><tr><td>

Approvers

</td><td>

This list is automatically generated from the workflow. You can also view the **Group** of approvers assigned to the task.

</td></tr><tr><td>

Change Tasks

</td><td>

The list of tasks can be created from a workflow. The default workflow generates tasks in the **Implementation** state. You can also create a change task. The **Planned start date** and **Planned end date** in task type **Implementation** must fall within the planned start and end dates specified in the change request.

</td></tr><tr><td>

Problems

</td><td>

If the change was generated from a problem, this list is generated automatically.

</td></tr><tr><td>

Incidents Fixed by Change

</td><td>

List of incidents that require the change for resolution.

</td></tr><tr><td>

Incidents Caused by Change

</td><td>

List of incidents caused by the implementation of the change.

</td></tr><tr><td>

CAB Agenda Items

</td><td>

List of agenda items and details of respective items. For example, the meeting start and end time, allocated time for the meeting, state of the meeting, and the decision made for that agenda item.**Note:** The CAB Agenda Items related list is not shown on the form when the list is empty. This feature is available only for Jakarta instances.

</td></tr></tbody>
</table>9.  When the change request is ready to move to the next state, select **Request Approval**.

    The state is moved forward based on the type of change request:

    -   Assess state: Group level approval for a normal change request. Approval records are automatically generated based on the **Assignment group**. You can conduct peer and technical reviews of the proposed change.
    -   Authorize state: An emergency change request.
    -   Scheduled state: Pre-approved standard changes.
    **Note:** To mail the change record, select the more options icon \(![More options icon.](../image/more-options.png)\) in the content frame and select **Email**. Both the user who requested the change and the user who is assigned to the change are automatically populated in the list of recipients.

    To view the calendar, select **View Calendar** in the title bar of the Change Request form.


## What to do next

[Process a change request](t_ProcessAChangeRequest.md)

-   **[Create a change request from a configuration item \(CI\)](t_CreateAChangeFromACI.md)**  
Create a change request from a list of configuration items \(CIs\), or add selected CIs from a list to a change record.
-   **[Create a standard change request from the catalog](t_RaiseNewStdCngeFmTempl.md)**  
You can create a standard change request from the published standard change catalog templates.
-   **[Copy a change request](copy-a-change-request.md)**  
You can copy details of an active or canceled change request to a new change request.
-   **[Create a change task](create-a-change-task.md)**  
You can create change tasks for a change request. A change task is a piece of work related to the change request. For example, there can be tasks to plan the change, implement the change, and test, and review the work.
-   **[Unauthorized change request](../concept/unauthorized-change-request.md)**  
Understand how an unauthorized change activity on a configuration item \(CI\) is captured and managed, so that you can review and take timely action on this change.

**Parent Topic:**[Using Change Management](../concept/using-change-management.md)

**Related topics**  


[Legacy: State model and transitions](../concept/c_ChangeStateModel.md)

[Place a change request on hold](t_PlaceAChangeRequestOnHold.md)

[Conflict calendar](../concept/change-conflict-calendar.md)

