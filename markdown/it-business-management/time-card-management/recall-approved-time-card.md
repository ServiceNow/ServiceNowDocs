---
title: Recall a processed time card
description: You can recall an incorrect time card in the Approved or Processed state to return it to the submitter. The submitter can then make the necessary changes and resubmit the time card.
locale: en-US
release: xanadu
product: Time Card Management
classification: time-card-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Time cards, Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Recall a processed time card

You can recall an incorrect time card in the Approved or Processed state to return it to the submitter. The submitter can then make the necessary changes and resubmit the time card.

## Before you begin

Role required: timecard\_approver or timecard\_admin

## About this task

The recall option is available only if the **Allow recall** option is selected on the associated [time sheet policy](create-time-sheet-policy.md).

## Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Time Sheet Portal**.

2.  Click the **My Time Sheet** list and select a user under **My Resources**.

3.  Navigate through the **Calendar** widget to select the time sheet.

    The time sheet must be within the recall period specified in the time sheet policy.

4.  To recall a time card, click the more actions icon \(![More actions icon](../../../product/alignment-planner-workspace/images/more-actions-icon.png)\) and select **Recall**.

    If the cost type for a cost plan is updated before recalling a time card, the expense line of the recalled time card will have the new expense type. For example:

    1.  A Time card is processed with Cost Plan=Labor Opex, an expense line is generated for $500 with Expense type=Labor Opex.
    2.  If the cost type of cost plan is updated to Cost type=Labor Capex.
    3.  If a time card is recalled, the recalled expense linewill have Expense type=Labor Capex.

## Result

-   Changes the state of the time card to **Recalled**. The state of the associated time sheet also changes to **Recalled** until all time cards in the time sheet are approved or processed again.
-   Reverts the actual effort and resource hours in a project or demand created when the time card for a task type was approved.
-   Creates negative expense lines to zero out the corresponding expense lines created when the time card was approved.
-   Returns the associated time sheet to its submitter for modifications.

**Parent Topic:**[Time cards](../concept/c_TimeCards.md)

