---
title: Chargeback in Mastercard transaction disputes
description: After a chargeback is initiated, the chargeback request is sent to Mastercard, which alerts the merchant. Mastercard requests collaboration from merchants, who either provide a voucher, refund, or First-Party Trust evidence as response. If the merchant doesn’t respond, the process escalates to formal chargeback procedures.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Chargeback in Mastercard transaction disputes

After a chargeback is initiated, the chargeback request is sent to Mastercard, which alerts the merchant. Mastercard requests collaboration from merchants, who either provide a voucher, refund, or First-Party Trust evidence as response. If the merchant doesn’t respond, the process escalates to formal chargeback procedures.

## Chargeback stages

The Chargeback stage in Mastercard is described in these stages:

1.  **Initiation of chargeback and collaboration**:
    -   The agent initiates a chargeback request with Mastercard.
    -   When Mastercard receives the chargeback request, it first attempts to resolve the dispute informally by connecting the merchant and the cardholder directly through a collaboration step that is supported by Ethoca's collaboration services. The merchant and the cardholder have to collaborate and resolve the dispute within a time frame of 72 hours.
    -   If the merchant accepts the collaboration request, the [Review and respond to collaboration](../task/review-respond-collaboration.md) task displays.
    -   If the merchant doesn’t respond or collaborate within the 72-hour time frame, Mastercard proceeds with the chargeback process and informs the merchant's bank with the chargeback request.
    -   The merchant then has the option to initiate a second presentment request.
2.  **Second presentment review**
    -   If the merchant submits documentation to contest the dispute, the agent reviews the response. The task [Review chargeback response and decide on pre-arbitration or arbitration](../task/review-and-decide-prearbitration.md) is displayed.
    -   Based on the review, either of the following applies:
        -   The agent accepts the second presentment.
        -   The agent escalates the case to pre-arbitration or arbitration.
        -   If the merchant doesn't respond within the specified time frame, the agent manually acts on the disputed transaction based on Mastercard's response that displays on the agent's **Landing page**

            **Note:** The agent can access Mastercard's response from **Landing Page** &gt; **Acquirer deadline expired tasks**. For more information, see [Dispute agent workspace](workspace-for-agent.md)


## Submitting supporting documents

Agents attach supporting documents as a `.zip` file for each task in the Chargeback stage as required.

When integrated with Mastercard's Mastercom APIs, the system automates the submission of supporting documents for each task throughout the Chargeback stage. It automatically checks attached files against Mastercard requirements for file type and size. When agents submit multiple attachments, the system compresses them into a single zip file and alerts the agent when any attachment doesn’t meet Mastercard requirements. For more information, see [Mastercard document requirements](../../fso-mastercard/reference/mastercard-image-and-document-requirements.md).

-   **[Initiate chargeback](../task/initiate-chargeback-mastercard.md)**  
Initiate a chargeback for Mastercard transaction disputes and request collaboration from merchants.
-   **[Review and respond to collaboration](../task/review-respond-collaboration.md)**  
The merchant responds to the collaboration by either providing a refund, a voucher, or a First-Party Trust evidence. If the collaboration isn’t successful, then the second presentment is awaited.
-   **[Review chargeback response and decide on pre-arbitration or arbitration](../task/review-and-decide-prearbitration.md)**  
Review second presentment for the chargeback and initiate pre-arbitration or arbitration, as required for the dispute workflow of the Chargeback stage. For Mastercard transaction chargeback, you can skip raising the pre-arbitration and directly raise the arbitration request.
-   **[Review pre-arbitration response and escalate to arbitration](../task/review-prearbitration-response-escalate-arbitration.md)**  
After you raised a pre-arbitration request in the Chargeback stage of Mastercard transaction dispute, review the response and decide whether to accept, reject, or escalate the pre arbitration to arbitration.
-   **[Review arbitration response](../task/review-arbitration-response-mc.md)**  
Review the arbitration response received from Mastercard and proceed to resolve the dispute. This step occurs in the Mastercard dispute process when you’ve escalated from pre‑arbitration to arbitration or skipped pre‑arbitration and moved directly into arbitration.
-   **[Reverse provisional credit](../task/reverse-provisional-credit-mc.md)**  
Reverse the temporary credit issued by the bank to the card holder.
-   **[Provide final credit to customer](../task/provide-final-credit-mc.md)**  
Issue immediate final credit to the card holder.
-   **[Convert provisional credit to final credit](../task/convert-provisional-credit-to-final-credit_mc.md)**  
Convert the provisional credit that was issued previously to a customer to a final credit issuance.

**Parent Topic:**[Processing a Mastercard dispute](processing-mastercard-dispute-case.md)

