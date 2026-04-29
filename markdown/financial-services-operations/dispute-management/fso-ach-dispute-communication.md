---
title: Dispute communication initiation
description: Initiate customer communication after the final decision on ACH dispute resolution is completed.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Processing an ACH dispute, Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Dispute communication initiation

Initiate customer communication after the final decision on ACH dispute resolution is completed.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

**Note:** When the ACH disputes resolution agentic workflow in Now Assist for FSO is enabled, the dispute communication AI Agent is available to assist you at this step. See [Dispute communication AI agent](../../fso-now-assist/task/dispute-communication-ai.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID.

7.  In Open Tasks, select **Dispute communication initiation**.

8.  In the email composer or by selecting the customer's email, compose the message to be sent.

9.  If more information is being requested from ODFI, indicate the **Merchant response** received after ODFI's reply:

    -   **Declined dispute**: The merchant declines the dispute as invalid.
    -   **Accepted dispute**: The merchant accepts the dispute as valid.
10. If the dispute is denied, indicate the **Customer response** received after the customer's reply:

    -   **Accepted**: The customer accepts that the dispute has been denied.
    -   **Denied**: The customer denies the dispute decision and is asked to provide support documents to strengthen their claim.
11. Enter any customer feedback or remarks.

12. Close the task.


**Parent Topic:**[Processing an ACH dispute](../concept/process-dispute-ach.md)

