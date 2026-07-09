---
title: Investigate Visa transactions
description: If a merchant refuses a transaction dispute, the case may move to the manual investigation task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/manually-investigate-disputed-transaction-visa.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investigate, Processing a Visa dispute, Managing disputes integrated with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Investigate Visa transactions

If a merchant refuses a transaction dispute, the case may move to the manual investigation task.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-combine-csm-industry-roles.md).

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(\[Omitted image "inline-data-vis-96px-list.png"\] Alt text: lists icon\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the transaction ID from the playbook to open the **Dispute Workspace** of the transaction.

6.  Select the **Investigate transactions** activity under the **Dispute Workspace**.

7.  Select whether to create a chargeback request in the **Pursue chargeback** drop-down list.

    -   `Yes` - Pursue a chargeback from the merchant.
    -   `No` - Do not pursue chargeback from the merchant.
8.  Fill in the required fields in the form, and any other related information that you have gathered.

9.  In the **Remarks** field, enter any comments.

    This step is optional.

10. Select **Update** to save your changes.

11. Select **Continue**.

    The case is submitted to the dispute manager for review and approval when the chargeback eligibility is `No` and the agent sets the **Pursue Chargeback** value to `Yes`. After the manager approves the task, the user agent can continue with the dispute.

12. Select **Initiate dispute**.


## Result

A dispute is initiated.

**Parent Topic:**[Investigate stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/investigate-stage.md)

