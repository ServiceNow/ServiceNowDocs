---
title: Working on a medical device out-of-service case in Workspace
description: Use the playbook available with the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application to manage medical device out-of-service cases and complete requests for setting the medical devices to out-of-service.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing medical device out-of-service cases in Workspace, Managing medical device cases in Workspace, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Working on a medical device out-of-service case in Workspace

Use the playbook available with the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application to manage medical device out-of-service cases and complete requests for setting the medical devices to out-of-service.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

The playbook experience provides fulfillers with visibility into cross-business workflows and the actionable activities used to complete these workflows. When the playbook experience is activated with Workspace in Healthcare CMMS, the **Playbook** tab appears for a medical device out-of-service case. For more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

As a clinical engineer with the sn\_hcls\_cmms.clinical\_engineer role, you can use the Healthcare CMMS playbook to complete all out-of-service activities for a medical device. You can access the **Playbook** tab on your Workspace when a medical device out-of-service case is assigned to you. The Healthcare CMMS workflow populates the case data for all launched activities on the **Playbook** tab. You can select a stage in the playbook to complete the activities associated with the stage.

By default, the following stages are available to you as a clinical engineer with the sn\_hcls\_cmms.clinical\_engineer role on the **Playbook** tab of the Workspace.

**Note:** The state of the medical device out-of-service case progresses as you complete a stage in the playbook. For more information, see [Life cycle of a medical device out-of-service case](cmms-retire-device-life-cycle.md).

## Completing the initial review activities

In the **Medical device out-of-service** stage of the playbook, complete the following activities:

1.  **Review medical device details**: Review the medical device details for a medical device model and update the details, if needed.

    After the medical device is reviewed and approved, a work order for the initial inspection for each device included in the model is created automatically.

2.  **Cancel work orders**: Review and cancel the work orders for each medical devices.
3.  **Set medical device out-of-service**: Set the medical device to out-of-service.
4.  **Disposal work order**: Create a disposal work order for the out-of-service device.

## Closing the out-of-service request

In the **Review and confirm** stage of the playbook, complete the **Close case** activity by waiting until all other activities are completed, and then selecting a resolution code and adding any resolution notes.

