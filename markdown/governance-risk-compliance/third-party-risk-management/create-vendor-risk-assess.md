---
title: Create an external assessment — Legacy process
description: Create an assessment and initiate the third-party risk assessment life cycle. An external assessment specifies the details for the third party or engagement and defines the plan for completing the assessment.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Work in the VRM classic UI, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create an external assessment — Legacy process

Create an assessment and initiate the third-party risk assessment life cycle. An external assessment specifies the details for the third party or engagement and defines the plan for completing the assessment.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager or sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

Assessments can be created on-demand or can recur on a specified schedule. When creating an on-demand external assessment, TPR managers select the questionnaire template or document request template and the third party. TPR managers can select multiple third parties at a time and automatically trigger assessments.

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **External Risk Assessments** &gt; **All Assessments**.

2.  Select **New** and then fill in the fields.

    ![Vendor Risk Assessment form.](../image/vendor-risk-assessment.png)

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

A more detailed explanation of the issue.

</td></tr><tr><td>

Number

</td><td>

For each external risk assessment, the system auto-assigns a unique ID number that starts with the text VRA.

 The unique ID is used in all references to the item. You can use the ID to search or filter for the item that you want to work on.

</td></tr><tr><td>

Applies to

</td><td>

The entity to which the assessment applies: **Third party** or **Engagement**.

</td></tr><tr><td>

Vendor

</td><td>

The assessed third party.**Note:** You can reactivate a third party that is in **Terminated** status. If such a request is accepted and closed, the third party's status is changed to **Active**.

</td></tr><tr><td>

Engagement

</td><td>

Select the engagement to assess. The field is visible only if you selected **Engagement** from the **Applies to** field.

</td></tr><tr><td>

Repeating assessment

</td><td>

The assessment used to create the current assessment. **Note:** You can create repeating assessments if you are using the classic assessment engine. You can configure rules that auto-generate and send questionnaires and doc requests to engagements and third parties using the Event-driven management feature if you are using the Smart Assessment Engine. For more information, see [Configure a risk assessment to recur on a schedule](define-repeating-vend-assess.md) and [Event-driven management — automate assessment processes](../../grc-workspace-vrm/task/tprm-event-drvn-mgt-rule-create.md).

</td></tr><tr><td>

Assessment template

</td><td>

Select an assessment template to create questionnaires or document requests for this assessment.

 To use multiple templates to create multiple questionnaires or document requests for the assessment, leave the field empty.

</td></tr><tr><td>

Owner

</td><td>

The individual who owns an assessment for audit purposes and monitors and manages overall assessment processes. The owner is responsible for confirming that the assessment is completed in a timely fashion by the third party, reviewing their responses, and creating and resolving issues. To drive the assessment to its completion, they are notified when an assessment reaches a particular milestone. They must have the TPR manager or TPR assessor role.

 For new requests, if the **Owner** field is empty, then the following action happens: The system sends an email notification to all users in the group that is specified in the **Assignment group**. The message states that the request was received and is in the **New** state. The message also includes a link to the details page for the request. See [Add users to groups based on responsibilities](../../grc-vendor-risk-implementation/task/tprm-groups-add-users-to.md).

 **Note:** If the **Owner** field is empty and you select **Start the IRQ process**, then you become the owner.

</td></tr><tr><td>

Assignment group

</td><td>

For new requests, the **Assignment group** is set to **Due diligence request assigners**. The system sends an email notification to all users in the group that is specified in the **Assignment group**. The message states that the request was received and is in the **New** state. The message also includes a link to the details page for the request.

 On the due diligence request form:

 -   Any member of the group can select **Assign to me** or set the **Owner** field to any other member of the group.
-   A TPR manager or TPR assessor can clear the **Assignment group** field or change the value to select from different TPR assessors in the **Owner** selection list.


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

Risk rating valid until

</td><td>

The date the risk rating expires. The date must be later than the **Risk rating valid to** date on any associated questionnaires or document requests.

</td></tr><tr><td>

Trigger by risk tier

</td><td>

Select the check box to initiate the assessment when the risk tier changes for the third party.

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

Override risk rating

</td><td>

Select the check box to override the computed risk rating for the third party. When selected, future changes to the assessment risk rating will affect only the computed risk rating, not the risk rating. **Note:** If you deselect a selected check box, then the computed risk rating is copied to the assessment.

</td></tr><tr><td>

Overridden risk rating

</td><td>

If you selected **Override risk rating**, enter the new risk rating.

</td></tr><tr><td>

Justification

</td><td>

If you selected **Override risk rating**, you must enter a reason for the override.

</td></tr><tr><td>

Issue risk rating

</td><td>

The risk rating for issues associated with the third parties being assessed. The issue risk rating is based on the priority of closed issues and how they were resolved. -   If the issue was **Closed Completed**, it indicates that the issue was resolved.
-   If the issue was **Closed Incomplete**, it indicates that the third party failed to complete the associated questions.
-   If the issue was **Closed Cancelled**, it indicates that the issue didn’t need to be resolved.
If the issue is closed and the **State** of the assessment isn’t closed or cancelled, the **Issue risk rating** is recalculated and displayed.**Note:** The **Computed risk rating** isn’t affected by this calculation.

