---
title: Certifying services using self-attestation
description: Certify the operational resilience status of your business services by completing the self-attestation process in the Operational Resilience Workspace. Complete the self-assessment questionnaire about the services, generate a self-attestation report, and upload the PDF so that you can have a copy of the report for your records. You can perform self-attestation on the selected business service and its child records.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Managing Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Certifying services using self-attestation

Certify the operational resilience status of your business services by completing the self-attestation process in the Operational Resilience Workspace. Complete the self-assessment questionnaire about the services, generate a self-attestation report, and upload the PDF so that you can have a copy of the report for your records. You can perform self-attestation on the selected business service and its child records.

## Creating a self-attestation

To create a self-attestation in the Operational Resilience application, navigate to **All** &gt; **Operational Resilience Workspace** &gt; **All self attestations** in an instance.

Use the self-attestation template supported by the Smart Assessment Engine to submit an assessment on the services. The following example shows the self-attestation template in the Operational Resilience Workspace.

![Self-attestation template in the Operational Resilience Workspace.](../../grc-operational-res/image/self-attestation-template.png "Self-attestation template in Operational Resilience Workspace")

## Self-attestation tasks and the states related to each task

With the sn\_oper\_res.manager role, you can complete the following self-attestation tasks in Operational Resilience Workspace:

1.  Initiate a self-attestation to attest one or more business services.​
2.  Select the assessment type as Smart Assessment.
3.  Select the Operational Resilience Attestation Template as the attestation template.
4.  Use the Default Self Attestation HTML Template as the PDF template for the self-attestation in the self-attestation form. This template provides the format for the PDF and an option to include your e-signature in the report. For instructions on configuring the attestation template, see [Create and edit the attestation template](../../grc-operational-res/task/create-new-attestation-template.md).
5.  Add the services that you want to certify the status for in the self-attestation form. Respond to the pre-defined set of questions in the assessment, such as the names and description of the services, details on the scenario analysis of the important services, your approach for the scenario analysis, and so on.
6.  Submit the assessment and attest for the services.
7.  Download a PDF of the self-attestation from the Activity section of the self-attestation form and save a copy of the report for your records. For instructions on configuring the attestation PDF template, see [Create HTML and PDF document templates​](../../grc-operational-res/task/create-an-html-template.md).
8.  Close the self-attestation so that the self-attestation process is complete.

As you complete the self-attestation tasks outlined in the self-attestation process, the associated states are automatically updated in a predetermined sequence. The states and corresponding UI actions for these tasks are detailed in the following table.

<table id="table_fp3_vcv_25b"><thead><tr><th>

States

</th><th>

Associated UI actions

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Select **New** in the self-attestation form.

</td><td>

When you select **New** to submit a self-attestation for the services, a record is created in the **Draft** state by default. The information on the self-attestation is displayed on the **Details** tab in the self-attestation form.

</td></tr><tr><td>

Awaiting attestation

</td><td>

Select **Attest** in the self-attestation form.

</td><td>

When you select the services that you want to certify, you can choose the attestation template and select **Attest** to proceed with the attestation. The application then creates an assessment instance automatically on the **Assessment Instances** tab.

 This action moves the state of the self-attestation record to **Awaiting attestation**.

 **Note:** To proceed with the attestation process, you must associate at least one service with the self-attestation.

</td></tr><tr><td>

Cancelled

</td><td>

In the self-attestation form, select **Cancel** .

</td><td>

When the self-attestation record is in the **Awaiting Attestation** state, you can cancel an erroneous or invalid attestation by selecting **Cancel** in the self-attestation form. This is an optional step. The state of the self-attestation is then updated to **Cancelled**.

</td></tr><tr><td>

Attestation received

</td><td>

In the attestation template, select **Submit** and select **Save** to complete the attestation process. Select **Export to PDF** to export the questionnaire response to a PDF.

</td><td>

When the self-attestation record is in the **Awaiting attestation** state, you can respond to the assessment questions that are given in the attestation template. To submit the responses, select **Submit** and then select **Save** to save the assessment. The state of the self-attestation is automatically updated to **Attestation received**.

 Select **Export to PDF** to export the questionnaire response to a PDF, sign the self-attestation, and save a copy for your records. You can download the PDF from the Activity section of the self-attestation form.

</td></tr><tr><td>

Closed

</td><td>

Select **Close** in the self-attestation form.

</td><td>

To close the attestation, select **Close** in the self-attestation form. The state of the self-attestation is then updated to **Closed**.

</td></tr></tbody>
</table>**Note:** Optionally, if the self-attestation contains invalid data and you're the owner of the self-attestation, you can delete the self-attestation by selecting **Delete** in the self-attestation form. The self-attestation is then deleted from the self-attestations list in Operational Resilience Workspace.

## Downloading the PDF of the self-attestation

As an owner of the self-attestation, you can download the PDF from the Activity section of the self-attestation form. You can also share it offline with the auditors, external contacts, or stakeholders.

## Roles required to perform the self-attestation tasks

If you're a user of Operational Resilience Workspace, you can perform different self-attestation tasks with the following roles:

-   With the sn\_oper\_res.admin role, you can create and maintain the pre-defined assessment questionnaire templates.
-   With the sn\_oper\_res.manager role, you can complete the self-attestation of the operational resilience profile of the services by selecting one or more services, by choosing the template for the self-attestation, and by providing the answers to a pre-defined set of questions.

    **Note:**

    If you're the owner of the self-attestation with the Operational Resilience manager or the Operational Resilience administrator role, you can create a self-attestation, update its details, or delete the self-attestation.

    As an Operational Resilience administrator, you can create and modify the assessment questionnaire template. You must have the Operational Resilience manager role to respond to the assessment questionnaire in the Operational Resilience application.


## Reference information

For more information on submitting a self-attestation in Operational Resilience Workspace, see [Perform the self-attestation assessment](../task/create-new-attestation-in-ws.md).

For the description of the field values that are listed in the self-attestation form in the Operational Resilience Workspace, see [Create New Self attestation form](../reference/self-attestation-new-record-reference-form-in-ws.md).

As an optional task, when you have the sn\_oper\_res.admin role, you can create a customized attestation template instead of using the default attestation template that is provided with the base system. For more information on creating a customized attestation template, see [Create and edit the attestation template](../../grc-operational-res/task/create-new-attestation-template.md).

