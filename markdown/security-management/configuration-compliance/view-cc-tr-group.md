---
title: View a remediation task
description: You can view, or, alternatively, create a remediation task and perform remediation.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Reference, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# View a remediation task

You can view, or, alternatively, create a remediation task and perform remediation.

**Important:** You can view the remediation tasks in the Vulnerability Manager Workspace. For more information, see [List page in the Vulnerability Manager Workspace](../../vr-vulnerability-manager-workspace/concept/vmws-list-page.md).

## Before you begin

Role required:

-   sn\_vulc.admin to update or create
-   sn\_vulc.remediation\_owner to view

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Remediation Tasks**.

2.  From the list, click the record you want to view.

3.  Alternatively, click **New** to create a new remediation task and fill in the fields.

<table id="table_j1g_qpc_m1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically generated number for this record.

</td></tr><tr><td>

State

</td><td>

Progress status of the remediation task.-   Open
-   Under investigation
-   Awaiting Implementation
-   Deferred
-   Resolved
-   Closed


</td></tr><tr><td>

Risk score

</td><td>

This score is the rolled-up value of the risk scores for all the active test results in a remediation task. This score changes as test results are remediated in the remediation task.

</td></tr><tr><td>

Assignment group

</td><td>

Group selected to work on this remediation task.

</td></tr><tr><td>

Risk rating

</td><td>

The amount of risk a failed test result poses to your system. It is based on a range of risk scores on a 1-5 numeric scale that rates risks as Critical \(1\) to None \(5\).

</td></tr><tr><td>

Assigned to

</td><td>

Individual from the selected assignment group that works on this set of tasks.

</td></tr><tr><td>

Remediation target

</td><td>

Date by which the test results should be remediated, since first identified.

</td></tr><tr><td>

Created

</td><td>

The date and time this remediation task was created.

</td></tr><tr><td>

Remediation status

</td><td>

Status of the remediation for the group. It is determined by the test result with the nearest due date.

For open groups states include In-flight, Approaching Target and Target Missed. For closed groups states include No Target, Target Met and Target Missed.For calculated remediation target dates, if the remediation task is closed, the overall remediation status of all of the closed test results is shown in the remediation task. Those determine whether the group met its date or not.

A closed remediation task remediation Status is **No Target** if none of its closed results had a remediation target date. It is **Target Missed** if any of its closed results missed their target date. It is **Target Met** if at least one closed result met its target and none of the others missed it.

</td></tr><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Updated

</td><td>

The date and time this record was last modified.

</td></tr><tr><td>

Short description

</td><td>

Brief description of this remediation task.

</td></tr><tr><td>

Description

</td><td>

Long description of the remediation task that includes the list of software associated with this remediation task.

</td></tr><tr><td>

Test

</td><td>

The configuration test associated with this remediation task.

</td></tr><tr><td colspan="2">

**Remediation Status \(Version 12.0\)**

</td></tr><tr><td>

Excludes Deferred

</td><td>

These values do not include deferred test results.

 -   **Open test results**: The number \(count\) of active \(any state other than **Closed**\) test results for this remediation task.
-   **% Test results remediated**: The percent of remediated \(closed\) test results for this remediation task.
-   **Total test results**: The total number of test results for this remediation task.


</td></tr><tr><td>

Includes Deferred

</td><td>

The values represent all active test results \(any state other than **Closed**\).

-   **Open test results**: The number \(count\) of active \(any state other than **Closed**\) test results for this remediation task.
-   **% Test results remediated**: The percent of remediated \(closed\) test results for this remediation task.
-   **Total test results**: The total number of test results for this remediation task.


</td></tr><tr><td>

**Group Configuration**

</td><td>

The type of filtering used to select the test results for the remediation task.

</td></tr><tr><td>

Grouping method

</td><td>

Name of method used.

</td></tr><tr><td>

Group rule

</td><td>

Name of the group rule used.

</td></tr><tr><td>

**Notes**

</td><td>

System notes associated with the record.

</td></tr><tr><td>

**Related Links**

</td><td>

**Version 12.0: Update status link**. Update the values on the test result record on-demand. View any data that has changed or been updated since the last scheduled job.

</td></tr><tr><td>

Test Results

</td><td>

The test results in this remediation task.

</td></tr><tr><td>

**Change requests \(v 12.0\)**

</td><td>

The list of change requests associated with this remediation task.

</td></tr><tr><td>

**State Change Approvals \(v 12.0\)**

</td><td>

Status and states of change request approvals associated with this remediation task.

</td></tr></tbody>
</table>