</td></tr><tr><td>

Override risk rating

</td><td>

Option to override the computed risk rating for the third party. When selected, any future changes made to the assessment risk rating will affect only the computed risk rating, not the risk rating. **Note:** If the check box is selected and then deselected, the computed risk rating is used.

</td></tr><tr><td>

Overridden risk rating

</td><td>

If you selected **Override risk rating**, enter the new risk rating.

</td></tr><tr><td>

Justification

</td><td>

If you selected **Override risk rating**, you must enter a reason for the override.

</td></tr><tr><td class="sub-head" colspan="2">

**Assessment Schedule**

</td></tr><tr><td>

Planned duration \(days\)

</td><td>

Estimated duration of the assessment

</td></tr><tr><td>

Planned start date / Planned end date

</td><td>

Planned start and completion dates and times for work on the assessment.

</td></tr><tr><td>

Created by

</td><td>

User who created this record.

</td></tr><tr><td>

Created

</td><td>

Date/time the record was created.

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

</td></tr><tr><td>

Updated

</td><td>

Date/time when the record was last updated.

</td></tr><tr><td class="sub-head" colspan="2">

**Questionnaire Schedule**

</td></tr><tr><td>

Planned duration \(days\)

</td><td>

The amount of time given to the third party to complete the assessment. The value is calculated using the **Planned state date** and **Planned end date**.

</td></tr><tr><td>

Review duration \(days\)

</td><td>

Time allocated for the customer to review all questionnaires.

</td></tr><tr><td>

Due date

</td><td>

Deadline for third party to respond to and return all questionnaires.

</td></tr><tr><td>

Completion date

</td><td>

Actual date when third party completed all questionnaires.

</td></tr><tr><td>

Submitted to third party

</td><td>

Delivery date for third party questionnaires.

</td></tr><tr><td>

Resubmitted to third party

</td><td>

Date that questionnaires are resent to the third party.

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
</table>3.  Save the record.

    Additional related lists appear. If you left the **Assessment template** field empty and want to use assessment templates to associate multiple questionnaires and/or document requests with this assessment, use the Questionnaires or Document Requests related lists.

    ![Several related lists appear when you save the Vendor Risk Assessment form.](../image/assessment-related-lists.png)

4.  To associate existing questionnaires and/or document requests with the assessment, perform the following steps.

    1.  Open the Questionnaires or Document Requests related list.
    2.  Select **Edit**, select the questionnaires or document requests to use, and then select **Save**.
    3.  Repeat for the other type of questions, if needed.
5.  To create new questionnaire and/or document request templates and associate them with the assessment, see [Create a questionnaire or document request template](create-questionnaire-template.md).

    **Important:** In the next step, you can choose to submit the questionnaire to the third party. To pre-populate the questionnaire with responses from the most recently closed assessment, you must select the **Include previous responses** option before you submit it to the third party. The setting cannot be changed after the questionnaire is sent to the third party. See [Create a questionnaire or document request template](create-questionnaire-template.md).

6.  Select **Submit to third party**.

    -   The state of the assessment changes to **Submitted to third party**.
    -   The templates that you selected generate questionnaires and/or document requests.
    -   If the **Include previous responses** option is selected for a questionnaire, then previous responses are copied and added to the outgoing questionnaire. The notification in the Third-party portal includes the number, name, and closing date of the assessment that supplied the responses. The notification also includes a link to the assessment.
    -   The primary third-party contact receives an email notification that includes a link to the assessment in the Third-party portal.

        **Note:** When you use the **Include previous responses** option, responses are copied from Assessment A to Assessment B one time. Any changes you make to Assessment A afterward won't be reflected in Assessment B. Both assessments remain separate.

7.  When the third-party contact is ready to respond to the assessment, they open the assessment in the Third-party portal.

    ![Working with an assessment in the third-party portal.](../image/portal-updated-assess.png)

    **Note:** In the example, one of the questionnaires requires a signature. The third party or reviewer must save and e-sign the questionnaire or document request before it can be submitted. For more information, see [E-signatures on questionnaires or document requests](../../grc-workspace-vrm/task/tprm-ws-approve-with-e-sig.md).

8.  The TPR assessor moves the state of the assessment to **Generating Observations**.

    During this time, the TPR assessor can select the **View Response** link in the Document Requests or Questionnaires related list to view the response and provide comments or change responses, as necessary.

    For any problems that arise, the TPR assessor creates an issue to track the remediation process \(Finalizing with third party\).

9.  The TPR assessor moves the assessment to **Closed** state.


## What to do next

The TPR assessor works through the third-party portal with the third party to close the assessment.

![Vendor risk assessment life cycle.](../image/vrm-workflow.png)

