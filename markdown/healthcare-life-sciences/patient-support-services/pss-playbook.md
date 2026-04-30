---
title: Working on an enrollment case in Workspace
description: Use the playbook available with the Patient Support Services application to manage enrollment cases and complete requests for patient support services.
locale: en-US
release: yokohama
product: Patient Support Services
classification: patient-support-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Managing enrollment requests in Workspace, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Working on an enrollment case in Workspace

Use the playbook available with the Patient Support Services application to manage enrollment cases and complete requests for patient support services.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

The playbook experience provides fulfillers with visibility into cross-business workflows and the actionable activities used to complete these workflows. When the playbook experience is activated with Workspace in Patient Support Services, the **Playbook** tab appears for an enrollment case. For more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

As a care coordinator with the sn\_patientservice.agent role, you can use the Patient Support Services playbook to complete all enrollment request activities for a patient. You can access the **Playbook** tab on your Workspace when an enrollment case is assigned to you. The Patient Support Services workflow populates the case data for all launched activities on the **Playbook** tab. You can select a stage in the playbook to complete the activities associated with the stage.

By default, the following stages are available to you as a care coordinator with the sn\_patientservice.agent role on the **Playbook** tab of the Enrollment request workspace.

<table id="table_irf_mxx_crb"><thead><tr><th>

Stage

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Intake](pss-playbook.md#section_o5n_czv_crb)

</td><td>

Complete the initial enrollment application review activities.

</td></tr><tr><td>

[Benefit investigation](pss-playbook.md#section_qbd_tsx_crb)

</td><td>

Capture or review the benefits investigation preference opted by the patient and manage the pre-authorization activities.

**Note:** By default, the **Benefit Investigation** characteristic is available for a program within the Patient Support Services application. Your administrator can add more characteristics and associate them with one or more programs. Depending on the configuration, the activities associated with a characteristic might appear in the playbook.

</td></tr><tr><td>

[Prescription details](pss-playbook.md#section_scf_5xx_crb)

</td><td>

Place a prescription order.

</td></tr><tr><td>

[Program services](pss-playbook.md#section_fz4_gzx_crb)

</td><td>

Review and fulfill the program services that the patient has been enrolled into.

</td></tr><tr><td>

[Resolve and close](pss-playbook.md#section_efd_c1y_crb)

</td><td>

Close the enrollment request.

</td></tr></tbody>
</table>**Note:** The state of the enrollment case progresses as you complete a stage in the playbook. For more information, see [Life cycle of an enrollment case](pss-enrollment-life-cycle.md).

## Completing the initial review activities

In the **Intake** stage of the playbook, complete the following activities:

1.  **Review enrollment details**: Review the patient, prescriber, program, and program services details entered for a patient included within an enrollment request. When the Review enrollment details activity is set to complete, the Patient Support Services workflow automatically sends a consent form to the patient.
2.  **Review insurance details**: Capture or review the insurance information of the patient.

    As a care coordinator, you can contact the patient directly to verify the insurance information. You can enter or review the insurance information from the **Review Insurance** activity of the playbook for Patient Support Services in your Workspace and mark the activity as complete when done.

3.  **Review prescription**: Capture or review the prescription ordered for a patient. You can add a new prescription record to include the prescription details. If there is no prescription available to you, contact the prescriber to enter the prescription details.

    To add a new prescription, click **Add new**, fill in the details of the prescription in the Medication Prescription form, and click **Save**. For more information, see [Medication Prescription form](../reference/hcls-med-prescription-form.md).

    **Note:** If there is no medication product associated with the program, the **Review prescription** activity doesn't appear in the playbook.

4.  **Review patient consent**: Check the status of completion of the patient consent form assigned to the patient. After the patient completes the to-do item for the consent form, the consent is listed in the activity. As a care coordinator, you can then review the consent and mark the **Review patient consent** activity to complete in the playbook.
5.  **Review enrollment eligibility**: Accept or reject the enrollment request based on the eligibility checklist.

## Completing the benefit investigation activities

In the **Benefit investigation** stage of the playbook, complete the following activities:

1.  **Review patient preference**: Review the benefits investigation preference opted by the patient.
2.  **Review specialty pharmacy details**: Review the specialty pharmacy details as provided by the patient. The **Review specialty pharmacy details** activity appears only when the patient has selected specialty pharmacy in the enrollment request form.
3.  **Review pre-authorization**: Review and verify if pre-authorization is required for the program. If pre-authorization is required, click **Add new**, fill in the details of pre-authorization details provided by a payer organization in the Pre-authorization request form, and click **Save**. For more information, see [Pre-authorization request form](../reference/hcls-pre-auth-form.md).

    **Note:** If pre-authorization is not required for the medication prescription, you can skip this activity.


## Placing a prescription order

In the **Prescription details** stage of the playbook, complete the **Submit prescription order** activity by contacting the pharmacy to place the prescription order. In addition, verify the medicine dosage and delivery location with the pharmacy and capture the expected delivery date.

**Note:** If there is no medication product associated with the program, the **Prescription details** stage doesn't appear in the playbook.

## Fulfilling the program services

In the **Program services** stage of the playbook, complete the **Fulfill services** activity by reviewing and fulfilling the program services that the patient has been enrolled into. The **Fulfill services** activity provides the complete visibility into the services fulfillment status.

In the **Number** column of the **Fulfill services** activity, click a program number and when a program service is completed, mark the activity as complete. If required, you can capture the shipping details in the **Fulfill services** activity along with other details including the tracking number.

**Note:** You can either fulfill the services on your own or assign them to another team who can fulfill the services activity.

When all the program services are fulfilled, the status of the associated enrolled program service record changes to **Fulfilled** and the date fulfilled is automatically set to the current date.

## Closing the enrollment request

In the **Resolve and close** stage of the playbook, complete the **Close enrollment request** activity by waiting until all other activities are completed, and then selecting a resolution code and adding any resolution notes. For the case marked as closed complete, a survey is sent out to the patient to fill in.

