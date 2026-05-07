---
title: Performing Importance and impact tolerance assessment
description: By analyzing the importance and the impact tolerance of your business service or service offering, you can measure how possible disruptions might impact the performance of a service. You can use the assessment questionnaire template​ in Operational Resilience Workspace to measure the importance and the impact tolerance of your selected business service and its child records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Performing Importance and impact tolerance assessment

By analyzing the importance and the impact tolerance of your business service or service offering, you can measure how possible disruptions might impact the performance of a service. You can use the assessment questionnaire template​ in Operational Resilience Workspace to measure the importance and the impact tolerance of your selected business service and its child records.

## Importance and impact tolerance of a business service

A business service's importance is determined by such factors as the number of customers that use the service, the revenue that the service generates, and its impact on your company's brand. By measuring the impact tolerance of a business service, you can see how long a service can be non-operational without causing some kind of loss to the business and its customers. Previously, we had only one Impact Tolerance that provided a value in terms of Duration. Now, we have four types of Impact Tolerance fields on the form:

-   Impact Tolerance \(Duration\)
-   Impact Tolerance \(Customer Impact\)
-   Impact Tolerance \(Financial Impact\)
-   Impact Tolerance \(Transaction Volume\)

If you have the sn\_oper\_res.admin role, you can create and maintain a pre-defined assessment template in Operational Resilience. With the sn\_oper\_res.manager role, you can select one or more business services that you want to analyze and use the assessment template to calculate the importance and the impact tolerance​ of your business services.

## Using Smart Assessment to evaluate importance and impact tolerance of a service

Beginning with Operational Resilience, release 21.x.x, the Smart Assessment functionality has been integrated with the Importance and impact tolerance assessment, enabling you to create and manage the Importance and impact tolerance assessments efficiently. It includes features such as an assessment type field with legacy and smart options, default templates, and automated data updates. To progress, all assessments must be completed, after which they become read-only and are ready for approval.

The system requires assessments to be completed, as cancellations are not supported. Defining the assessment scope is mandatory, and the system prevents creation of an assessment without the scope.

With the enhanced approval flow, completed assessments are reviewed and validated, after which the assessor can request approval, and the approver can then approve the assessment, completing the workflow. With Smart Assessment, the assessment can now be moved back to the **Pending Response** state, allowing the assessor to retake the assessment and resubmit it for approval.

## Tasks and states that are associated with the assessment workflow

The process for the assessment workflow is as follows:

-   The owner of the assessment selects one or more business services and submits the Importance and impact tolerance​ assessment in Operational Resilience Workspace. This action creates an **Assessment** tab in Operational Resilience Workspace that contains the questions from the pre-populated questionnaire template.
-   The assessor of the assessment receives an email notification with a link to the assessment.
-   The assessor selects the link for the assessment and responds to the questionnaire. Based on the assessor's responses to the questionnaire, an assessment of the importance rating and the tolerable duration for one or more of the business services is generated.
-   After the assessment is completed, the owner reviews the responses and requests an approval for the Importance and impact tolerance​ assessment. The owner's responses may override the importance and impact tolerance rating of the assessment.
-   The approver of the assessment verifies the responses to the questions and approves the assessment.
-   The owner of the assessment then closes the assessment in Operational Resilience Workspace.

When you perform the assessment tasks, the assessment is updated through different states in Operational Resilience Workspace as described in the following table.

<table id="table_pjj_2x5_25b"><thead><tr><th>

State

</th><th>

Associated UI actions

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Select **New** in the All assessments form.

</td><td>

When you select **New** in the All assessments form, a record is created in the **Draft** state by default.

 Navigate to the **Details** tab and add the assessment details. In the **Services** tab, associate one or more business services with the assessment.

</td></tr><tr><td>

Pending response

</td><td>

Select **Assess** in the assessment form.

</td><td>

When you select **Assess** to proceed with the assessment, the application populates the assessment questionnaire under the **Assessment** tab.

 The state of the assessment is then automatically updated to the **Pending response** state. The assessor receives an email notification with a link to the assessment.

**Note:** To proceed with the assessment, you must associate at least one service with the assessment.

</td></tr><tr><td>

Assessment received

</td><td>

Select **Submit** in the assessment template and select **Save** in the assessment form to complete and save the assessment.

</td><td>

When the assessment is in the **Pending response** state, you can respond to the assessment questions that are given in the assessment template. To submit the responses, select **Submit**. To save the assessment, select **Save**. The state of the assessment is updated to **Assessment received**.

 An importance rating and the duration of the impact tolerance are automatically generated based on the questionnaire responses.

 The owner of the assessment requests an approval for the assessment. The approver of the assessment receives an email notification about the assessment.

</td></tr><tr><td>

Approved

</td><td>

Select **Request approval** in the assessment form.

</td><td>

The approver of the assessment verifies the responses to the questions and selects **Request approval**. The state of the assessment is automatically updated to **Approved**.

</td></tr><tr><td>

Closed

</td><td>

Select **Close** in the assessment form.

</td><td>

An assessment can be closed only when it is in the **Approved** state. To close the assessment, select **Close** in the assessment form. The state of the assessment is updated to **Closed**.

</td></tr></tbody>
</table>**Note:** If you have the sn\_oper\_res.admin role, you can delete the assessment in any state.​

If you have the sn\_oper\_res.admin role, you can set up the assessment ratings by updating the criticality and order of the assessment rating in the Important choices module. For more information on setting up the assessment rating, see [Update the Important choices module](../../grc-operational-res/task/set-up-important-choices.md).

For more information on the Operational Resilience roles, see [Roles installed with Operational Resilience](../../grc-operational-res/reference/roles-installed-with-op-res.md).

