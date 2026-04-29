---
title: Create a GRC indicator
description: Create an Indicator to monitor the controls and risks and collect evidence of performance.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Risk Monitoring &amp; Indicators, Audit Management Overview, Audit Management, Governance, Risk, and Compliance]
---

# Create a GRC indicator

Create an Indicator to monitor the controls and risks and collect evidence of performance.

## Before you begin

Role required: compliance\_admin or compliance\_manager, risk\_admin or risk\_manager, audit\_admin or audit\_manager

## Procedure

1.  Navigate to one of the following locations:

    -   **Policy and Compliance** &gt; **Indicators** &gt; **Indicators**.
    -   **Risk** &gt; **Indicators** &gt; **Indicators**.
    -   **Audit** &gt; **Indicators** &gt; **Indicators**.
2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique identification number.

</td></tr><tr><td>

Name

</td><td>

Name of the indicator.

</td></tr><tr><td>

Template

</td><td>

Related indicator template.

</td></tr><tr><td>

Category

</td><td>

Category associated with the Control/Risk that is selected. This field can’t be edited.

</td></tr><tr><td>

Active

</td><td>

Option that determines whether the indicator is active.

</td></tr><tr><td>

Control/Risk

</td><td>

Related control or risk.

</td></tr><tr><td>

Applies to record

</td><td>

Profile related to the **Item**.

</td></tr><tr><td>

Owner

</td><td>

Owner of the indicator.

</td></tr><tr><td>

Owning group

</td><td>

The group that owns the indicator.

</td></tr><tr><td>

Override Template

</td><td>

Option to override the indicator template associated with this indicator

</td></tr><tr><td>

Last result passed

</td><td>

Option that indicates whether the controls were compliant or non-compliant. If the controls were compliant, the check box is selected.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Collection frequency

</td><td>

Collection frequency for indicator results. Indicator tasks and results are generated automatically based on the indicator schedule.

</td></tr><tr><td>

First run date

</td><td>

First collection time for indicator results.This field is automatically set based on when an indicator or an indicator template runs for the first time. The value in this field can’t be modified.

</td></tr><tr><td>

Next run date

</td><td>

Next run time to collect indicator results of all downstream indicators for this indicator template.

</td></tr><tr><td>

Due date duration \(days\)

</td><td>

Due date duration in days between the creation and due date of the indicator task and generation of its results.The due date duration added to the creation date reflects as the **Due date** of the indicator task.

This field appears only when **Manual** is selected from the **Type** field.

For more information, see [Performance enhancements for Indicator nightly job](../../grc-workspace-compliance/concept/performance-enhancements-indicator-jobs.md).

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Method

</td></tr><tr><td>

Type

</td><td>

Results can be gathered manually using task assignment or automatically using basic filter conditions, Performance Analytics, or a script.-   Manual: Used to create an Indicator task for an assignee to complete.
-   Basic: Used to designate whether the indicator identifies the passed or failed controls.
-   Script: Used to write a script to collect the required data.


</td></tr><tr><td>

Short Description

</td><td>

If Type is **Manual**, this field is present. A brief description of the issue.

</td></tr><tr><td>

Instructions

</td><td>

If Type is **Manual**, this field is present. Instructions for the collection of indicator results.

</td></tr><tr><td>

Value Mandatory

</td><td>

If Type is **Manual**, this field is present.

</td></tr><tr><td>

Passed/Failed

</td><td>

If Type is **Basic**, this field is present. The indicator passes or fails.

</td></tr><tr><td>

Script

</td><td>

If Type is **Script**, this field is present. Script that obtains the required system information.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Supporting Data

</td></tr><tr><td colspan="2">

**Note:** Starting with version 10.1, the actual historical data for the supporting data records from the indicator results or indicator tasks is displayed. Earlier, only the real-time state of the records collected could be viewed.

</td></tr><tr><td>

 

</td><td>

 

</td></tr><tr><td>

Table

</td><td>

Use supporting data to gather supporting evidence from other applications.

</td></tr><tr><td colspan="2">

 

</td></tr><tr><td>

Supporting data fields

</td><td>

Supporting data fields based on the selected table.

</td></tr><tr><td>

Criteria

</td><td>

Conditions that must be met for the supporting data.

</td></tr><tr><td>

Sample size

</td><td>

Number of records to select for the supporting data.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Manage GRC key risk and control indicators](../reference/continuous-monitoring.md)

