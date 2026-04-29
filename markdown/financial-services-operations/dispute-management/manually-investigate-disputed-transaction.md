---
title: Investigate transactions
description: If a merchant refuses a transaction dispute, the case may move to the manual investigation task.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investigation, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Investigate transactions

If a merchant refuses a transaction dispute, the case may move to the manual investigation task.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level playbook of the **Processing** tab, select the transaction ID.

7.  Select the **Investigate transactions** activity under the Investigation playbook stage.

8.  Review the chargeback eligibility and chargeback ineligibility reasons for the disputed transaction.

9.  Select whether to create a chargeback request in the **Pursue chargeback** drop-down list.

    -   `Yes` - Pursue a chargeback from the merchant.
    -   `No` - Do not pursue chargeback from the merchant.
10. On the form, fill in the required fields and any other related information that you have gathered.

11. In the  **Remarks** field, enter any comments.

12. Select **Update** to save your changes.

13. Select **Continue**.

    The case is submitted to the dispute manager for review and approval when the chargeback eligibility is `No` and the agent sets the **Pursue Chargeback** value to `Yes`. After the manager approves the task, the user agent can continue with the dispute.

14. Select **Initiate chargeback**.


## Result

The dispute moves into the Chargeback stage.

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

