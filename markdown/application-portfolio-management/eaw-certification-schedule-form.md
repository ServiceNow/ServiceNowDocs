---
title: Certification schedule form in Enterprise Architecture Workspace
description: A system administrator with Enterprise Architecture \(formerly APM\) admin role can create and assign data certification tasks to the system owners for certifying business application data.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Certification schedule form in Enterprise Architecture Workspace

A system administrator with Enterprise Architecture \(formerly APM\) admin role can create and assign data certification tasks to the system owners for certifying business application data.

## Certification Schedule form fields

<table id="table_lns_kjg_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the certification schedule.

</td></tr><tr><td>

Filter

</td><td>

Select a filter for the table data.

</td></tr><tr><td>

Table

</td><td>

The table consisting the data that is to be certified. Defaults to cmdb\_ci\_business\_application table.

 **Note:** Data certification can be applied only on one table at a time. Create another table if you require data certification on that table.

</td></tr><tr><td>

Display fields

</td><td>

Select the fields to be displayed from the business application.

 **Note:** Display fields can’t be the same as Certification fields. They’re mutually exclusive.

</td></tr><tr><td>

Certification fields

</td><td>

Select fields to be displayed that require individual field certification. Specify the fields that you want to be certified.**Application URL**, **Business criticality**, **Data classification**, **Contract end date**, **Active**, **Active user count**, **Status**, **User base**, and **Last change applied date** are some of the fields preconfigured for data certification.

</td></tr><tr><td>

Assignment type

</td><td>

Select a user reference field from the target table.

 -   **User field**: Select and assign a specific field in the Business application table in the **Assign to** field.
-   **Specific User**: Select and assign a specific user in the **User** field.
-   **Group Field**: Assign the certification schedule to a group in the **Assign to group** field.
-   **Specific Group**: Select and assign the certification schedule to a group in the **Group** field.

</td></tr><tr><td>

Assign to

</td><td>

Owner of the application who is responsible for certifying the data of the business application.

</td></tr><tr><td>

User

</td><td>

Select a user to whom all the unassigned tasks will be assigned to.

</td></tr><tr><td>

Assign to group

</td><td>

Select a group from the business application table.

</td></tr><tr><td>

Group

</td><td>

Select a group from the list.

</td></tr><tr><td>

Assign to empty

</td><td>

Select a value from the list:

-   **Do Not Create Task**: Certification task is not created for these records.
-   **Create Unassigned Task**: Certification task is created but is unassigned.
-   **Create Assigned Task**: Certification task is created and assigned to the specific user or group.

**Note:** The field is available only when you select the **Assignment type** as **User Field** or **Group Field**.

</td></tr><tr><td>

Days to complete

</td><td>

Enter the number of days by which you require the certification to be completed.

</td></tr><tr><td>

Active

</td><td>

The job is inactive by default. Select the check box to run the scheduled job.

</td></tr><tr><td>

Run

</td><td>

Frequency with which the certification task is performed: Daily, Weekly, Monthly, Periodically, Once, On Demand.

</td></tr><tr><td>

Last run date

</td><td>

Defaults to the prior date when the certification was run. The field cannot be edited if the certification schedule is a new record.

</td></tr><tr><td>

Task description

</td><td>

Brief description of the certification task.

</td></tr><tr><td>

Instructions

</td><td>

Detailed instruction to the application owner about the task.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Number|Number of the certification instance.|
|Certification Schedule|Defines the information that requires certification and the frequency of execution. Defaults to the certification schedule that you selected.|
|State|Status of the certification: **Work in Progress** or **Complete**.|
|Created|Created date of the certification instance.|
|Complete by|The date on which the certification task is to be completed. **Days to complete** is added to the **Created** date.|
|Percent complete|For each field \(out of the total number of certification fields\) that the application owner certifies the percent is calculated. The system administrator can track the progress of the data certification task.|
|Short description|Brief description of the certification instance.|

|Field|Description|
|-----|-----------|
|Number|Number assigned to the certification task.|
|Assigned to|Owner of the application to whom the task is assigned and who is authorized to certify the data.|
|Assignment group|Task can also be assigned to users of a group.|
|Escalation|Defaults to Normal.|

**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Add or edit a certification policy](../../task/eaw-task/eaw-manage-cert-schedules.md)

[Manage certification policies](../../concept/eaw-concept/eaw-config-cert-schedules.md)

