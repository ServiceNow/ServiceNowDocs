---
title: Investigate Mastercard dispute
description: The Investigate stage displays the dispute tasks related to investigating the Mastercard transaction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/investigate-mastercard-dispute.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Investigate Mastercard dispute

The Investigate stage displays the dispute tasks related to investigating the Mastercard transaction.

The **Investigate** stage of the disputed transaction includes the following tasks:

|Task|Description|
|----|-----------|
|[Report fraud to card network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/report-fraud-mc.md)|Used to report fraud to the card network. This task is displayed when the dispute category is **Fraud**.|
|[Make a decision on chargeback, write off, or transaction denial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/make-decision-on-chargeback.md)|Task for a recovery option and choose whether to pursue chargeback for a transaction.|
|[Alert merchant regarding dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/alert-merchant-dispute-mc.md)|Task to review merchant response regarding the dispute. The merchant can choose to resolve the disputed transaction or decline to resolve the dispute.|
|[Investigate the dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/investigate-dispute-mc.md)|Task to investigate the transaction and decide whether to pursue chargeback or end the life cycle for the transaction.|

|Task|Description|
|----|-----------|
|[Issue provisional credit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/issue-provisional-credit-mc.md)|Task to provide provisional credit for transaction that qualifies for Immediate provisional credit.|
|[Provide final credit to customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/provide-final-credit-mc.md)|Task to issue final credit if the policy is Immediate final credit for the transaction.|
|[Reverse provisional credit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/reverse-provisional-credit-mc.md)|Task to reverse the temporary credit issued by the bank to the card holder.|
|[Convert provisional credit to final credit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/convert-provisional-credit-to-final-credit_mc.md)|Task to convert the provisional credit that was issued previously to the cardholder.|
|Issue final credit and write off|Action to issue final credit and write off. If **Yes**, provide final credit to the cardholder and the dispute life cycle ends. If **No**, no credit is given and the dispute life cycle ends.|

If the chargeback eligibility rules are evaluated as ineligible and **Pursue chargeback** is set to **Yes**, the system triggers an approval request for the dispute manager. The manager reviews the approval task and can select **Approve** to proceed further or **Reject** to return to the investigation task. After the manager approves, the dispute agent proceeds with the dispute case.

**Parent Topic:**[Processing a Mastercard dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/processing-mastercard-dispute-case.md)

