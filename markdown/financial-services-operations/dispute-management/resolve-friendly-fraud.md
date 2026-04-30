---
title: Detect friendly fraud
description: Detect friendly fraud and determine the course of actions required depending on the amount being disputed, the customer relationship, and the outcome of the detection logic.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-03-26"
reading_time_minutes: 3
breadcrumb: [Investigating a dispute, Working on a dispute case, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Detect friendly fraud

Detect friendly fraud and determine the course of actions required depending on the amount being disputed, the customer relationship, and the outcome of the detection logic.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

Friendly fraud occurs when a consumer makes a legitimate purchase but later disputes the transaction, claiming it was unauthorized or that they didn't receive the product or service. To detect friendly fraud accurately, a set of predefined rules is applied to disputed transactions.

By default, transactions are flagged for friendly fraud if they:

-   Took place with the same merchant.
-   Were conducted using Visa cards.
-   Were made on the same card account.
-   Occur within 120 to 365 days from each other.
-   Have no active fraud reports or disputes.
-   Have at least two matching core data elements \(User ID, IP address, shipping address, device ID/fingerprint\), with one being either IP address or device ID/fingerprint.

The dispute agent can decline requests, issue credits, or proceed with chargebacks, along with modifying communication templates for customer interaction.

Dispute agents can also use the Help resolve friendly fraud disputes agentic workflow in Now Assist for FSO to provide suggested actions and draft customer responses.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  Select the transaction ID in the transaction level playbook of the **Processing** tab.

    The **Investigate** stage is initiated for the transaction.

7.  If a friendly fraud is detected based on the rules defined for the fraud, the **Detect friendly fraud** activity appears in the **Investigate** stage.

8.  The transaction details along with the **Evidence** are displayed.

    If the Friendly fraud AI Agent in Now Assist for FSO is enabled and is triggered based on the rules in the agentic workflow, then the AI agent provides a recommendation for the dispute along with a valid reason. The AI agent guides the dispute agent using the Now Assist panel to select the appropriate action and provide the reasons for the selection of options.

    For more information, see [Using agentic workflows in Now Assist for Financial Services Operations \(FSO\)](../../fso-now-assist/concept/using-ai-agent-use-cases-in-now-assist-for-fso.md).

9.  Select one of the following options.

<table id="choicetable_z24_15n_52c"><thead><tr><th align="left" id="d88209e231">

Action

</th><th align="left" id="d88209e234">

Result

</th></tr></thead><tbody><tr><td id="d88209e240">

**Decline dispute transaction**

</td><td>

1.  Provide the reason for the decline and select **Mark Complete.**
2.  The next activity **Customer communication** is displayed. See [Customer communication](resolve-fraud-customer-communication.md).


</td></tr><tr><td id="d88209e270">

**Issue credit and write-off**

</td><td>

1.  Provide the **Resolution reason**.
2.  Select **Mark complete**.

The **Issue credit** activity is displayed.

3.  Provide the final credit and select **Close task**. The task is marked as **Closed Complete.**
.

</td></tr><tr><td id="d88209e306">

**Proceed with dispute**

</td><td>

The **Report fraud** activity is displayed. Follow the further steps to resolve the fraud. For more information, see [Report fraud to a card network](report-fraud-to-card-network.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Investigating a dispute](investigate-a-dispute.md)

**Related topics**  


[Now Assist for Financial Services Operations \(FSO\)](../../fso-common/concept/now-assist-for-financial-services-operations.md)

[Resolve friendly fraud by using agentic AI](../../fso-now-assist/task/resolve-friendly-fraud-using-agentic-ai.md)

