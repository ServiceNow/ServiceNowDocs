---
title: Life cycle of a medical device AEM case
description: Medical device AEM cases within the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application can be in one of the several states as it progresses through the fulfillment cycle.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing medical device AEM cases in Workspace, Managing medical device cases in Workspace, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Life cycle of a medical device AEM case

Medical device AEM cases within the Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application can be in one of the several states as it progresses through the fulfillment cycle.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

The following diagram shows the different states of a medical device AEM case.

![Life cycle of Medical device AEM case. For more information on each state, refer to the Medical device AEM case states section.](../image/cmms-aem-cd-case-lc.png "Medical device AEM case life cycle")

<table id="table_hrb_hsl_drb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Medical device AEM case is created but not yet assigned to anyone.

</td></tr><tr><td>

Open

</td><td>

Medical device AEM case is assigned.

</td></tr><tr><td>

Review in progress

</td><td>

Medical device AEM case is being reviewed by a clinical engineer.

</td></tr><tr><td>

Model setup

</td><td>

New maintenance plan is being created for the model based on the AEM request.

</td></tr><tr><td>

Closed complete

</td><td>

Medical device AEM case was closed with the resolution code and notes, and the review process of the AEM request was completed.

</td></tr><tr><td>

Closed incomplete

</td><td>

Medical device AEM case was marked as incomplete because the AEM request was not approved.

</td></tr><tr><td>

Canceled

</td><td>

Medical device AEM case was canceled because the AEM request was invalid.

</td></tr></tbody>
</table>**Note:** You can't edit a medical device AEM case when the state of the case is set to **Closed complete**, **Closed incomplete**, or **Canceled**.

