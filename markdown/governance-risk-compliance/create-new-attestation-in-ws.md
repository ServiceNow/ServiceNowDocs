---
title: Perform the self-attestation assessment
description: Create an assessment for the self-attestation and certify the resilience status of services in the Operational Resilience Workspace. Perform the self-attestation assessment using the Smart Assessment template provided with the base system.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Certifying services using self-attestation, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Perform the self-attestation assessment

Create an assessment for the self-attestation and certify the resilience status of services in the Operational Resilience Workspace. Perform the self-attestation assessment using the Smart Assessment template provided with the base system.

## Before you begin

Role required: sn\_oper\_res.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** and select **All self attestations** from the list view.

2.  Select **New**.

    You can create the self-attestation assessment in the Operational Resilience Workspace.

    The Create New Self-attestation form is displayed.

    ![Self-attestation form.](../../grc-operational-res/image/self-attest-record.png)

3.  In the **Name** and **Description** fields, add the name and description for the self-attestation.

4.  Choose the assessment type from the **Assessment type** field.

    You can select the type of assessment as shown in the table.

<table id="choicetable_ltj_f4q_xfc"><thead><tr><th align="left" id="d221586e125">

Choice

</th><th align="left" id="d221586e128">

Description

</th></tr></thead><tbody><tr><td id="d221586e134">

**Select __Smart assessment__.**

</td><td>

Select the Smart Assessment method for performing the self-attestation.

</td></tr><tr><td id="d221586e152">

**Select __Legacy assessment__.**

</td><td>

Select the Legacy assessment method for performing the self-attestation.

 Select the Self-attestation Template in the **Assessment template** field.

</td></tr></tbody>
</table>5.  To use the Legacy assessment, select the **Operational Resilience Attestation Template** option.

    The attestation template contains the pre-defined questions for the assessment. The Operational Resilience application provides an attestation template as part of the base system.

    **Note:** If you have the sn\_oper\_res.admin role, you can customize the default attestation template for your own business needs. For information on creating a customized attestation template, see [Create and edit the attestation template](../../grc-operational-res/task/create-new-attestation-template.md).

6.  To use the Smart Assessment, select the default **Self attestation assessment template** populated in the **Smart assessment templates** field.

    The base version includes the default **Self attestation assessment template**, using the Smart Assessment, with a pre-configured questionnaire. Operational Resilience administrators can set up their own attestation templates in the Assessment Workspace and choose from various data types to suit their needs.

    **Note:** Before starting the self-attestation process, verify that Operational Resilience administrator has set up and published the Self-attestation template in the Assessment Workspace. If the Smart Assessment template for Self-attestation is not set up and published in the Assessment Workspace, it will not be displayed for selection in the **Smart assessment templates** field in the self-attestation form.

    For information on setting up Smart Assessment templates, see [Create and edit the attestation template](../../grc-operational-res/task/create-new-attestation-template.md).

    For information on Smart Assessment documentation, see [Create a Smart Assessment template](../../grc-operational-res/task/create-sm-asmt-temp-as-ws.md) and [Create an assessment template](../../assessment-engine/task/sae-asmnt-template-create.md).

    ![Default questionnaire.](../../grc-operational-res/image/self-attest-default-questions.png)

    When creating a template, ensure that you select **Self attestation assessment** as the purpose from the Assessment templates list in the Assessment Workspace as shown in the example.

    ![Purpose.](../../grc-operational-res/image/self-attest-purpose.png)

    **Note:** Beginning with Operational Resilience Release 22.0.x, contributors can answer questions, but only an assessor can submit the self-attestation assessment.

7.  Select the **Default Self Attestation HTML Template** from the **PDF Template** field.

    You can use the Default Self Attestation HTML Template to generate the PDF of the self-attestation report.

    **Note:** To access the PDF template option in the self-attestation form, ensure that the Document Templates application is installed on your instance. The PDF template option will only be visible if this application is available.

8.  In the **Signature** field, select **Attach image** to attach the signature image for the self-attestation.

    The following informational message is displayed: **Select the e-signature to be embedded in the template.**

    **Note:** You must select the supported file format, such as either the JPEG, PNG, BMP, GIF, ICO, SVG format, for the signature image. If you select a file format that is not supported, such as the Microsoft Word format, the following error message is displayed on the screen: **Selected file type is invalid. Valid field types: JPEG, PNG, BMP, GIF, ICO, SVG.**

    If you want to delete an existing image and add a new image instead, you can use the **Delete** icon in the **Signature** field and add another signature image.

9.  In the Assignees panel, update the **Owner** field to select the owner of the self-attestation.

10. In the Milestones panel, add the due date for the self-attestation.

    The following informational message is displayed on the screen: **Next step: Save the attestation details to proceed with the selection of services.**

11. Select **Save**.

    The self-attestation details are saved in the instance.

    The self-attestation is created in the **Draft** state.

    The **Details** tab is updated with the self-attestation information. The attestation details are saved. You can define the scope of the self-attestation in the **Scope** tab.

12. In the **Scope** tab, select **Add**, select one or more services, and select **Add** again in the modal.

    You can select the services to be certified in the self-attestation report.

    **Note:** You must add at least one service to proceed with the self-attestation.

13. To send the attestation to the owner, select **Attest** in the form.

    The self-attestation record moves to the **Awaiting attestation** state and an assessment is created for it.


## What to do next

Request responses on the assessment and then submit the self-attestation to the owner for the certification. For more information, see [Submit the self-attestation report](update-a-self-attestation-record-in-ws.md).

