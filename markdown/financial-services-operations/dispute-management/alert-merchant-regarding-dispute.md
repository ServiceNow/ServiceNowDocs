---
title: Review participating merchant alerts
description: Alert the merchant about a card transaction dispute.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Investigating a dispute, Working on a dispute case, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Review participating merchant alerts

Alert the merchant about a card transaction dispute.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

During the investigation stage of a transaction dispute, this task alerts the merchant to the disputed transaction. The merchant can choose to resolve the disputed transaction or decline to resolve the dispute.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

    The case playbook goes through the steps that are involved in resolving a case.

6.  In the case playbook integrated with Visa, select the **Processing** tab and select the transaction ID.

7.  Select the **Review participating merchant alerts** activity under the **Investigation** playbook stage.

8.  On the form, fill in the required fields and any other related information.

    In the **Merchant response** field, select one of the following options:

    -   **Accepted Dispute**- Merchant chose to resolve the dispute with the customer.
    -   **Declined Dispute**- Merchant declined to resolve the dispute with the customer.
9.  In the **Remarks** field, enter any comments.

10. Select one of the following actions.

    |Dispute activity|Action|
    |----------------|------|
    |**To save changes to the activity**|Select **Update**.|
    |**To close the Review participating merchant alerts activity**|Select **Close task**.|


## Result

The task state updates to **Closed Complete**. The outcome that the transaction sets to depends on the merchant's decision:

-   If the merchant resolves the dispute with the customer directly, the transaction moves to a Closed complete outcome.
-   If the merchant declines to resolve the dispute with the customer, the transaction dispute remains in the Work in progress state, and continues through the dispute process workflow stages.

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

