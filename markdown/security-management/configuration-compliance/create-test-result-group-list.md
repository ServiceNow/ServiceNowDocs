---
title: Manually create a Configuration Compliance remediation task from the Test Results list
description: You can manually create a remediation task from the Test Result list and perform remediation from the resulting remediation task.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuration Compliance remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Manually create a Configuration Compliance remediation task from the Test Results list

You can manually create a remediation task from the **Test Result** list and perform remediation from the resulting remediation task.

## Before you begin

Role required: sn\_vulc.admin

## About this task

This method requires selecting test results to include and creating the group from the **Actions on selected rows...** menu. This method is good for results that are not easily filtered or situations where you want to specify test results for remediation.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Test Results**.

2.  In the navigation panel, select a Test Result module to open a list.

3.  Select the test results to include in the group by checking the box next to each one.

4.  Open the **Actions on selected rows...** menu at the bottom of the list.

    ![Remediation task from a list](../image/TestResultGroupList.png)

5.  Choose **Create Remediation Task**.

    The remediation task is created and opens.

    ![v10.3 Test result group form](../image/v11TestResultGroupUIAction.png "Test Result Group form")

    The test results you selected for the group are displayed on the Test Results related list along with any associated change requests.

    ![Test Results and Change Requests related lists on new Test Result Group](../image/v11TestResultGroupUIActionbottom.png)

6.  Fill in the fields on the form, as appropriate.

<table id="table_t4d_4bd_5s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-assigned ID in the system.

</td></tr><tr><td>

Score

</td><td>

Auto-populated by risk score rollup calculator.This is a rollup risk score. This risk score is weighted, with 85% of the score from the max risk score across all Test Results not 'Closed' \(Open, Under Investigation, Awaiting Implementation, Deferred, Resolved\), and 15% of the score from the number of test results that are not 'Closed'.

</td></tr><tr><td>

Rating

</td><td>

Auto-populated by risk score rollup calculator. Based on a range of risk scores on a 1-5 numeric scale that rates overall risk based on a range of risk scores as 1 - Critical to 5 - None. This field replaces the Priority field in previous versions.

</td></tr><tr><td>

Historical risk score

</td><td>

Auto-populated by risk score rollup calculator. The inherent risk score across all the passed test results in a remediation task. This field displays the amount of risk that was remediated by a test group and is only displayed after a test group is in the ‘Closed’ state and the risk score is zero.

</td></tr><tr><td>

State

</td><td>

Initially **Open**, is the remediation state of the group. For more information, see [Configuration Compliance states](../concept/vuln-config-compl-states.md).

</td></tr><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Assignment group

</td><td>

Assign the remediation task to a remediation group.

</td></tr><tr><td>

Assigned to

</td><td>

Assign personnel to remediate the group.

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

Text description of this remediation task.

</td></tr><tr><td>

 

</td><td>

Select a Configuration Test for this Remediation Task.

</td></tr><tr><td colspan="2">

**Related tabs**

</td></tr><tr><td>

Group Configuration

</td><td>

Grouping Methods to use:-   Manual \(default\)
-   Filter
 Table: preselected as Test Result

 Test result condition: Choose the filters to use.

**Note:**

The records match condition link above the filter conditions displays the test result records you have chosen in a new window.

 Click **Preview** to see how many results your filter criteria returns before you save the new group.

</td></tr><tr><td>

Notes

</td><td>

Work notes related to this remediation task.

</td></tr><tr><td colspan="2">

**Related lists**

</td></tr><tr><td>

Test results

</td><td>

Test results included in this group.

</td></tr><tr><td>

Change requests

</td><td>

Change requests associated with this group.

</td></tr></tbody>
</table>7.  Right click on the header to **Save** or click **Submit** to save and return to the list of remediation tasks.


**Parent Topic:**[Configuration Compliance remediation](../concept/vuln-config-compl-remediation.md)

