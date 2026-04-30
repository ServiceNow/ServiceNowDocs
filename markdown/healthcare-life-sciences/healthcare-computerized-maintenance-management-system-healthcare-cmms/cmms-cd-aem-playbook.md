---
title: Working on a medical device AEM case in Workspace
description: Use the playbook available with the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application to manage medical device AEM cases and complete the review of an alternative equipment maintenance \(AEM\) request for a medical device model.
locale: en-US
release: yokohama
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing medical device AEM cases in Workspace, Managing medical device cases in Workspace, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Working on a medical device AEM case in Workspace

Use the playbook available with the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application to manage medical device AEM cases and complete the review of an alternative equipment maintenance \(AEM\) request for a medical device model.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

The playbook experience provides fulfillers with visibility into cross-business workflows and the actionable activities used to complete these workflows. When the playbook experience is activated with Workspace in Healthcare CMMS, the **Playbook** tab appears for a medical device AEM case. For more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

As a clinical engineer with the sn\_hcls\_cmms.clinical\_engineer role, you can use the Healthcare CMMS playbook to complete all activities for reviewing an AEM request for a medical device model. You can access the **Playbook** tab on your Workspace when a medical device AEM case is assigned to you. The Healthcare CMMS workflow populates the case data for all launched activities on the **Playbook** tab. You can select a stage in the playbook to complete the activities associated with the stage.

By default, the following stages are available to you as a clinical engineer with the sn\_hcls\_cmms.clinical\_engineer role on the **Playbook** tab of the Workspace.

<table id="table_irf_mxx_crb"><thead><tr><th>

Stage

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Intake](cmms-cd-aem-playbook.md#section_ry3_4cd_bvb)

</td><td>

Review the medical device AEM case details, make changes to the existing maintenance plan, and submit the AEM request for approval.

</td></tr><tr><td>

[Manage AEM plan](cmms-cd-aem-playbook.md#section_c41_4cd_bvb)

</td><td>

Remove the medical device model from the current maintenance plan.

</td></tr><tr><td>

[Review and confirm](cmms-cd-aem-playbook.md#section_tnh_ncd_bvb)

</td><td>

Close the review request.

</td></tr></tbody>
</table>**Note:** The state of the medical device AEM case progresses as you complete a stage in the playbook. For more information, see [Life cycle of a medical device in-service case](cmms-cd-ob-life-cycle.md).

## Completing the initial review activities

In the **Intake** stage of the playbook, complete the following activities:

1.  **Review AEM request**: Review the details entered for an AEM request for a medical device model and update the details, if needed.
2.  **Submit AEM request for approval**: Review any additional information required for the medical device model and submit the AEM request for approvals. If an approval workflow for AEM request is configured by your administrator, the AEM request is submitted for approvals.

## Managing AEM requests

In the **Manage AEM plan** stage of the playbook, complete the **Remove from maintenance plans** activity by removing the medical device model from the current maintenance plan, if available.

You can create a new maintenance plan by clicking **Add plan** and creating a work plan from the Work Plan page.

In the new Work Plan page, the required conditions and set conditions are automatically populated.

## Closing the AEM request

In the **Review and confirm** stage of the playbook, complete the **Close case** activity by waiting until all other activities are completed, and then selecting a resolution code and adding any resolution notes.

