---
title: Working on a procedure request case in Workspace
description: Use the playbook available with the Pre-Visit Management application to manage procedure request cases and schedule a high value procedure for patients.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage procedure requests, Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Working on a procedure request case in Workspace

Use the playbook available with the Pre-Visit Management application to manage procedure request cases and schedule a high value procedure for patients.

**Important:**

Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

The playbook experience provides fulfillers with visibility into cross-business workflows and the actionable activities used to complete these workflows. When the playbook experience is activated with Workspace in Pre-Visit Management, the **Playbook** tab appears for a procedure request case. For more information on how to interact with a playbook, see Interact with Playbook.

As a patient service representative with the sn\_previsit.patient\_service\_agent role assigned to you, you can use the playbook to complete all pre-visit activities for a patient. You can access the **Playbook** tab on your Workspace when a procedure request case is assigned to you. The Pre-Visit Management workflow populates the case data for all launched activities on the **Playbook** tab. You can select a stage in the playbook to complete the activities associated with the stage.

By default, the following stages are available to you as a patient service representative with the sn\_previsit.patient\_service\_agent role on the **Playbook** tab of the Procedure request workspace.

<table id="table_irf_mxx_crb"><thead><tr><th>

Stage

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Intake](pre-visit-playbook.md#section_r4f_qjv_2rb)

</td><td>

Complete the initial procedure order review activities.

</td></tr><tr><td>

[Pre-authorizations](pre-visit-playbook.md#section_rwx_tjv_2rb)

</td><td>

Capture pre-authorization details for follow-up and audit purposes.

</td></tr><tr><td>

[Schedule procedure](pre-visit-playbook.md#section_zzj_yjv_2rb)

</td><td>

Review appointments created for the procedure.

</td></tr><tr><td>

[Resolve and close](pre-visit-playbook.md#section_azx_gkv_2rb)

</td><td>

Wait until all child activities are completed so that the procedure request is automatically closed.

</td></tr></tbody>
</table>**Note:** Before the appointment date, the Pre-Visit Management workflow automatically assigns the to-do item to the patient for reviewing and signing the procedure consent, and also sends an email notification about the to-do item to the patient. The day when to send the procedure consent form is configured by your administrator. For more information, see [Configure when to send the procedure consent form to a patient](../task/pre-visit-config-proc-consent-time.md).

## Completing the initial review activities

In the **Intake** stage of the playbook, complete the following activities:

1.  **Review order**: Review a procedure request order for a patient. When the review order activity is set to complete, the Pre-Visit Management workflow automatically assigns to-dos to the patient and sends an email notification about to-do items to the patient.
2.  **Patient To-dos**: Check the status of to-dos items for a procedure request assigned to the patient. By default, the to-do items configured for the patients are to review their insurance information and sign the privacy consent form.
3.  **Review Insurance**: Capture or review the insurance information of the patient.

    As a patient service representative, you can contact the patient directly to verify the insurance payment information. You can enter or review the insurance payment information from the **Review Insurance** activity of the playbook for Pre-Visit Management in your Workspace and mark the activity as complete when done. The Verify payment information form also includes the procedure payment type detail. Pre-authorization is only required with the insurance payment type. If the self-pay payment type is selected, the **Pre-authorizations** stage is automatically removed from the Pre-Visit Management playbook.

    **Note:** A patient can also access the to-do list from their patient portal and complete the insurance information verification activity. After the patient completes the to-do item for the insurance payment information, the **Review Insurance** activity is automatically set to **Pending review**. As a patient service representative, you can then mark the **Review Insurance** activity as complete in the playbook.

4.  **Review patient consent**: Check the status of completion of the patient consent form assigned to the patient. After the patient completes the to-do item for the consent form, the consent is listed in the activity. As a patient service representative, you can then review the consent and mark the **Review patient consent** activity to complete in the playbook.

## Completing the pre-authorization activities

In the **Pre-authorizations** stage of the playbook, complete the following activities:

1.  **Create pre-authorization**: Enter the pre-authorization reference number as provided by the insurance company.
2.  **Review pre-authorization**: Capture the pre-authorization final status, approval or denial reasons, and other details for audit purposes.

## Reviewing appointments for procedures

In the **Schedule procedure** stage, complete the **Review appointments** activity.

Only after the booked appointment details are entered by using the **Create appointment** UI action, the patient service representative can review the appointment details and mark the **Review appointments** activity of the **Schedule procedure** stage as complete in the Pre-Visit Management playbook. For more information, see [Managing appointment bookings for procedure requests](pre-visit-booking-appt.md#).

**Note:** After the **Schedule procedure** stage is completed, the **Resolve and Close** stage is automatically run.

## Closing the procedure request

The **Resolve and Close** stage is automatically closed when all the child activities associated with a procedure request case are completed.

