---
title: Initiate risk assessment on AI asset's risks
description: Request risk assessments for risks identified during the AI system's impact assessment. These risks are generated based on the responses provided during the impact assessment of the AI system.
locale: en-US
release: yokohama
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Initiate risk assessment on AI asset's risks

Request risk assessments for risks identified during the AI system's impact assessment. These risks are generated based on the responses provided during the impact assessment of the AI system.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst

## Procedure

1.  Navigate to **All** &gt; **AI Risk and Compliance** &gt; **AI Risk and Compliance Workspace**.

2.  Select the list ![List icon.](../image/list-icon-airc-ws.png) icon.

3.  From the List, open the AI asset for which you want to request risk assessments.

4.  Navigate to **Risk and compliance posture** &gt; **Risks**.

5.  Select the required risks from the list.

6.  Select **Assess risks**.

7.  On the Request risk assessments dialog box, fill in the fields.

<table id="table_l35_zwl_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assessment methodology

</td><td>

Risk assessment methodology \(RAM\) that you use to assess risks. This is auto-populated based on the published risk RAMs.

</td></tr><tr><td>

Assessor type

</td><td>

Option to select a user or group responsible for assessing the risk. Options are as follows:-   **Same as AI system analyst**: Option to select the AI system analyst as the assessor.
-   **Specify user**: Option to select a user responsible for assessing the risk.
-   **Specify group**: Option to select a group responsible for assessing the risk.


</td></tr><tr><td>

Assessor

</td><td>

Person or group responsible for assessing the risk.**Note:** This field is automatically set to AI system analyst's name, when **Same as AI system analyst** is selected from **Assessor type**.

</td></tr><tr><td>

Approver type

</td><td>

Option to select a user or group responsible for approving the risk assessment. Options are as follows:-   **Specify user**: Option to select a user responsible for approving the risk assessment.
-   **Specify group**: Option to select a group responsible for approving the risk assessment.
-   **None**: Option to select if no specific user or group is assigned for approving the risk assessment.


</td></tr><tr><td>

Approver

</td><td>

Person or group responsible for approving the assessment.**Note:** This field is available only when **Specify user** or **Specify group** is selected from **Approver type**.

</td></tr><tr><td>

Days to overdue

</td><td>

Number of days within which the assessment should be completed after it’s initiated. For example, if you define a value of 10, the due date of the assessment will be set to 10 days after the date the assessment is initiated. The default value is 0.

</td></tr></tbody>
</table>8.  Select **Request assessments**.


## What to do next

[Perform advanced risk assessment in the Risk Workspace](../../grc-workspace-risk/task/perform-ara-workspace.md)

**Parent Topic:**[Using AI Risk and Compliance](../concept/using-ai-risk-and-compliance.md)

