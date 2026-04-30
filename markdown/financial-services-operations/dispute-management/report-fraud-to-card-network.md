---
title: Report fraud to a card network
description: Report potential fraud on a transaction to a card network.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Initiating a chargeback, Work on a dispute case, Managing dispute service requests, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
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

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

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

If fraud was flagged, if not previously triggered, the block and reissue card task triggers. The transaction moves to the Initiate chargeback stage.

**Parent Topic:**[Initiating a chargeback](initiate-a-chargeback.md)

