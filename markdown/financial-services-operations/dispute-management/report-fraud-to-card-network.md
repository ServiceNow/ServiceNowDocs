---
title: Report fraud to a card network
description: Report potential fraud on a transaction to a card network.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Chargeback, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Report fraud to a card network

Report potential fraud on a transaction to a card network.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

A transaction will include the Fraud reporting task within the workflow if potential fraud was flagged for a transaction during manual investigation.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Fraud reporting** activity under the Chargeback playbook stage.

7.  Select the fraud reporting task that you want to complete.

8.  On the form, fill in the required fields and any other related information that you've gathered.

9.  In the **Work notes** field, enter any comments.

10. Close the task from the task form.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the Fraud reporting task**|Select **Close**.|


## Result

If fraud was flagged, if not previously triggered, the [block and reissue card](block-and-reissue-new-card.md) task triggers. The transaction moves to the Initiate chargeback stage.

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

