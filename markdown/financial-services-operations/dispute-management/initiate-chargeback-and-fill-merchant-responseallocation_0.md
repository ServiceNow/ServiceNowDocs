---
title: Initiate chargeback and fill merchant response- Allocation workflow
description: This is a part of the allocation dispute workflow for the Chargeback stage. Initiate a chargeback request for the card network issuer to credit the card holder with the card network, and await a response from the merchant.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Allocation workflow, Chargeback, Processing a Visa dispute, Resolving disputes with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Initiate chargeback and fill merchant response- Allocation workflow

This is a part of the allocation dispute workflow for the **Chargeback** stage. Initiate a chargeback request for the card network issuer to credit the card holder with the card network, and await a response from the merchant.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

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

7.  Select the **Initiate chargeback and fill merchant response** activity.

8.  The chargeback reason code and dispute amount is displayed.

9.  Submit the request by selecting **Initiate chargeback**.


## Result

The questionnaire data from the Initiate stage is sent to Visa. The task is set to the **Awaiting External Info** state, and the form is set to read-only during this waiting period. Once you receive the response, the transaction state changes to **Work in Progress**. The activity stream displays whether the request to Visa was successful. If the request fails, the **Retrigger** option appears to retry.

## What to do next

1.  After you initiate the chargeback for the dispute, if the acquirer is not happy, they can initiate pre arbitration. The **Incoming pre arbitration received** field is set to **Yes** or **No** and the next activity [Review and respond to a pre-arbitration request](review-and-respond-to-pre-arbitration.md) is displayed.
2.  Select **Close task**.

**Parent Topic:**[Allocation dispute workflow](../concept/allocation-dispute-work-flow.md)

