---
title: Manually create a Configuration Compliance remediation task
description: You can manually create a remediation task from the Remediation Tasks module and perform remediation.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuration Compliance remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Manually create a Configuration Compliance remediation task

You can manually create a remediation task from the **Remediation Tasks** module and perform remediation.

**Important:** You can create remediation tasks in the:

-   Vulnerability Manager Workspace as a user with the sn\_vulc.admin role.
-   IT Remediation Workspace as a user with sn\_vulc.remediation\_owner role.

## Before you begin

Role required: sn\_vulc.admin

## About this task

Using remediation task rules automatically populates the **Test Results** tab. Manual creation is useful for a group that doesn't need a rule or to be repeated.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Remediation Tasks**.

2.  In the navigation panel, click on **My Open Tasks** or **All Open Tasks** to view the list.

3.  Click **New**.

    ![Test result group form](../image/v11TestResultGroupNewForm.png "Remediation task form")

4.  Fill in the fields on the Remediation Task form, as appropriate.

<table id="table_t4d_4bd_5s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-assigned ID in the system.

</td></tr><tr><td>

Risk score

</td><td>

Auto-populated by risk score calculator.This is a rollup risk score. This risk score is weighted, with 85% of the score from the max risk score across all Test Results not 'Closed' \(Open, Under Investigation, Awaiting Implementation, Deferred, Resolved\), and 15% of the score from the number of test results that are not 'Closed'.

</td></tr><tr><td>

Risk rating

</td><td>

Auto-populated by risk score calculator. Based on a range of risk scores on a 1-5 numeric scale that rates overall risk based on a range of risk scores as 1 - Critical to 5 - None. This field replaces the Priority field in previous versions.

</td></tr><tr><td>

State

</td><td>

Initially **Open**, is the remediation state of the group. For more information, see [Configuration Compliance states](../concept/vuln-config-compl-states.md).

</td></tr><tr><td>

Assignment group

</td><td>

Assign the remediation task to a remediation group.

</td></tr><tr><td>

Assigned to

</td><td>

Assign personnel to remediate the remediation task.

</td></tr><tr><td>

Created

</td><td>

Date you created this group.

</td></tr><tr><td>

Updated

</td><td>

Date you updated this group.

</td></tr><tr><td>

Short Description

</td><td>

Name of the remediation task.

</td></tr><tr><td>

Description

</td><td>

Description of this remediation task.

</td></tr><tr><td>

Test

</td><td>

Select a Configuration Test for this Remediation Task.

</td></tr><tr><td colspan="2">

**Related tabs**

</td></tr><tr><td>

Group Configuration

</td><td>

Grouping Methods to use:-   Manual \(default\):
-   Filter or Group Rule:
 Table: preselected as Test Result \[sn\_vulc\_result\]

 Test result condition: Choose the filters to use.

**Note:**

The records match condition link above the filter conditions displays the test result records you have chosen in a new window.

 Click **Preview** to see how many results your filter criteria returns before you save the new group.

 The Test Results related list must be created manually by clicking the **Edit** button in the **Test Results** related tab.

</td></tr><tr><td>

Notes

</td><td>

Work notes related to this remediation task.

</td></tr></tbody>
</table>5.  Right click in the header to **Save** or click **Submit** to save and return to the list of remediation tasks.

    Displays the **Test Results** and **Change Request** related lists.

    ![Test result group related tab](../image/TestResultGroupRelatedTab.png)


**Parent Topic:**[Configuration Compliance remediation](../concept/vuln-config-compl-remediation.md)

