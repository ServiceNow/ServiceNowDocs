---
title: Submit a treasury service case for fulfillment
description: Collect all required information about the customer and submit the case to back-office agents for fulfillment.
locale: en-US
release: zurich
product: Financial Services Treasury Operations
classification: financial-services-treasury-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Treasury Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Submit a treasury service case for fulfillment

Collect all required information about the customer and submit the case to back-office agents for fulfillment.

## Before you begin

Role required: sn\_bom\_treasury.contributor or sn\_bom\_treasury.agent\_connector

**Important:** For the agent connector or contributor role to work, they must be combined with one of the roles in CSM industry data model or Contributor users. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

Fill in the customer data in the Initiate stage of the case playbook and submit the application for activating the requested treasury product. A treasury agent can also perform the activities in the Initiate stage of the case playbook.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Treasury Service Cases**, click **All**.

4.  In the list, select the case to work on.

5.  Select the **Playbook** tab.

6.  Complete activities under the **Initiate** stage.

    1.  In the setup activity, fill in the fields and click **Mark complete**.

        **Note:** Fields are available depending on the treasury product type, such as wire transfer or RDC.

    2.  In the accounts activity, click **Add new** to add the customer accounts to be used for the treasury service.

    3.  In the users activity, click **Add new** to add the users for the treasury service.

    4.  In the Submit case activity, enter any comments in the **Submission comment** field and then click **Submit** to complete the application.


## Result

-   The treasury case is submitted for fulfillment.
-   The Initiate stage in the case playbook shows as complete and the case automatically advances to the next stage.
-   The associated treasury tasks are assigned to an assignment group or an agent in the treasury service. Any document tasks are assigned to a group or an agent in the document service. The assignment group or user that the task is assigned to is based on the assignment rules.

**Parent Topic:**[Using Financial Services Treasury Operations](../concept/using-treasury-ops.md)

