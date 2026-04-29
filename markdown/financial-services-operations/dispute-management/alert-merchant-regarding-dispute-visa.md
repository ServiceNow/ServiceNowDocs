---
title: Review participating merchant alerts for Visa disputes
description: Alert the merchant about a Visa card transaction dispute.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Investigate, Processing a Visa dispute, Resolving disputes with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review participating merchant alerts for Visa disputes

Alert the merchant about a Visa card transaction dispute.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

During the investigation stage of a transaction dispute, this task alerts the merchant to the disputed transaction. The merchant can choose to resolve the disputed transaction or decline to resolve the dispute.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Review participating merchant alerts** activity under the **Investigation** playbook stage.

7.  On the form, fill in the required fields and any other related information.

    In the **Merchant response** field, select one of the following options:

    -   **Accepted Dispute**- Merchant chose to resolve the dispute with the customer.
    -   **Declined Dispute**- Merchant declines to resolve the dispute with the customer.
8.  In the  **Remarks** field, enter any comments.

9.  Select one of the following actions.

    |Dispute activity|Action|
    |----------------|------|
    |**To save changes to the activity**|Select **Update**.|
    |**To close the activity**|Select **Close task**.|


## Result

The task state updates to Closed Complete. The outcome that the transaction sets to depends on the merchant's decision:

-   If the merchant resolves the dispute with the customer directly, the transaction moves to a Closed complete outcome.
-   If the merchant declines to resolve the dispute with the customer, the transaction dispute remains in the Work in progress state, and continues through the dispute process workflow stages.

**Parent Topic:**[Investigate stage](../concept/investigate-stage.md)

