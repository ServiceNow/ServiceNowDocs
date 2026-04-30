---
title: Processing an ACH dispute
description: On the Processing tab of the card disputes playbook, all disputed transactions in an ACH dispute case are displayed on a dashboard. The tab also provides transaction information such as dispute amount, transaction date and time, merchant, transaction state, current activity, and activity SLA.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 3
breadcrumb: [Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Processing an ACH dispute

On the **Processing** tab of the card disputes playbook, all disputed transactions in an ACH dispute case are displayed on a dashboard. The tab also provides transaction information such as dispute amount, transaction date and time, merchant, transaction state, current activity, and activity SLA.

The Investigate stage displays the dispute tasks related to investigating the disputed ACH transaction.

The Investigate stage of the disputed transaction includes the following tasks:

<table id="table_wc4_vr4_fhc"><tbody><tr><td>

**Task**

</td><td>

**Description**

</td></tr><tr><td>

Evaluate merchant analysis

</td><td>

Evaluate the merchant credibility to help validate the disputed ACH transaction.

</td></tr><tr><td>

Provide provisional credit to customer

</td><td>

Provide a temporary provisional credit to the account holder while the dispute is investigated.

</td></tr><tr><td>

Evaluate Nacha guidelines

</td><td>

Evaluate the Nacha \(National Automated Clearing House Association\) operating guidelines to verify that a disputed ACH transaction meets the Nacha operating rules for return eligibility by verifying required documentation such as a valid Written Statement of Unauthorized Debit \(WSUD\).

</td></tr><tr><td>

Review ACH dispute return recommendation

</td><td>

Review the ACH dispute information and determine the final action.-   Deny: The ACH dispute is determined to be invalid and is denied. The provisional credit is reversed.
-   File return: The ACH dispute is determined to be valid and meets eligibility for return. A refund is initiated.
-   Follow up ODFI: More information is required from the ODFI before a refund can be either denied or issued.

</td></tr><tr><td>

Dispute communication initiation

</td><td>

Provide a response and feedback to the customer for a decision made on a dispute.This communication is sent to customers if the final action taken is either **File return** or **Deny** customer. If **Follow up ODFI** is the final action, the communication is sent to ODFI \(Originating Depository Financial Institution\).

</td></tr><tr><td>

Verify customer supporting documents

</td><td>

After communicating dispute denial to a customer, if a customer denies the decision to decline a dispute, they’ll be asked to provide support documentation along with their response. Verify the supporting documents that you received from the customers.

</td></tr><tr><td>

Verify ODFI supporting documents

</td><td>

After following up with ODFI \(Originating Depository Financial Institution\) to request further documentation about the dispute, verify the supporting documents that you received.

</td></tr><tr><td>

File ACH return

</td><td>

File a refund for an ACH dispute when the dispute has been determined to be eligible.

</td></tr><tr><td>

Settle payment with customer

</td><td>

Complete the financial adjustment so that the customer receives the appropriate funds after the dispute is resolved.

</td></tr><tr><td>

Reverse provisional credit

</td><td>

Reverse the temporary credit issued by the bank to the account holder in case of denial.

</td></tr></tbody>
</table>-   **[Evaluate merchant analysis](../task/fso-ach-evaluate-merchant.md)**  
Evaluate a merchant's credibility to determine whether the transaction is legitimate or potentially fraudulent before deciding on a resolution.
-   **[Issue provisional credit to customer](../task/fso-ach-provide-credit.md)**  
Provide a temporary provisional credit to the account holder while the ACH dispute is investigated.
-   **[Evaluate Nacha operating guidelines](../task/fso-ach-evaluate-nacha.md)**  
Evaluate the Nacha \(National Automated Clearing House Association\) operating guidelines to ensure that the ACH dispute qualifies for potential reimbursement.
-   **[Review ACH dispute return recommendation](../task/fso-ach-review-recommendation.md)**  
Review the ACH dispute information based on merchant analysis and Nacha eligibility recommendations and determine the final action.
-   **[Dispute communication initiation](../task/fso-ach-dispute-communication.md)**  
Initiate customer communication after the final decision on ACH dispute resolution is completed.
-   **[Verify customer supporting documents](../task/fso-ach-verify-customer-documents.md)**  
After following up with the customer to request further documentation about the dispute, verify the supporting documents that you received.
-   **[Verify ODFI supporting documents](../task/fso-ach-verify-odfi.md)**  
After following up with the Originating Depository Financial Institution \(ODFI\) to request further documentation about the dispute, verify the supporting documents that you received.
-   **[File ACH return](../task/fso-ach-file-refund.md)**  
File a return to ODFI for a disputed transaction if it has been determined to be eligible for a refund.
-   **[Settle payment with customer](../task/fso-ach-settle-payment.md)**  
Complete the financial adjustment so the customer receives the correct funds after the dispute is resolved.
-   **[Reverse provisional credit](../task/fso-ach-dispute-reverse-provisional.md)**  
Reverse the temporary credit issued by the bank to the account holder.

**Parent Topic:**[Resolving ACH disputes](work-dispute-ach.md)

