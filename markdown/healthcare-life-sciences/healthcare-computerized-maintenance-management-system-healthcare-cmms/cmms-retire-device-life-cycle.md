---
title: Life cycle of a medical device out-of-service case
description: Medical device out-of-service cases within the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application can be in one of the several states as it progresses through the fulfillment cycle.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing medical device out-of-service cases in Workspace, Managing medical device cases in Workspace, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Life cycle of a medical device out-of-service case

Medical device out-of-service cases within the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application can be in one of the several states as it progresses through the fulfillment cycle.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

The following diagram shows the different states of a medical device out-of-service case.

![Life cycle of a medical device out-of-service case. For more information on the case states, see the text that follows.](../image/cmms-lifecycle-retiring-device.png "Medical device out-of-service case life cycle")

<table id="table_ht1_n2p_5wb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Medical device out-of-service case is created but not yet assigned to anyone.

</td></tr><tr><td>

Open

</td><td>

Medical device out-of-service case is assigned.

</td></tr><tr><td>

Review in progress

</td><td>

Medical device out-of-service case is being reviewed by a clinical engineer.

</td></tr><tr><td>

Medical device out-of-service

</td><td>

Cancel all work orders for the medical device and sets the medical device to out-of-service.

</td></tr><tr><td>

Closed complete

</td><td>

Medical device out-of-service case was closed with the resolution code and notes, and the out-of-service process of the medical device was completed.

</td></tr><tr><td>

Closed incomplete

</td><td>

Medical device out-of-service case was marked as incomplete because the medical device was not set to out-of-service.

</td></tr><tr><td>

Canceled

</td><td>

Medical device out-of-service case was canceled because it was an invalid request.

</td></tr></tbody>
</table>