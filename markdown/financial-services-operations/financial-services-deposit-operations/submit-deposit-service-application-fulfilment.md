---
title: Submit a deposit service case for fulfillment
description: Collect all required information and documents from the customer and submit the deposit service case to back-office agents for fulfillment.
locale: en-US
release: xanadu
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Financial Services Deposit Operations, Financial Services Deposit Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Submit a deposit service case for fulfillment

Collect all required information and documents from the customer and submit the deposit service case to back-office agents for fulfillment.

## Before you begin

Role required:

-   For a business deposit service for a business customer \(account or contact\): sn\_bom\_deposit\_b2b.contributor or sn\_bom\_deposit\_b2b.agent\_connector
-   For a personal deposit service for a consumer: sn\_bom\_deposit\_b2c.contributor or sn\_bom\_deposit\_b2c.agent\_connector

**Important:** For the agent connector or contributor role to work, they must be combined with one of the roles in CSM industry data model or Contributor users. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

As a deposit contributor or agent connector, fill in the customer data and collect the required documents in the Initiate stage of the case playbook and submit the application for the required service. A deposit agent can also perform the activities in the Initiate stage of the case playbook.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![Lists icon.](../../fso-card-operations/image/list-icon.png)\).

3.  In the **Lists** tab, open the case list.

    -   For cases for the accounts managed by you, navigate to **Customer Cases** &gt; **My cases**.
    -   For all deposit service cases, navigate to **Deposit Cases** &gt; **All**.
4.  In the list, select the case to work on.

5.  Select the **Playbook** tab.

6.  Complete activities under the **Initiate and review** stage.

    **Note:** Depending on the deposit service type, a playbook might have additional or fewer activities in this stage.

    1.  In activity forms, fill in the fields and click **Mark complete**.

        **Note:** Fields are available depending on the deposit service type, such as Add standing order or Originate deposit account.

    2.  If applicable, in the Collect inbound documents activity, collect the listed documents from the customer.

        You can also collect customer documents from the Inbound Documents tab.

    3.  In the Submit application activity, enter any comments in the **Submission comment** field and then click **Submit** to complete the application.


## Result

-   The deposit case is submitted for fulfillment.
-   The Initiate and review stage in the case playbook shows as complete and the case automatically advances to the next stage.
-   The associated deposit tasks are assigned to an assignment group or an agent in the deposit service. Any document tasks are assigned to a group or an agent in the document service. The assignment group or user that the task is assigned to is based on the assignment rules.

**Parent Topic:**[Using Financial Services Deposit Operations](../concept/using-deposit-ops.md)

