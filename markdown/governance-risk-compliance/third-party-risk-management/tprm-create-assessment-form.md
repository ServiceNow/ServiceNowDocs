---
title: Third-party risk assessment form
description: Use the third-party risk assessment form to capture all the information that you need to create an assessment using the Third-party Risk Management application. As a third-party risk assessor or manager, you can create an external assessment.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Third-party \(external\) risk assessment management, Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Third-party risk assessment form

Use the third-party risk assessment form to capture all the information that you need to create an assessment using the Third-party Risk Management application. As a third-party risk assessor or manager, you can create an external assessment.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name that identifies the third-party risk assessment on all forms and lists.

</td></tr><tr><td>

Description

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

The party to which the assessment applies: **Third party**, **Engagement**, **Entity**.

</td></tr><tr><td>

Third party

</td><td>

The assessed third party.**Note:** You can reactivate a third party that is in **Terminated** status. If such a request is accepted and closed, the third party's status is changed to **Active**.

</td></tr><tr><td>

Engagement

</td><td>

Select the engagement to assess. The field is visible only if you selected **Engagement** from the **Applies to** field.

</td></tr><tr><td>

Entity

</td><td>

Select the entity to assess. The field is visible only if you selected **Entity** from the **Applies to** field.**Note:** This is an entity record created as part of the third-party element collection process. For more information, see [Monitoring third-party elements](../concept/tprm-monitor-tp-elements.md).

</td></tr><tr><td>

Repeating assessment

</td><td>

The assessment used to create the current assessment.**Note:** You can create repeating assessments if you’re using the classic assessment engine. You can configure rules that auto-generate and send questionnaires and doc requests to engagements and third parties using the Event-driven management feature if you’re using the Smart Assessment Engine. For more information, see [Configure a risk assessment to recur on a schedule](../task/define-repeating-vend-assess.md) and [Event-driven management — automate assessment processes](../../grc-workspace-vrm/task/tprm-event-drvn-mgt-rule-create.md).

</td></tr><tr><td>

Assessment template

</td><td>

Select an assessment template to create questionnaires or document requests for this assessment.

 To use multiple templates to create multiple questionnaires or document requests for the assessment, leave the field empty.

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

The process of collecting assessment data from a third party transitions through several states. See [Life cycle states of a external assessment](../concept/tprm-external-assessment-lifecycle.md) for detailed descriptions.

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

Risk rating valid to

</td><td>

The date the risk rating expires. The date must be later than the **Risk rating valid to** date on any associated questionnaires or document requests.

</td></tr><tr><td>

Trigger by third-party tier

</td><td>

Select the check box to initiate the assessment when the risk tier changes for the third party.

</td></tr><tr><td>

Assigned to

</td><td>

The individual who owns an assessment for audit purposes and monitors and manages overall assessment processes. The owner is responsible for confirming that the assessment is completed in a timely fashion by the third party, reviewing their responses, and creating and resolving issues. To drive the assessment to its completion, they are notified when an assessment reaches a particular milestone. They must have the TPR manager or TPR assessor role.

</td></tr><tr><td>

Watch list

</td><td>

Add users that should be notified when this record is modified.

</td></tr><tr><td class="sub-head" colspan="2">

**Risk Scoring** **Note:** Risk ratings are calculated and displayed after assessment responses have been received.

</td></tr><tr><td>

Computed risk rating

</td><td>

Average of the third-party risk area risk ratings.

</td></tr><tr><td>

Issue risk rating

</td><td>

The risk rating for issues associated with the third parties being assessed. The issue risk rating is based on the priority of closed issues and how they were resolved. -   If the issue was **Closed Completed**, it indicates that the issue was resolved.
-   If the issue was **Closed Incomplete**, it indicates that the third party failed to complete the associated questions.
-   If the issue was **Closed Cancelled**, it indicates that the issue didn’t need to be resolved.

If the issue is closed and the **State** of the assessment isn’t closed or canceled, the **Issue risk rating** is recalculated and displayed.**Note:** The **Computed risk rating** isn’t affected by this calculation.

</td></tr><tr><td>

Override risk rating

</td><td>

Option to override the computed risk rating for the third party. When selected, any future changes made to the assessment risk rating affects only the computed risk rating, not the risk rating. **Note:** If the check box is selected and then deselected, the computed risk rating is used.

</td></tr><tr><td>

Overridden risk rating

</td><td>

Risk rating to override the current computed risk rating.If you selected **Override risk rating**, enter the new risk rating.

</td></tr><tr><td>

Justification

</td><td>

Justification for overridden risk rating.If you selected **Override risk rating**, you must enter a reason for the override.

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

**Questionnaire Schedule**

</td></tr><tr><td>

Planned duration \(days\)

</td><td>

The amount of time given to the third party or engagement to complete all questionnaires.

</td></tr><tr><td>

Review duration \(days\)

</td><td>

Time allocated for the Assessment reviewer to review all questionnaires.**Note:** Users with the Third-party assessment reviewer \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] role can review and leave comments for the following:

-   Tiering assessments
-   Internal assessments
-   External assessments
-   Third-party risk issues
-   Third-party risk tasks
-   Third-party risk due diligence requests

</td></tr><tr><td>

Submitted to third party

</td><td>

Delivery date for third party questionnaires.

</td></tr><tr><td>

Due date

</td><td>

Deadline for third party to respond to and return all questionnaires.**Note:** The **Due date** is set to a duration of 10 days by default. You can extend the due date of a questionnaire by increasing the **Planned duration \(days\)**; however, the **Planned end date** of the assessment won’t be updated.

</td></tr><tr><td>

Completion date

</td><td>

Actual date when third party completed all questionnaires.

</td></tr><tr><td>

Responses expected by

</td><td>

The date that your organization expects the responses to be returned by the third-party contact.

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
</table>**Parent Topic:**[Third-party \(external\) risk assessment management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-extrnl-assessment.md)

**Related topics**  


[Assessing your third-party risk](../concept/tprm-assessing-tpr.md)

