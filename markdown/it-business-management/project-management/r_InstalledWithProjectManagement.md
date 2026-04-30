---
title: Properties installed with Project Management
description: There are several Project properties that you can configure.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Reference, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Properties installed with Project Management

There are several Project properties that you can configure.

You need the pps\_admin role to access the Project properties.

Navigate to **Project Administration** &gt; **Settings** &gt; **Preferences - Project** to configure the following properties.

<table id="project_application_properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable firing of Business Rules on save from Planning Console. This property will be applicable only during insert and delete of tasks and relations.com.snc.project.fire\_brs\_from\_planning\_console

</td><td>

If set to true, the project planning console triggers business rules.**Note:** Reload the console if you make changes to this property.

 Default value: false

</td></tr><tr><td>

Enable move project for WIP projectscom.snc.project.move\_project.wip

</td><td>

If set to true, this property enables you to move the projects which are in WIP state.**Note:** When a project is moved, only tasks in open and pending state are moved and the project takes the rolled up dates from all the project tasks.

Default value: false

</td></tr><tr><td>

Calculate ROI percentage based on a project's estimated cost and its net value com.snc.project.calculate\_roi

</td><td>

If set to true, this property calculates the return on investment using the \(net value/estimated cost\) x 100 formula. This field is only available from the Advanced view of the Project form.Default value: true

</td></tr><tr><td>

Enable alter of planned date with Actual for Manual Projectcom.snc.project.change\_planned\_date\_from\_actual\_for\_manual

</td><td>

If set to true, the property recalculates the planned end date of a manual project from actual start date and planned duration.Default value: false

</td></tr><tr><td>

Enable project cost rollup \(estimated and actual\) – updating the cost of a project task will update the cost of its parent com.snc.project.rollup.cost

</td><td>

If set to true, this property updates the cost of a parent project task if the cost of the child task is updated. Default value: false

</td></tr><tr><td>

Roll up project start date from tasks com.snc.project.rollup\_project\_start\_date

</td><td>

If set to true, the project planned start date rolls up from the planned start date of the earliest task. Disable this property if you want the project planned start date to remain the same despite the start date of the earliest task. Default value: true

</td></tr><tr><td>

Automatically close project milestone tasks when they change to work state com.snc.project.auto\_close\_milestones

</td><td>

If set to true, this property closes milestones automatically so you do not have to close them manually.Default value: false

</td></tr><tr><td>

Enable altering of planned date\(s\) for task in WIP/Closed com.snc.project.enable\_alter\_of\_planned\_dates

</td><td>

If set to true, this property enables you to change the planned start date for tasks even if they are in the Work in progress state or any of the closed states.Default value: false

</td></tr><tr><td>

Change Resource Plan, Cost Plan and Benefit Plan Start Date with Demand or Project Start Date change. Benefit Plan Start Date will change only if the offset type for the plan is not Nonecom.snc.project.date\_change\_cascade

</td><td>

If set to true, this property changes the start dates for a resource plan, cost plan, and benefit plan when there is a change in the project or demand start dates. **Note:** The start date of benefit plans with the offset type **None** does not change with the project or demand date change.

 Default value: true

</td></tr><tr><td>

Retain users &amp; resource plan state as confirmed / allocated when project movescom.snc.project.date\_change\_cascade\_persist\_resource\_plan\_state

</td><td>

If set to true, this property retains the confirmed or allocated state of a resource plan, booked resources, and planned daily contour when a property is moved. On moving the project, the resource plan is reallocated or reconfirmed based on the availability of the resources in the future time period to which the project is moved.**Note:** This property is enabled only when the **Change Resource Plan, Cost Plan and Benefit Plan Start Date with Demand or Project Start Date Change** property has been set to true.

 Default value: true

</td></tr><tr><td>

Create project\(s\) on confirming demands from portfolio workbench com.snc.project.portfolio\_workbench.confirm\_to\_create\_project

</td><td>

If set to true, this property converts all selected demands in a portfolio to projects.Default value: false

</td></tr><tr><td>

List of attributes \(comma-separated\) that will be copied from the originating project taskcom.snc.project.copy.additional\_attributes

</td><td>

By default, the **Copy Project** and **Copy partial project** options only copy the short description, planned dates, and duration fields from source project to the target project. If additional columns must be copied, they should be declared in this property. Default value: blank

</td></tr><tr><td>

Default the expense type for a new project.sn\_plng\_att\_core.default.expense\_type

</td><td>

When a new project is created in the Project Workspace, expense type of the project is marked as Opex.

</td></tr></tbody>
</table>The following project properties are available in system property \[sys\_properties\] table. Only pps\_admin can edit these properties.

<table id="table_Project-Properties-system-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Retain start on constraint on tasks after adding relations com.snc.project.allow\_start\_on\_relations

</td><td>

The property keeps the **Start on** selection of a task even after you put the task in a relation to another task, for example, FS relation.Default value: true

</td></tr><tr><td>

Max duration \(in days\) allowed for a project/project task com.snc.project.task.max\_task\_duration

</td><td>

The property governs the max duration of a project task or the overall project. **Note:** If your project includes milestones, the duration is calculated taking holidays and weekends into account.

 Default value: 2600

**Warning:** Increasing the value of the property to more than 2600 will have an impact on memory usage of the platform. A very high value causes out of memory error, for example, if you try to create a project or a project task with 15000 days duration.

</td></tr><tr><td>

Max date span into future or past from the current date for the project/project task com.snc.project.task.check\_date\_span\_years

</td><td>

The property governs the max date in future when entering the planned dates of a project or a project task. Default value: 10

**Warning:** Increasing the value of the property to more than 10 will have an impact on memory usage of the platform. A very high value causes out of memory error.

</td></tr><tr><td>

Synchronize the planned and original dates when creating or updating a project or taskcom.snc.project.sync\_original\_dates\_with\_planned\_dates

</td><td>

If set to true, this property synchronizes the planned and original dates.Default value: true

</td></tr><tr><td>

Use a predefined template when generating a status reportsn\_pw.project\_status\_report\_default\_templateId

</td><td>

The property specifies the default template used for generating project status reports. You can replace the existing default template with your desired template and set it as default by updating the sys id in value field of project status report default template property.

</td></tr><tr><td>

Generate the status report as read-onlysn\_pw.doc\_status\_report\_read\_only

</td><td>

The property restrict edits in the status report. The property sets the status report to read-only.Default value: true

</td></tr></tbody>
</table>**Parent Topic:**[Project Management reference](project-management-reference.md)

