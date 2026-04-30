---
title: Create new internal assessment form
description: Use the internal assessment form to capture all the information that you need to create an internal assessment. As a third-party risk assessor, you can create an assessment template.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [IRQ process management, Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create new internal assessment form

Use the internal assessment form to capture all the information that you need to create an internal assessment. As a third-party risk assessor, you can create an assessment template.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name that identifies the third-party risk assessment on all forms and lists.

</td></tr><tr><td>

Short description

</td><td>

A more detailed explanation of the purpose of the assessment.

</td></tr><tr><td>

Number

</td><td>

For each external risk assessment, the system auto-assigns a unique ID number that starts with the text VRA.

 The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Applies to

</td><td>

The party to which the assessment applies: **Third party** or **Engagement**.

</td></tr><tr><td>

Third party

</td><td>

Select the third party to assess.**Note:** You can reactivate a third party that is in **Terminated** status. If such a request is accepted and closed, the third party's status is changed to **Active**.

</td></tr><tr><td>

Engagement

</td><td>

Select the engagement to assess. The field is visible only if you selected **Engagement** from the **Applies to** field.

</td></tr><tr><td>

Due diligence request

</td><td>

If there’s an existing due diligence request associated with this assessment, it’s listed here.

</td></tr><tr><td>

Assessment Engine

</td><td>

The assessment engine used for the Third-party risk assessment. This field is set to **Smart**.

This field is only visible if you have enabled the Smart Assessment Engine enabled \[`sn_vdr_risk_asmt.sae_enabled`\] property. For more information about this property, see [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

**Note:** When reviewing previous assessments, you can determine which engine was used by checking this field. If the assessment was created using the Classic assessment engine, the field displays **Classic**.

</td></tr><tr><td>

State

</td><td>

Current stage of the internal assessment process.

</td></tr><tr><td>

Assigned to

</td><td>

The individual who owns an assessment for audit purposes and monitors and manages overall assessment processes. The owner is responsible for confirming that the assessment is completed in a timely fashion by the third party, reviewing their responses, and creating and resolving issues. To drive the assessment to its completion, they are notified when an assessment reaches a particular milestone. They must have the TPR manager or TPR assessor role.

</td></tr><tr><td>

Risk rating

</td><td>

The overall risk rating for the third party. -   Critical
-   High
-   Moderate
-   Low
-   Minor

**Note:** The **Risk rating** is determined by finding a risk rating scale range in which the risk score falls. It defines how a minimum and maximum range of assessment scores maps to a qualitative risk score.

</td></tr><tr><td>

Respondents

</td><td>

Individual who is assigned to respond to the internal assessment. Multiple respondents can be assigned to an internal assessment.

</td></tr><tr><td class="sub-head" colspan="2">

**Assessment Schedule**

</td></tr><tr><td>

Planned duration \(days\)

</td><td>

Estimated duration of the assessment.**Note:** This estimate includes the amount of time needed to receive responses and for internal and external users to review.

</td></tr><tr><td>

Planned start date / Planned end date

</td><td>

Planned start and completion dates and times for work on the assessment.**Note:** The **Planned end date** is automatically set to one month from the **Planned start date**. After the assessment is saved, this date can’t be changed.

</td></tr><tr><td>

Actual duration

</td><td>

The amount of time it took to complete the third-party risk assessment. This field is calculated using the **Actual state date** and **Actual end date**.

</td></tr><tr><td>

Actual start date

</td><td>

Date and time that work on the assessment began.

</td></tr><tr><td>

Actual end date

</td><td>

Completion date and time for the assessment.

</td></tr><tr><td class="sub-head" colspan="2">

**Notes and Comments**

</td></tr><tr><td>

Work notes

</td><td>

Information about the assessment. Work notes are visible to users assigned to the issue.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Public information about the assessment.

</td></tr></tbody>
</table>**Parent Topic:**[IRQ process management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-irq-tab.md)

**Related topics**  


[Create an external assessment template](../task/create-vendor-risk-assess-temp.md)

