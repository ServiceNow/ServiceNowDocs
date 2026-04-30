---
title: Investigate stage
description: In the Investigate stage of the card dispute playbook, perform tasks such as issuing provisional credit, reviewing participating merchant alerts, and investigating the transaction.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-03-03"
reading_time_minutes: 1
breadcrumb: [Processing a dispute case with the Card Dispute Transaction playbook, Working on a dispute case integrated with Visa, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Investigate stage

In the **Investigate** stage of the card dispute playbook, perform tasks such as issuing provisional credit, reviewing participating merchant alerts, and investigating the transaction.

The dispute agent manages disputed transactions through various activities in the transaction playbook. The **Investigate** stage of the card dispute playbook for Visa transactions includes the following key activities:

|Activity|Description|
|--------|-----------|
|[Report fraud](../task/report-fraud.md)|Fraud report activity, when the dispute category is **Fraud**.|
|[Issue provisional credit](../task/provide-provisional-credit-to-customer.md)|Provisional credit for transactions that qualify for IPC.|
|[Set recovery option](../task/recovery-option-for-final-credit.md)|Recovery options for transactions that qualify for immediate final credit \(IFC\).|
|[Immediate Final credit \(IFC\)](../task/provide-immediate-final-credit.md)|Final credit for transactions qualifying for IFC after setting the recovery option.|
|[Review participating merchant alerts](../task/alert-merchant-regarding-dispute.md)|Merchant alerts and options **Declined dispute** to proceed or **Accepted dispute** to end the life cycle and move to closure.|
|[Investigate transactions](../task/manually-investigate-disputed-transaction.md)|Transaction investigation and options to pursue chargeback or end the life cycle for the transaction.|

If the chargeback eligibility rules are evaluated as ineligible and **Pursue chargeback** is set to **Yes**, the system prompts an approval request for the dispute manager. The manager reviews the approval task and can select **Approve** to proceed further or select **Reject** to return to the investigation task. After the manager approves, the dispute agent proceeds with the dispute case.

**Parent Topic:**[Processing a dispute case with the Card Dispute Transaction playbook](processing-a-dispute-case.md)

