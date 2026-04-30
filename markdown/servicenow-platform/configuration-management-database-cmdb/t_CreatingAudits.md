---
title: Create a compliance audit
description: Create a compliance audit. Compliance offers two types of audits: one uses templates to define conditions and the other uses a script.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Certification audits, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a compliance audit

Create a compliance audit. Compliance offers two types of audits: one uses templates to define conditions and the other uses a script.

## Before you begin

Role required: certification\_admin

## Procedure

1.  Ensure that an appropriate template record was created for this audit.

    **Note:** Conditions in the template define the values to audit.

2.  Use the CI Class Manager:

    1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

    2.  Select a class from the **Class Hierarchy**.

    3.  In the sidebar, check **Advanced** and then select **Audit** in the **Compliance** group.

3.  Or, navigate to one of these modules:

    -   **All** &gt; **Compliance** &gt; **Audits**
    -   **All** &gt; **Compliance** &gt; **Architecture Compliance** &gt; **Audits**
    -   **All** &gt; **Compliance** &gt; **Desired State** &gt; **Audits**
    -   **All** &gt; **Compliance** &gt; **Scripted Audits** &gt; **Audits**
4.  Select **New**.

    The system opens a new record for the audit type associated with the navigation path you selected. The **Audit type** field is read-only.

5.  Complete the form using the fields described in the table below.

6.  Right-click the header bar and select **Save**.

    The Audit Results and the Follow On Tasks related lists appear on the form.

7.  To run the audit immediately, select **Run Audit**.

    When template audits run, ServiceNow updates the date and time in the **Last run date** field and populates the related lists. For scripted audits, the **Last run date** field is not populated.

8.  View the records that passed and the discrepancies found by the audit in the **Audit Results** related list.

    You can open template records and any follow-on tasks directly from this related list. Notice that the value in the **Task description** field appears as the **Short description** in the follow-on tasks.

    **Note:** You cannot delete audit records that have audit results or audit results that have follow-on tasks. ServiceNow disables the **Delete** option in records and lists where these dependent records exist.

<table id="table_r1l_nm3_dp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for this audit.

</td></tr><tr><td>

Filter

</td><td>

Filter to use when the audit type is Scripted. This field is required for scripted audits, but is hidden for all other audit types.

</td></tr><tr><td>

Template

</td><td>

\[Required\] Template to use when this audit runs. Audit type filters the list of available templates, and only the active versions of templates are available for selection. For example, when you create an audit from Desired State, only templates of the Desired State audit type are available for selection. For the Desired State and Architecture Compliance audit types, only templates for tables that extend the Configuration Item \[cmdb\_ci\] table are available. This field is hidden when the audit type is **Scripted**.

</td></tr><tr><td>

Table

</td><td>

\[Read-only\] Table for the template.

</td></tr><tr><td>

Create tasks

</td><td>

Option to create follow-on tasks for correcting discrepancies \(selected\). In a scripted audit, you can create the logic for either task state by using **true** to create tasks or **false** to not create tasks. By default, this check box is cleared \(**false**\) in a new audit record.

</td></tr><tr><td>

Assignment type

</td><td>

Method for assigning follow-on tasks. This field is visible only when the **Create task** check box is selected. Choices are:-   User Field: Select a user reference field on the table being audited. For example, you choose the user identified in the **Managed by** field on the failed record to perform the tasks. This selection displays the **Assigned to** and **Assign to empty** fields. If the reference field on the record is empty, the value in the **Assign to empty** field is used.
-   Specific User: Select a specific user to perform the tasks. This selection displays the **User** field.
-   Group Field: Select a group reference field on the table being audited. For example, you choose the group identified in the **Support group** field on the failed record to perform the tasks. Tasks are assigned to all members of the group. This selection displays the **Assign to group** and **Assign to empty** fields. If the reference field on the record is empty, the value in the **Assign to empty** field is used.
-   Specific Group: Select a specific group to perform the tasks. This selection displays the **Group** field. All members of the selected group are assigned to the tasks.


</td></tr><tr><td>

User

</td><td>

Specific user this audit assigns to follow-on tasks. This user must have the certification role. This field is available under these conditions:-   Assignment type is set to **Specific User**.
-   Assign to empty is set to **Create Assigned Task**, and **Assignment type** is set to **User Field**.


</td></tr><tr><td>

Assign to group

</td><td>

Group field that defines which group this audit assigns to the follow-on task. This field is available only when the **Assignment type** is **Group Field**.

