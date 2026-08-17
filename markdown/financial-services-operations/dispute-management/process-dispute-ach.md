---
title: Processing an ACH dispute
description: On the Processing tab of the card disputes playbook, all disputed transactions in an ACH dispute case are displayed on a dashboard. The tab also provides transaction information such as dispute amount, transaction date and time, merchant, transaction state, current activity, and activity SLA.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/process-dispute-ach.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
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
</table>## Using AI agents in ACH disputes processing

Several of the tasks in the Investigate stage can be assisted by an AI agent. Each AI agent is scoped to a single task and can be enabled or disabled independently, so a case can move through a mix of AI-assisted and manually completed tasks.

Once a dispute agent is assigned to a case and its related transactions, either automatically through your Advanced Work Assignment \(AWA\) configuration or manually by selecting **Assign to me** on a specific task, any AI agent enabled for that task is invoked automatically.

**Note:** Ensure that your assignment logic, such as AWA, is configured so that when a dispute case is assigned to an agent, all associated transactions are automatically assigned to the same agent. This alignment helps maintain consistency and speeds up case resolution.

Each AI agent draws on the same set of resources to form its recommendation:

-   Knowledge base \(KB\) articles, such as the reason-code and eligibility rules installed with the Nacha dispute content pack
-   The ACH dispute's task details
-   Previous ACH dispute cases

When an AI agent completes its analysis, the dispute agent reviews the recommendation and chooses one of these options on the workspace:

-   **Apply Recommendation**: Accept the AI agent's recommendation. The recommended outcome and rationale are copied into the task's final action and resolution reason fields, and the task closes.
-   **Ask a follow up**: Ask the AI agent to clarify or expand on its analysis in the ServiceNow Otto panel before deciding.

A dispute agent can also decide not to follow a recommendation. In that case, the AI agent prompts for a rationale for the disagreement before the task proceeds.

The following AI agents can assist with ACH dispute processing:

-   Merchant analysis with AI agent: Checks merchant credibility using web search ratings and reviews and past dispute history. See [Evaluate merchant analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-evaluate-merchant.md).
-   Nacha operating guidelines check AI agent: Verifies that a disputed transaction meets Nacha rules and timelines, including required documentation such as a valid Written Statement of Unauthorized Debit \(WSUD\). See [Evaluate Nacha operating guidelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-evaluate-nacha.md).
-   ACH dispute return recommendation AI agent: Reviews past disputes with similar transaction values and recommends a final action \(Deny, File return, or Follow up with ODFI\). See [Review ACH dispute return recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-review-recommendation.md).
-   Dispute communication AI agent: Selects an appropriate email template, drafts the customer or ODFI communication, and lets the dispute agent review it before sending. See [Dispute communication initiation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-dispute-communication.md).

If an AI agent isn't enabled for a task, the dispute agent completes that task manually, as described in the corresponding task topic.

-   **[Evaluate merchant analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-evaluate-merchant.md)**  
Evaluate a merchant's credibility to determine whether the transaction is legitimate or potentially fraudulent before deciding on a resolution. When the ACH disputes AI agent workflow is enabled, an AI agent can perform this analysis automatically based on merchant reviews and past dispute history.
-   **[Issue provisional credit to customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-provide-credit.md)**  
Provide a temporary provisional credit to the account holder while the ACH dispute is investigated.
-   **[Evaluate Nacha operating guidelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-evaluate-nacha.md)**  
Evaluate the Nacha operating guidelines to ensure that the ACH dispute qualifies for potential reimbursement. When enabled, the Nacha operating guidelines check AI agent can verify eligibility automatically based on documents such as a valid Written Statement of Unauthorized Debit \(WSUD\).
-   **[Review ACH dispute return recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-review-recommendation.md)**  
Review the ACH dispute information based on merchant analysis and Nacha eligibility recommendations and determine the final action. When the ACH dispute return recommendation AI agent is enabled, it can analyze past disputes with similar transaction values and recommend an action for you.
-   **[Dispute communication initiation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-dispute-communication.md)**  
Initiate customer communication after the final decision on ACH dispute resolution is completed. When the dispute communication AI agent is enabled, it can automatically select an email template, draft the message, and let you review it before sending.
-   **[Verify customer supporting documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-verify-customer-documents.md)**  
After following up with the customer to request further documentation about the dispute, verify the supporting documents that you received.
-   **[Verify ODFI supporting documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-verify-odfi.md)**  
After following up with the Originating Depository Financial Institution \(ODFI\) to request further documentation about the dispute, verify the supporting documents that you received.
-   **[File ACH return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-file-refund.md)**  
File a return to ODFI for a disputed transaction if it has been determined to be eligible for a refund.
-   **[Settle payment with customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-settle-payment.md)**  
Complete the financial adjustment so the customer receives the correct funds after the dispute is resolved.
-   **[Reverse provisional credit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/fso-ach-dispute-reverse-provisional.md)**  
Reverse the temporary credit issued by the bank to the account holder.

**Parent Topic:**[Resolving ACH disputes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/work-dispute-ach.md)

**Related topics**  


[Dispute Reason Codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/components-installed-with-dispute-rules-content-pack-for-nacha.md)

