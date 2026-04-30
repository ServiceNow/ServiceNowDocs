---
title: Investigate stage
description: The Investigate stage of the card dispute playbook, perform tasks such as issuing provisional credit, reviewing participating merchant alerts, and investigating the transaction.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Processing a Visa dispute, Resolving disputes with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Investigate stage

The **Investigate** stage of the card dispute playbook, perform tasks such as issuing provisional credit, reviewing participating merchant alerts, and investigating the transaction.

The dispute agent manages disputed transactions through various activities in the transaction playbook. The **Investigate** stage of the card dispute playbook includes the following key activities:

|Activity|Description|
|--------|-----------|
|[Report fraud](../task/report-fraud-visa.md)|Fraud report activity, when the dispute category is **Fraud**.|
|[Issue provisional credit](../task/issue-provisional-credit-visa.md)|Provisional credit for transactions that qualify for IPC.|
|[Determine recovery option for providing final credit](../task/recovery-option-for-final-credit-visa.md)|Recovery options for transactions that qualify for immediate final credit \(IFC\).|
|[Provide immediate final credit](../task/provide-immediate-final-credit-visa.md)|Final credit for transactions qualifying for IFC after setting the recovery option.|
|[Review participating merchant alerts for Visa disputes](../task/alert-merchant-regarding-dispute-visa.md)|Merchant alerts and options **Declined dispute** to proceed or **Accepted dispute** to end the life cycle and move to closure.|
|[Investigate Visa transactions](../task/manually-investigate-disputed-transaction-visa.md)|Transaction investigation and options to pursue chargeback or end the life cycle for the transaction.|

If the chargeback eligibility rules are evaluated as ineligible and **Pursue chargeback** is set to **Yes**, the system triggers an approval request for the dispute manager. The manager reviews the approval task and can select **Approve** to proceed further or select **Reject** to return to the investigation task. After the manager approves, the dispute agent proceeds with the dispute case.

-   **[Issue provisional credit](../task/issue-provisional-credit-visa.md)**  
Initiate temporary provisional credit to the Visa card holder.
-   **[Determine recovery option for providing final credit](../task/recovery-option-for-final-credit-visa.md)**  
Complete the Recovery option task to choose whether to pursue chargeback for a Visa transaction where final credit to the card customer will be provided.
-   **[Provide immediate final credit](../task/provide-immediate-final-credit-visa.md)**  
Issue immediate final credit to the Visa card holder.
-   **[Review participating merchant alerts for Visa disputes](../task/alert-merchant-regarding-dispute-visa.md)**  
Alert the merchant about a Visa card transaction dispute.
-   **[Investigate Visa transactions](../task/manually-investigate-disputed-transaction-visa.md)**  
If a merchant refuses a transaction dispute, the case may move to the manual investigation task.

**Parent Topic:**[Processing a dispute case with the Card Dispute Transaction playbook](processing-a-dispute-case.md)

**Related topics**  


[Report fraud](../task/report-fraud-visa.md)

[Issue provisional credit](../task/issue-provisional-credit-visa.md)

[Determine recovery option for providing final credit](../task/recovery-option-for-final-credit-visa.md)

[Provide immediate final credit](../task/provide-immediate-final-credit-visa.md)

[Review participating merchant alerts for Visa disputes](../task/alert-merchant-regarding-dispute-visa.md)

[Investigate Visa transactions](../task/manually-investigate-disputed-transaction-visa.md)

