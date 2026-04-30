---
title: Create a control indicator using the Compliance Workspace
description: Indicator data for controls, risk, and audit evidence are measured differently depending on the GRC application.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage control indicators using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a control indicator using the Compliance Workspace

Indicator data for controls, risk, and audit evidence are measured differently depending on the GRC application.

## Before you begin

Role required: sn\_compliance\_admin, sn\_compliance\_manager

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace** &gt; **Control monitoring** &gt; **All indicators**.
    -   **Risk** &gt; **Control monitoring** &gt; **All indicators**.
    -   **Audit** &gt; **Control monitoring** &gt; **All indicators**.
2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

The type of indicator being created. Select **Compliance Indicator** for a control indicator and **Risk Indicator** for a risk indicator.

</td></tr><tr><td>

Inherit from template

</td><td>

Use a selected template to fill in the form.

</td></tr><tr><td>

Template

</td><td>

If you selected the **Inherit from template** check box, select the template you want to use to fill in the form. After you have selected a template, the rest of the fields in the Create New Indicator screen are pre-filled and set to Read-only. For more information, see [Create a GRC indicator template using the Compliance Workspace](create-grc-indicator-template-ws.md).

</td></tr><tr><td>

Override template

</td><td>

If you selected the **Inherit from template** check box, and you want to customize your entries in the form, select this check box. You can then edit some or all of the fields on the form.

</td></tr><tr><td>

Name

</td><td>

Name of the indicator.

</td></tr><tr><td>

Description

</td><td>

A description of this indicator.

</td></tr><tr><td>

Entity

</td><td>

Entity associated with this indicator.

</td></tr><tr><td>

Control

</td><td>

Control associated with this indicator.

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the indicator.

</td></tr><tr><td>

Owner

</td><td>

Indicator owner.

</td></tr><tr class="sub-head"><td colspan="2">

Method

</td></tr><tr><td>

Type

</td><td>

Results can be gathered manually using task assignment or automatically using basic filter conditions, Performance Analytics, or a script.-   Manual
-   Basic
-   Script
For manual indicators, if the associated control is exempt through policy exception, indicator tasks are not generated.

</td></tr><tr><td>

Applies to

</td><td>

Entity related to the **Item**.

</td></tr><tr><td>

Last result passed

</td><td>

Option that indicates whether last result passed.

</td></tr><tr><td>

Short Description

</td><td>

If Type is **Manual**, this field is present. Brief description of the issue.

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

If Type is **Basic**, this field is present. Indicator passes or fails.

</td></tr><tr><td>

PA Threshold

</td><td>

If Type is **PA Indicator**, this field is present. The associated PA Threshold.

</td></tr><tr><td>

Script

</td><td>

If Type is **Script**, this field is present. Script that obtains the desired system information.

</td></tr><tr class="sub-head"><td colspan="2">

Schedule

</td></tr><tr><td>

Collection frequency

</td><td>

Collection frequency for indicator results. Indicator tasks and results are generated automatically based on the indicator schedule.

</td></tr><tr><td>

Next run date

</td><td>

Next collection time for indicator results.

</td></tr><tr class="sub-head"><td colspan="2">

Supporting Data

</td></tr><tr><td colspan="2">

**Note:** Starting with Version 10.1, the actual historical data for the supporting data records from the indicator results or indicator tasks is displayed. Earlier, only the real-time state of the records collected could be viewed.

</td></tr><tr><td>

Table

</td><td>

Use supporting data to gather supporting evidence from other applications.

</td></tr><tr><td>

Supporting data fields

</td><td>

Supporting data fields based on the selected table.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

If you are implementing the [Policy and Compliance Management](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) software, you have completed the mandatory setup steps. Return to the [Policy and Compliance Management setup checklist](../../grc-policy-compliance-implementation/task/policy-compliance-impl-checklist.md) and proceed to the optional steps, as needed.

