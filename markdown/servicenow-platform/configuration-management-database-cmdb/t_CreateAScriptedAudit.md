---
title: Create a scripted audit
description: A scripted audit is an audit whose conditions are defined by a script.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Scripted audits, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a scripted audit

A scripted audit is an audit whose conditions are defined by a script.

## Procedure

1.  Navigate to **All** &gt; **Compliance** &gt; **Scripted Audits** &gt; **Audits**.

    An audit type of Scripted filters the list.

2.  Click **New**.

3.  Complete the form \(see table\).

4.  Create the audit script.

    The Run this script field includes a sample script with instructions for performing the audit and generating the follow-on tasks. This field appears only when you access audits from the Scripted Audits module.

5.  Click **Submit**.

    Sample script:

    ```
    /*
    /////////////////////////////////////////////////////
    /// This script works with Data Center Zones filter //
    /////////////////////////////////////////////////////
     
    var desiredFloorSpaceUsage = 30;		// Value to audit against
    var assignToUser = '46d44a23a9fe19810012d100cca80666';	 // Beth Anglin
    var assignToGroup = '8a5055c9c61122780043563ef53438e3';	// Hardware group
    var taskMsg = 'See the audit results below for the discrepancies that must be addressed';
     
    // API call to retrieve records based on the filter
    var gr = new SNC.CertificationProcessing().getFilterRecords(current.filter);
     
    // Loop over all records defined by the filter
    while(gr.next()) {
    	var sysId = gr.getValue('sys_id');	// Sys ID of audited record
    	var floorSpaceInUse = gr.getValue('floor_space_in_use');	// Value to audit
     
    	// Determine if certification condition passes or fails
    	if (floorSpaceInUse < desiredFloorSpaceUsage) {
    		var columnNameSpace = gr.floor_space_in_use.getLabel();	// String value of column audited against
     
    		// Call create Follow on Task API and save the returned sys_id for use in logging audit result fail
    		// Params: 
    		// auditId - Sys id of the audit record executed
    		// ciId Sys - id of the configuration item.  Empty string if not a cmdb ci
    		// assignedTo - Sys id of user to assign task to.  Can be empty
    		// assignmentGroup - Sys id of group to assign task to.  Can be empty
    		// shortDescr - Short description for the Follow On Task.  Can be empty
    		// Return value: Sys id of the created follow on task
    		var followOnTask = new SNC.CertificationProcessing().createFollowOnTask(current.sys_id, sysId, assignToUser, '', taskMsg);
     
    		// Call log failed result API
    		// Params:
    		// auditId - Sys id of audit record executed
    		// auditedRecordId - Sys id of the record audited
    		// followOnTask - Sys id of the follow on task associated with the audited record(@see auditedRecordId). Can be empty
    		// columnDisplayName - Label of the column audited(ex. Disk space (GB)).  Can be empty
    		// operatorLabel - Label of the operator used to audit the column(ex. is not empty, greater than). Can be empty
    		// desiredValue - Desired value of the column.  Can be empty
    		// discrepancyValue - Discrepancy value.  Can be empty
    		// isCI - True, if audited record is a CI. False, otherwise.
    		// domainToUse - Sys domain of the "cert_audit" record.  Can be empty
    		new SNC.CertificationProcessing().logAuditResultFail(current.sys_id, sysId, followOnTask, columnNameSpace, 'greater than', desiredFloorSpaceUsage, floorSpaceInUse, true);
    	} else { // If certification condition pass, write a Audit Result Pass via API
    		// Params:
    		// auditId - Sys id of audit record executed
    		// auditedRecordId - Sys id of the record audited
    		// isCI - True, if audited record is a CI. False, otherwise.  Can be empty.
    		// domainToUse - Sys domain of the "cert_audit" record.  Can be empty.
    		new SNC.CertificationProcessing().logAuditResultPass(current.sys_id, sysId, true);
    	}
    }
    */
    ```

<table id="table_pfr_v43_5q"><thead><tr><th>

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

\[Required\] Template to use when this audit runs. Audit type filters the list of available templates and only the active versions of a template are available for selection. This field is hidden when the audit type is Scripted.

</td></tr><tr><td>

Table

</td><td>

\[Read-only\] Displays the table for the template.

</td></tr><tr><td>

Create tasks

</td><td>

Creates follow-on tasks for correcting discrepancies when selected. In a scripted audit, you can create the logic for either task state by using true to create a task or false if no task is created. By default, this check box is cleared \(false\) in a new audit record.

</td></tr><tr><td>

Assignment type

</td><td>

A choice list to select how the audit assigns the follow-on tasks. This field is visible only when the Create task check box is selected. Choices are:

