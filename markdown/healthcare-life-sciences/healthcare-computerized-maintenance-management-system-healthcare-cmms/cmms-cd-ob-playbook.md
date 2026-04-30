---
title: Working on a medical device in-service case in Workspace
description: Use the playbook available with the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application to manage medical device in-service cases and complete requests to set the medical devices in-service.
locale: en-US
release: yokohama
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Managing medical device in-service cases in Workspace, Managing medical device cases in Workspace, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Working on a medical device in-service case in Workspace

Use the playbook available with the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application to manage medical device in-service cases and complete requests to set the medical devices in-service.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

The playbook experience provides fulfillers with visibility into cross-business workflows and the actionable activities used to complete these workflows. When the playbook experience is activated with Workspace in Healthcare CMMS, the **Playbook** tab appears for a medical device in-service case. For more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

As a clinical engineer with the sn\_hcls\_cmms.clinical\_engineer role, you can use the Healthcare CMMS playbook to complete all medical device in-service activities for a medical device. You can access the **Playbook** tab on your Workspace when a medical device in-service case is assigned to you. The Healthcare CMMS workflow populates the case data for all launched activities on the **Playbook** tab. You can select a stage in the playbook to complete the activities associated with the stage.

By default, the following stages are available to you as a clinical engineer with the sn\_hcls\_cmms.clinical\_engineer role on the **Playbook** tab of the Workspace.

<table id="table_irf_mxx_crb"><thead><tr><th>

Stage

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Medical device model intake](cmms-cd-ob-playbook.md#section_ewd_4zx_1vb)

</td><td>

Review the medical device model associated with the medical device.

</td></tr><tr><td>

[Maintenance plan intake](cmms-cd-ob-playbook.md#section_wjw_nzx_1vb)

</td><td>

Capture or review the benefits investigation preference opted by the patient and manage the pre-authorization activities.

</td></tr><tr><td>

[Medical device intake](cmms-cd-ob-playbook.md#section_gdm_nzx_1vb)

</td><td>

Review the medical devices to be in-service and the work orders created for the initial inspection of those devices.

</td></tr><tr><td>

[Maintenance plans](cmms-cd-ob-playbook.md#section_rq5_mzx_1vb)

</td><td>

Review the maintenance plans selected for the medical devices to be in-service.

</td></tr><tr><td>

[Review and confirm](cmms-cd-ob-playbook.md#section_dhd_nzx_1vb)

</td><td>

Close the medical device in-service request.

</td></tr></tbody>
</table>**Note:** The state of the medical device in-service case progresses as you complete a stage in the playbook. For more information, see [Life cycle of a medical device in-service case](cmms-cd-ob-life-cycle.md).

## Reviewing the medical device model

In the **Medical device model intake** stage of the playbook, complete the **Review model** activity by reviewing the name, number, and manufacturer details including the short description entered for a medical device model included within an medical device in-service request and modify the details, if needed.

**Note:** If there’s no new model required for the medical device, the **Medical device model intake** stage doesn't appear in the playbook.

## Managing maintenance plans

In the **Maintenance plan intake** stage of the playbook, complete the **Manage maintenance plans** activity by managing maintenance plans and schedules for the medical device. You can create a new maintenance plan by clicking **Add plan** and creating a work plan from the Work Plan page.

In the new Work Plan page, the required conditions and set conditions are automatically populated.

**Note:** If there’s no new model required for the medical device, the **Maintenance plan intake** stage doesn't appear in the playbook.

## Completing the medical device intake activities

In the **Medical device intake** stage of the playbook, complete the following activities:

1.  **Review devices**: Review the medical devices included within a medical device model and edit their details, if needed. You also evaluate the risks for a medical device. When the risk assessment is completed, the risk score is displayed for the device. For more information, see [Assess the risks when setting a medical device in-service](../task/cmms-assess-risk-ob-cd.md).

    After the medical device is reviewed, a work order for the initial inspection for each device included in the model is created automatically.

2.  **Review work orders**: Mark this step as complete when a technician completes the work order associated with the device. You can also view all work orders associated with the medical device model or create another work order by clicking **View all**.

## Reviewing maintenance plans

In the **Maintenance plans** stage of the playbook, review the schedule of the maintenance plan for the device that is automatically populated from the medical device model.

## Closing the medical device in-service request

In the **Review and confirm** stage of the playbook, complete the **Close case** activity by waiting until all other activities are completed, and then selecting a resolution code and adding any resolution notes.

**Note:** After the state of the medical device in-service case is set to **Closed complete**, the state of the medical device is automatically set to **Installed**.

