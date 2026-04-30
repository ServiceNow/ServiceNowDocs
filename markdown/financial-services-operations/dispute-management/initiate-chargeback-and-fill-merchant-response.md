---
title: Initiate chargeback and fill merchant response
description: This is a part of the collaboration dispute workflow for the Chargeback stage. Initiate a chargeback request for the card network issuer to credit the customer with the card network and await a response from the merchant.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-02-28"
reading_time_minutes: 1
breadcrumb: [Collaboration dispute workflow, Chargeback stage, Processing a dispute case with the Card Dispute Transaction playbook, Working on a dispute case integrated with Visa, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Initiate chargeback and fill merchant response

This is a part of the collaboration dispute workflow for the **Chargeback** stage. Initiate a chargeback request for the card network issuer to credit the customer with the card network and await a response from the merchant.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

4.  In the list, select a case that you want to work on.

5.  Select the **Playbook** tab.

6.  In the transaction level playbook of the **Processing** tab, select the transaction ID.

7.  Select the **Initiate chargeback and fill merchant response** activity.

8.  The chargeback reason code and dispute amount is displayed.

9.  Review the details and add any other details.

10. Submit the request by selecting **Initiate chargeback**.


## Result

The questionnaire data from the **Initiate** stage is sent to Visa. The task is set to the **Awaiting External Info** state, and the form is set to read-only during this waiting period. Once you receive the response, the transaction state changes to **Work in Progress**. The activity stream displays whether the request to Visa was successful. If the request fails, the **Retrigger** option appears to retry.

## What to do next

Review the response from the merchant and fill the further details.

1.  After you receive the merchant's response, the **Dispute response** field is set to **Yes** or **No** and the next activity [Review dispute response and create pre-arbitration](review-dispute-response-and-create-pre-arbitration.md) is displayed.
2.  Select **Close task**. The next activity appears based on the selected option.

**Parent Topic:**[Collaboration dispute workflow](../concept/collaboration-dispute-workflow.md)

