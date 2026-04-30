---
title: Create an Importance and impact tolerance assessment
description: Determine the importance and impact tolerance of a business service by conducting an assessment using either Smart Assessment or Legacy assessment. The assessment questionnaire helps you to measure the service's importance and its impact on customers based on their responses. By evaluating the feedback, you can effectively gauge the significance of your business service and understand its effects on your customers.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Performing Importance and impact tolerance assessment, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create an Importance and impact tolerance assessment

Determine the importance and impact tolerance of a business service by conducting an assessment using either Smart Assessment or Legacy assessment. The assessment questionnaire helps you to measure the service's importance and its impact on customers based on their responses. By evaluating the feedback, you can effectively gauge the significance of your business service and understand its effects on your customers.

## Before you begin

Role required: sn\_oper\_res.user, sn\_oper\_res.manager

## About this task

Operational Resilience Managers \(sn\_oper\_res.manager\) have the Smart Assessment reader role \(sn\_smart\_asmt.assessment\_reader\). They have read-only access to the Smart Assessment template, enabling them to view but not create or edit it.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **List** &gt; **Importance and impact tolerance assessment** &gt; **All assessments**.

    The Importance and impact tolerance assessments \(IIA\) in the Operational Resilience application are displayed in the All assessments list view as shown in the following example.

    ![List view in the All assessments form.](../image/list-view-of-assessments.png "List view in the All assessments form")

2.  To create an assessment, select **New**.

    This action opens an assessment form where you can add the details about the assessment. The system auto-assigns a number for the Importance and impact tolerance assessment, such as IIA0010018.

3.  In the **Name** and **Description** fields, provide a name and description for the assessment.

4.  Select the type of assessment in the **Assessment type** field.

    You can select the following types of assessment in the **Assessment template** field:

    -   Smart Assessment: You can add multiple smart assessment templates for the `Assessment type: Smart assessment` in the **Smart assessment templates** field.
    -   Legacy Assessment: You can add a single assessment template for the `Assessment type: Legacy assessment` in the **Assessment template** field.
<table id="choicetable_ltj_f4q_xfc"><thead><tr><th align="left" id="d159950e176">

Choice

</th><th align="left" id="d159950e179">

Description

</th></tr></thead><tbody><tr><td id="d159950e185">

**Select __Smart assessment__.**

</td><td>

Smart Assessment method for performing the importance and impact tolerance assessment using the Smart Assessment Engine.

 To perform Smart Assessment and measure the importance and impact tolerance, the base version includes the following templates. You can select one or multiple templates:

-   **Importance assessment template**: Use this template to measure the importance of a service.
-   **Impact tolerance assessment template**: Use this template to measure the impact tolerance of a service.
-   **Importance and impact tolerance assessment template**: Use this template to importance and assess the impact tolerance of a service.
**Note:** Templates are provided as demo data only. You can modify the existing templates or use them to create new templates for your specific requirements.

 You can select multiple templates and assign them to different users, enabling for separate assessments. For example, one user can work on the importance assessment and another user can work on the impact tolerance assessment.

 **Note:** To make the desired Smart Assessment templates visible in the drop-down of the IIA form in the Operational Resilience Workspace, ensure that following steps are completed in the Assessment Workspace.

-   Select the necessary template, such as the Importance and impact tolerance assessment template, in the Details section.
-   Choose either the **Importance assessment**, **Impact tolerance assessment**, or **Importance and impact tolerance assessment** category in the **Assessment template categories** field. If you choose a different category, the desired template will not be shown in the Operational Resilience Workspace.
-   Choose **Importance and impact tolerance assessment** as the target in the **Assessment targets** field.
-   To read the assessment, specify the reader role \(sn\_smart\_asmt.assessment\_reader\) as the minimum role in the **Assessment reader role** field of the Settings section.
-   Publish the assessment template.
Only when these conditions are met, the template is available for selection in the drop-down on the IIA form.

 Operational Resilience administrators can edit or create Smart Assessment templates in the base version and update their automation logic to suit the business needs.

 **Note:** For information on setting up Smart Assessment templates, see [Create a Smart Assessment template](../../grc-operational-res/task/create-sm-asmt-temp-as-ws.md) and [Create an assessment template](../../assessment-engine/task/sae-asmnt-template-create.md).

</td></tr><tr><td id="d159950e324">

**Select __Legacy assessment__.**

</td><td>

Legacy assessment method for performing the importance and impact tolerance assessment. For the Legacy assessment, the Importance and Impact Tolerance Template is available with the base version.

 To perform the traditional Legacy assessment, select the Importance and Impact Tolerance Template in the **Assessment template** field.

</td></tr></tbody>
</table>5.  In the Assignees panel, select the owner, approver, and assessor for the assessment.

    **Note:** The approver must be a user other than the owner and assessor.

    For a description of the field values on the Importance and impact tolerance assessment form, see [Create New Importance and impact tolerance assessment form](../reference/importance-and-impact-tolerance-assessment-reference-in-ws.md).

6.  In the **Assessment due date** field under the Milestones panel, select the due date for the assessment.

7.  To reassign the assessment to another assessor, update the **Assessor** field in the **Details** tab.

    This step reassigns all assessment cards to the updated assessor.

    **Note:** Only open assessments can be reassigned to another user; completed assessments remain assigned to the existing assessor. Reassignment is restricted to the assessment owner, requester, or approver. If the assessment is in the **Canceled** state, it does not get reassigned to the updated user.

8.  To start a Sidebar discussion on the assessment, select **More actions** and select **Discuss**.

    1.  Add the subject for the discussion and add participants that have access to the record.

    2.  Include a brief message for the participants.

    3.  Select **Start discussion**.

9.  To delete the assessment, select **Delete**, confirm the deletion, and select **OK**.

10. To save the assessment, select **Save**.

    An assessment is created in the **Draft** state. The details of the assessment are displayed in the assessment form as shown in the following example.

    ![Importance and impact tolerance assessment.](../image/assessment-draft-state-details-panel.png "Importance and impact tolerance assessment")


## What to do next

Add scope for the assessment. For more information, see [Define the scope and begin the assessment](submit-an-assessment-in-ws.md).

