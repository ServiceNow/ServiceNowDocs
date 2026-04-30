---
title: Allocation dispute workflow
description: In the allocation workflow, dispute agents work to resolve fraud and authorization disputes. Acquirers can choose to initiate pre-arbitration and arbitration, and issuers can respond. This is a part of the allocation dispute workflow for the Chargeback stage.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Chargeback, Processing a Visa dispute, Resolving disputes with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Allocation dispute workflow

In the allocation workflow, dispute agents work to resolve fraud and authorization disputes. Acquirers can choose to initiate pre-arbitration and arbitration, and issuers can respond. This is a part of the allocation dispute workflow for the Chargeback stage.

The transaction playbook helps dispute agents in handling **Fraud** and **Authorization** within the Visa allocation workflow. The playbook includes key activities such as initiating chargebacks, reviewing dispute responses, and managing pre-arbitration and arbitration tasks. The following table outlines the use case steps in this process.

<table id="table_kbh_msz_m2c"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Initiate chargeback and fill merchant response](../task/initiate-chargeback-and-fill-merchant-response.md)

</td><td>

Initiates the chargeback process and submits the dispute questionnaire to Visa.

</td></tr><tr><td>

[Review and respond to a pre-arbitration request](../task/review-and-respond-to-pre-arbitration.md)

</td><td>

1.  After the batch queue is triggered, the incoming pre-arbitration is reviewed and moves the transaction to the appropriate state. For more information on how to configure the batch queue, see [Configure the Visa Queue Scheduler Flow](../../fso-visa-spoke/task/activate-visa-queue-scheduler-flow.md)
2.  Reviews and responds to pre-arbitration details.

</td></tr><tr><td>

[Review a case filing response and appeal the decision](../task/review-case-filing-response-and-appeal.md)

</td><td>

1.  After the batch queue is triggered, receives an update about incoming arbitration.
2.  Reviews the arbitration and waits for the decision.
3.  When the batch queue is triggered again, receives an update about decision from Visa.
4.  Based on ruling from Visa, decides to go for an appeal.

 **Note:** An appeal can be created by either the acquirer or issuer.

</td></tr><tr><td>

[Review the case filing appeal](../task/review-case-filing-appeal.md)

</td><td>

1.  After the batch queue is triggered, receives an update on the appeal and moves the transaction to the appropriate state.
2.  Reviews the appeal decision letter and decides if the dispute should be resolved or if further action is needed.

</td></tr><tr><td>

[Convert provisional credit to final credit](../task/convert-provisional-credit-to-final-credit_visa.md)

</td><td>

Converts provisional credit to final credit if applicable and closes the task.

</td></tr><tr><td>

[Reverse provisional credit](../task/reverse-provisional-credit_0.md)

</td><td>

Reverses the provisional credit only for Imediate Provisional Credit, provided **Reverse** is selected in the previous task, and then closes the task.

</td></tr></tbody>
</table>-   **[Initiate chargeback and fill merchant response- Allocation workflow](../task/initiate-chargeback-and-fill-merchant-responseallocation_0.md)**  
This is a part of the allocation dispute workflow for the **Chargeback** stage. Initiate a chargeback request for the card network issuer to credit the card holder with the card network, and await a response from the merchant.
-   **[Review and respond to a pre-arbitration request](../task/review-and-respond-to-pre-arbitration.md)**  
Review and respond to the pre-arbitration request created by the acquirer.
-   **[Review incoming case filing and appeal](../task/review-incoming-case-filing-and-appeal.md)**  
Review the incoming case filing created by the acquirer and create an appeal if required.
-   **[Review the case filing appeal](../task/review-case-filing-appeal.md)**  
Review the appeal and get an acknowledgment from Visa for the appeal.

**Parent Topic:**[Chargeback stage](chargeback-stage.md)

