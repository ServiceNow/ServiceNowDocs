---
title: Life cycle of a medical device in-service case
description: Medical device in-service cases within the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application can be in one of the several states as it progresses through the fulfillment cycle.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing medical device in-service cases in Workspace, Managing medical device cases in Workspace, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Life cycle of a medical device in-service case

Medical device in-service cases within the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application can be in one of the several states as it progresses through the fulfillment cycle.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

The following diagram shows the different states of a medical device in-service case.

![Life cycle of a Medical device in-service case. For more information on the case states, see the Medical device in-service case states section.](../image/cmms-ob-cd-case-lc.png "Medical device in-service case life cycle")

<table id="table_hrb_hsl_drb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Medical device in-service case is created but not yet assigned to anyone.

</td></tr><tr><td>

Open

</td><td>

Medical device in-service case is assigned.

</td></tr><tr><td>

Review in progress

</td><td>

Medical device in-service case is being reviewed by a clinical engineer.

</td></tr><tr><td>

Model setup

</td><td>

New medical device model is being created and a maintenance plan is being created for the model.

 **Note:** The **Model setup** state occurs when a new medical device model is requested for the medical device.

</td></tr><tr><td>

Device setup

</td><td>

Medical device is being added to the application, risks are being assessed for the medical device, and the work order for the initial inspection of the medical device is being completed.

</td></tr><tr><td>

Closed complete

</td><td>

Medical device in-service case was closed with the resolution code and notes, and the in-service process of the medical device was completed.

</td></tr><tr><td>

Closed incomplete

</td><td>

Medical device in-service case was marked as incomplete because the medical device was not in-service.

</td></tr><tr><td>

Canceled

</td><td>

Medical device in-service case was canceled because it was an invalid request.

</td></tr></tbody>
</table>**Note:** You can't edit a medical device in-service case when the state of the case is set to **Closed complete**, **Closed incomplete**, or **Canceled**.

