---
title: Provide immediate final credit
description: Issue immediate final credit to the card holder.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Investigation, Resolving disputes without network integration, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Provide immediate final credit

Issue immediate final credit to the card holder.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

Based on business rules, the bank can make a determination to issue immediate final credit to the card holder. Immediate final credit can be issued during the Investigation stage.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the **Immediate final credit** activity under the Investigation playbook stage.

7.  Select the immediate final credit task that you want to complete.

8.  On the form, fill in the required fields and any other related information that you have gathered.

9.  In the **Work notes** field, enter any comments.

10. After you have entered the details in the task, select **Update**.

11. Close the task from the playbook.

    |Dispute activity|Action|
    |----------------|------|
    |**To close the Immediate final credit task**|Select **Close**.|


## Result

The task state updates to Closed Complete. The dispute transaction moves to the Chargeback stage.

**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

