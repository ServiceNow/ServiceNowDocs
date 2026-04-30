---
title: Collaboration dispute workflow
description: In the collaboration workflow, dispute agents work to resolve consumer disputes and processing errors. In this workflow, issuers can choose to initiate pre-arbitration and arbitration, and acquirers can respond to these events.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-03-03"
reading_time_minutes: 4
breadcrumb: [Chargeback stage, Processing a dispute case with the Card Dispute Transaction playbook, Working on a dispute case integrated with Visa, Managing dispute service requests, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Collaboration dispute workflow

In the collaboration workflow, dispute agents work to resolve consumer disputes and processing errors. In this workflow, issuers can choose to initiate pre-arbitration and arbitration, and acquirers can respond to these events.

The transaction playbook helps dispute agents in handling **Consumer disputes** and **Processing errors** within the Visa collaboration workflow. The playbook includes key activities such as initiating chargebacks, reviewing dispute responses, and managing pre-arbitration and arbitration tasks.

<table id="table_kbh_msz_m2c"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Initiate chargeback and fill merchant response](../task/initiate-chargeback-and-fill-merchant-response.md)

</td><td>

1.  The chargeback process gets initiated and the merchant response is submitted Visa for review.
2.  After the batch queue is triggered, the transaction moves to **Work in progress**. For more information on how to configure the batch queue, see [Configure the Visa Queue Scheduler Flow](../../fso-visa-spoke/task/activate-visa-queue-scheduler-flow.md).

</td></tr><tr><td>

[Associate dispute transaction](associate-dispute-transaction.md)

</td><td>

Associated transactions and the dispute response, determine if pre-arbitration is required.

</td></tr><tr><td>

[Review dispute response and create pre-arbitration](../task/review-dispute-response-and-create-pre-arbitration.md)

</td><td>

1.  Merchant response review for the dispute and initiate pre-arbitration.
2.  After the batch queue is triggered, the pre-arbitration responses are received.

</td></tr><tr><td>

[Review the pre-arbitration response and create a case filing](../task/review-pre-arbitration-response-and-create-case-filing.md)

</td><td>

1.  Pre-arbitration response review and if unresolved, determine whether to file an arbitration.
2.  After the batch queue is triggered, the response for arbitration is received and the transaction moves to **Work in progress**.

</td></tr><tr><td>

[Review a case filing response and appeal the decision](../task/review-case-filing-response-and-appeal.md)

</td><td>

1.  Arbitration decision review and, if unresolved, decide to proceed with an appeal.
2.  After the batch queue is triggered, response for arbitration is received, moving the transaction to **Work in progress**.

 **Note:** Appeal can be created by either the acquirer or issuer.

</td></tr><tr><td>

[Review the case filing appeal](../task/review-case-filing-appeal.md)

</td><td>

Appeal decision review and mark the response as resolved or unresolved, determining next steps for the transaction.

</td></tr><tr><td>

[Convert provisional credit to final credit](../task/convert-provisional-credit-to-final-credit_0.md)

</td><td>

Conversion of provisional credit into final credit once the case is resolved, and close the task.

</td></tr><tr><td>

[Reverse provisional credit](../task/reverse-provisional-credit_0.md)

</td><td>

Reversal of provisional credit only for Immediate Provisional Credit, provided **Reverse** is selected in the previous task. After this, close the task.

</td></tr></tbody>
</table>-   **[Initiate chargeback and fill merchant response](../task/initiate-chargeback-and-fill-merchant-response.md)**  
This is a part of the collaboration dispute workflow for the **Chargeback** stage. Initiate a chargeback request for the card network issuer to credit the customer with the card network and await a response from the merchant.
-   **[Associate dispute transaction](associate-dispute-transaction.md)**  
List associated transactions identified by Visa after the chargeback creation. Review these transactions and associate them with the disputed transaction to help deflect and resolve the dispute in the next activity.
-   **[Review dispute response and create pre-arbitration](../task/review-dispute-response-and-create-pre-arbitration.md)**  
Review a merchant’s response for the dispute and initiate pre-arbitration, if necessary for the collaboration dispute workflow of the Chargeback stage.
-   **[Review the pre-arbitration response and create a case filing](../task/review-pre-arbitration-response-and-create-case-filing.md)**  
Review the merchant’s response to the pre-arbitration and create a case filing.
-   **[Review a case filing response and appeal the decision](../task/review-case-filing-response-and-appeal.md)**  
An appeal can be created by the issuer or acquirer if either party isn’t satisfied with the arbitration ruling from Visa. Review the case filing response and receive the decision letter from Visa.
-   **[Review the case filing appeal](../task/review-case-filing-appeal.md)**  
Review the appeal and get an acknowledgment from Visa for the appeal.
-   **[Convert provisional credit to final credit](../task/convert-provisional-credit-to-final-credit_0.md)**  
Convert the provisional credit that was issued previously to a customer to a final credit issuance.
-   **[Reverse provisional credit](../task/reverse-provisional-credit_0.md)**  
Reverse the temporary credit issued by the bank to the card holder.

**Parent Topic:**[Chargeback stage](chargeback-stage.md)

