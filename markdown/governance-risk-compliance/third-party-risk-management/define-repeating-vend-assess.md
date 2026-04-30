---
title: Configure a risk assessment to recur on a schedule
description: Configure a third-party risk assessment to recur on a schedule to regularly update risk results for a third party or an engagement.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Configure a risk assessment to recur on a schedule

Configure a third-party risk assessment to recur on a schedule to regularly update risk results for a third party or an engagement.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

You can create repeating assessments if you are using the classic assessment engine. You can configure rules that auto-generate and send questionnaires and doc requests to engagements and third parties using the Event-driven management feature if you are using the Smart Assessment Engine. For more information, see [Configure a risk assessment to recur on a schedule](define-repeating-vend-assess.md) and [Event-driven management — automate assessment processes](../../grc-workspace-vrm/task/tprm-event-drvn-mgt-rule-create.md).

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **External Risk Assessments** &gt; **Assessment scheduling**.

2.  Select **New**, fill in the form, and then select **Submit**.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

For each external risk assessment, the system auto-assigns a unique ID number that starts with the text VRA.The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the recurring assessment.

</td></tr><tr><td>

Name

</td><td>

Name of the recurring assessment.

</td></tr><tr><td>

Assessment template

</td><td>

Template used to create the current assessment.

</td></tr><tr><td>

Applies to

</td><td>

The entity to which the assessment applies: **Third party** or **Engagement**.

</td></tr><tr><td>

Third party

</td><td>

Select the third party being assessed.

</td></tr><tr><td>

Engagement

</td><td>

Select the engagement being assessed.

 The field is visible only if you selected **Engagement** in the **Applies to** field.

</td></tr><tr><td>

Active

</td><td>

Option to enable the current recurring assessment to run when scheduled.

</td></tr><tr><td>

Next assessment creation \(months\)

</td><td>

The next assessment will be created in the specified number of months after the previous assessment is closed.

</td></tr><tr><td>

Next assessment end date \(months\)

</td><td>

The end date for the new assessment after the previous assessment is closed.

</td></tr><tr><td>

Assessment results valid duration \(days\)

</td><td>

The number of days that the assessment results are valid.

</td></tr></tbody>
</table>    The Assessment occurrences related list displays the status of each time the assessment took place and the risk rating that resulted from the assessment.