</td></tr><tr><td>

Group

</td><td>

Specific group this audit assigns to follow-on tasks. This field is available only when the **Assignment type** is **Specific Group**.

</td></tr><tr><td>

Assign to

</td><td>

User field that defines which user this audit assigns to the follow-on task. This field is available only when the **Assignment type** is **User Field**.

</td></tr><tr><td>

Assign to empty

</td><td>

Behavior to use if the field selected in **Assign to** or **Assign to group** is blank on the record being audited. For example, if a follow-on task must be assigned to a manager, but no manager is identified, the **Assign to empty** setting determines what happens. This field appears only when the **Assignment type** is **User Field** or **Group Field**. Choices are:-   Do Not Create Task: No follow-on task is created when the **Assign to** or **Assign to group** field is empty.
-   Create Unassigned Task: Create a follow-on task, but do not assign it to any user or group. The task can be manually assigned later.
-   Create Assigned Task: Create a follow-on task and assign it to the user or group specified. If the assignment type is **User Field**, the **User** field becomes available. If the assignment type is **Group Field**, the **Group** field becomes available.
The audit automatically creates follow-on tasks for all records that have **Assign to** populated, regardless of the **Assign to empty** setting.

</td></tr><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Short description

</td><td>

Brief description of the purpose of the audit.

</td></tr><tr><td>

Task description

</td><td>

General description of the work required for the follow-on tasks for the audit. All follow-on tasks created by this audit inherit this description.

</td></tr><tr><td>

Active

</td><td>

Activation control for this audit record. Clear this check box to prevent this audit from running and creating follow-on tasks.

</td></tr><tr><td>

Run

</td><td>

How often to run the schedule that generates the audit.-   Daily
-   Weekly
-   Monthly
-   Periodically
-   Once
-   On Demand


</td></tr><tr><td>

Day

</td><td>

-   If **Run** is **Weekly**, the day of the week when the audit runs.
-   If **Run** is **Monthly**, the day of the month when the audit runs. If the day is 29, 30 or 31, for shorter months the audit runs on the last day of the month.


</td></tr><tr><td>

Repeat Interval

</td><td>

If **Run** is **Periodically**, the frequency that the audit runs, based on a 24-hr. clock. Enter the number of days between audits and the time of day that you want the audit to run. For example, set **Days** to **10** and **Hours** to **14:00:00** to run the audit every 10 days at 2:00pm.

</td></tr><tr><td>

Starting

</td><td>

If **Run** is **Periodically** or **Once**, the date and time when the audit runs.

</td></tr><tr><td>

Time

</td><td>

If **Run** is **Daily**, **Weekly**, **Monthly**, or **Once**, the time of day, on a 24-hour clock, when the audit runs.

</td></tr><tr><td>

Last run date

</td><td>

\[Read-only\] The last date and time the audit ran, either on its regular schedule or manually. Audit previews do not update this field.

</td></tr><tr><td>

Next scheduled run

</td><td>

\[Read-only\] The next date and time when the audit runs. The system recalculates this field when you change the schedule.

</td></tr><tr><td>

Audit type

</td><td>

\[Read-only\] The type assigned to this audit. The system selects the audit type based on the application from which the audit is created. The type can be:-   Desired State
-   Architecture Compliance
-   Compliance
-   Scripted


</td></tr><tr><td>

Health window

</td><td>

Duration of the evaluation period for threshold and stability. The health window value defines the number of Health window units in an evaluation period for an audit. This value is expressed as a positive integer. The default value for this field is **7**.

</td></tr><tr><td>

Health window unit

</td><td>

Unit of measurement that defines the duration of a health window. The default value for this field is **Days**. Choices are:-   Minutes
-   Hours
-   Days
-   Months


</td></tr><tr><td>

Threshold count

</td><td>

Acceptable number of audit failures for the desired state field that can occur within the specified health window for a CI. The audit results indicate when a desired state field is within or has exceeded this threshold limit. The default value for the threshold is 5.

</td></tr><tr><td>

Stability count

</td><td>

Acceptable number of times that audit results for a CI can switch between **Certified** and **Failed** within the specified health window. The audit results for a CI indicate whether it is stable or unstable. The default value for stability is 1.

</td></tr><tr><td>

Run this script

</td><td>

Audit script to run which contains the conditions that a CI need to comply with to pass the audit. This field is available only when the audit type is **Scripted**. The Audit form includes a sample script with instructions for performing the audit and generating the follow-on tasks.

</td></tr></tbody>
</table>