-   User Field: elect a user reference field on the table being audited. As an example, select the user named in the Managed by field on the failed record to perform the tasks. This selection displays the Assigned to and Assign to empty fields. If the reference field on the record is empty, the value in the Assign to empty field is used.
-   Specific User: Select a specific user to perform the tasks. This selection displays the User field.
-   Group Field: Select a group reference field on the table being audited. As an example, select the Support group from the failed record to perform the tasks. This selection displays the Assign to group and Assign to empty fields. All members of the group from the reference field on the failed record are assigned to the tasks. If the reference field on the record is empty, the value in the Assign to empty field is used.
-   Specific Group: Select a specific group to perform the tasks. This selection displays the Group field. All members of the selected group are assigned to the tasks.


</td></tr><tr><td>

User

</td><td>

The specific user this audit assigns to follow-on tasks. This field is available under these conditions:

-   Assignment type is set to Specific User.
-   Assign to empty is set to Create Assigned Task, and Assignment type is set to User Field.
 **Note:** Ensure that the specified user has the [certification role](../../data-certification/reference/r_InstalledWithDataCertification.md).

</td></tr><tr><td>

Assign to group

</td><td>

The group field that defines which group this audit assigns to the follow-on task. This field is available only when the Assignment type is Group Field.

</td></tr><tr><td>

Group

</td><td>

The specific group this audit assign to follow-on tasks. This field is available only when the Assignment type is Specific Group and you have selected Group Field as the assignment type.

</td></tr><tr><td>

Assign to

</td><td>

The user field that defines which user this audit assigns to the follow-on task. This field is available only when the Assignment type is User Field.

</td></tr><tr><td>

Assign to empty

</td><td>

The behavior to use if the field selected in Assign to or Assign to group is blank on the record being audited. For example, if a follow-on task must be assigned to a manager, but no manager is identified, the value in this field determines what happens. This field appears only when the Assignment type is User Field or Group Field. The possible selections are:

-   Do Not Create Task: No follow-on task is created when the Assign to or Assign to group field is empty.
-   Create Unassigned Task: Create a follow-on task, but do not assign it to any user or group. The task can be manually assigned later.
-   Create Assigned Task: Create a follow-on task and assign it to the user or group specified. If you selected an assignment type of User Field, the User field becomes available. If you selected the Group Field type, the Group field becomes available.
 The audit automatically creates follow-on tasks for all records that have Assign to populated, regardless of which selection you make for Assign to empty.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the purpose of the audit.

</td></tr><tr><td>

Task description

</td><td>

General description of the work required for the follow-on tasks created by this audit. All follow-on tasks created by this audit inherit this description.

</td></tr><tr><td>

Active

</td><td>

Activates this audit schedule and generates follow-on tasks at the scheduled date and time. Clear this check box to hide scheduling fields on the form \(except Last run date\) and not generate follow-on tasks.

</td></tr><tr><td>

Run

</td><td>

How often to run the schedule that generates the audit.-   Daily
-   Weekly
-   Monthly
-   Periodically
-   Once
-   On demand


</td></tr><tr><td>

Day

</td><td>

-   If Run is Weekly, the day of the week when the audit runs.
-   If Run is Monthly, the day of the month when the audit runs. If the day is 29, 30 or 31, for shorter months the audit runs on the last day of the month.


</td></tr><tr><td>

Repeat Interval

</td><td>

If Run is Periodically, the frequency that the audit runs entered in time, days, or both. For example, set Days to 10 and Hours to 14:00:00 to run the audit every 10 days at 2:00pm.

</td></tr><tr><td>

Starting

</td><td>

If Run is Periodically or Once, the date and time when the audit runs.

</td></tr><tr><td>

Time

</td><td>

If Run is Daily, Weekly, Monthly, or Once, the time of day, on a 24-hour clock, when the audit runs.

</td></tr><tr><td>

Last run date

</td><td>

\[Read-only\] The last date and time the audit ran, either on its regular schedule or manually. Audit previews do not update this field.

</td></tr><tr><td>

Next scheduled run

</td><td>

\[Read-only\] The next date and time on which the audit runs. The system recalculates this field when you change the schedule.

</td></tr><tr><td>

Audit type

</td><td>

\[Read-only\] The type assigned to this audit. The system selects the audit type based on the application from which the audit was created and can be:-   Desired State
-   Architecture Compliance
-   Compliance
-   Scripted


</td></tr><tr><td>

Run this script

</td><td>

Audit script to run. This field is available only when the audit type is Scripted. The Audit form includes a sample script with instructions for performing the audit and generating the follow-on tasks. See [Script Methods](../reference/r_ScriptMethods.md) for a list of the methods provided and the accepted parameters.

</td></tr></tbody>
</table>
