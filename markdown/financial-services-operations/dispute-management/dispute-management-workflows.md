---
title: Managing dispute workflows
description: As a card dispute agent or agent connector, you can work on a credit or debit card dispute case by investigating and resolving dispute requests for cardholders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/financial-services-operations/dispute-management/dispute-management-workflows.html
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Understanding Dispute Management, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Managing dispute workflows

As a card dispute agent or agent connector, you can work on a credit or debit card dispute case by investigating and resolving dispute requests for cardholders.

When an agent disputes a transaction on behalf of a customer, it initiates a dispute service case and triggers the dispute transaction flow. This flow includes various tasks specific to the case details.

For credit or debit card dispute management cases, tasks are generated for each transaction that has a dispute request. The playbook guides you through these tasks, ensuring you effectively manage and fulfill them based on investigations and decisions made by parties involved, such as the cardholder, card network, or merchant. With input or decisions from these parties, you, as a dispute agent, will complete activities and tasks within the Initiate, Review,Processing,Investigate, Chargeback, and Closure stages of a dispute case.

## Initiate

When a dispute agent initiates a case, the case begins in the Initiate stage. Dispute cases created using Now Assist for Financial Services Operations \(FSO\) with the Disputes intakes via Virtual Agent skill will also begin in the Initiate stage.

During this phase, you can identify the disputed transaction, add more transactions \(if the dispute category is Fraud\), select associated transactions, complete the dispute questionnaire, and upload any supporting documentation. Dispute cases created using Now Assist for FSO are populated with information collected and inferred from the customer's responses in the Virtual Agent chat.

When a transaction is selected for dispute, you can obtain additional information about the transaction with an integration, such as Ethoca Consumer Clarity and Order Insight Digital Management.

The system evaluates decision rules and determines policy rules for each transaction in the case \(for example, which transaction qualifies for a provisional credit as opposed to a final credit\).

The system generates tasks based on the policy rules that are evaluated when a case is submitted. For instance, when a case has a dispute category of Fraud, the system creates a task to block and reissue the card.

For information about configuring business rules, see [Exploring Decision Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/decision-designer-overview.md).

For information about Now Assist for FSO, see [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md).

## Review

If a dispute case was submitted by a customer via a service portal, the case begins at the Review stage. If the case was initiated by an agent, this stage will be skipped.

The dispute agent reviews the dispute intake, including the disputed transactions, the dispute amount, and the reasons for dispute.

The agent provides answers to any additional questions not answered by the cardholder and to any questions they are expected to address. If the dispute category changes, the system will produce a questionnaire for the newly selected category, which is then filled out by the agent.

After review, the agent submits the case and continues with the subsequent lanes and activities in the case.

The system generates tasks based on the policy rules that are evaluated when a case is submitted. For instance, when a case has a dispute category of Fraud, the system creates a task to block and reissue the card.

## Processing

After the case is submitted, an agent can monitor and progress the disputed transactions in the Processing stage. This stage presents an overview of the overall case and tracks the status of each transaction and its related tasks.

Each disputed transaction in the case is displayed in this view as a separate card. Each card contains the following information:

-   Card disputes transaction number
-   The stage at which the disputed transaction is at \(Investigate, Chargeback, or Complete\)
-   Whether the transaction is card present or card not present
-   Dispute amount
-   Transaction date
-   Merchant type
-   Transaction status
-   Current activity
-   Activity SLA

## Investigate

This stage applies for each disputed transaction in a case. You can access this stage by opening a disputed transaction in the Processing stage of the playbook.

During this stage, the card network, card issuing bank, merchant bank or acquirer, and merchant engage in review processes to make final determinations for each transaction. In this stage, you can [alert the merchant to a card transaction dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/dispute-management/alert-merchant-regarding-dispute.md). If a merchant declines a disputed transaction, then a task to [Investigate transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/dispute-management/manually-investigate-disputed-transaction.md) is created.

The card dispute rules for Internal Policy decision table automates decisions for the transaction such as:

-   Deny: The dispute for the transaction is denied.
-   Immediate final credit: This decision provides final credit immediately to the cardholder. For example, if the disputed transaction amount is below $25 USD, a bank's business rule may choose to initiate immediate final credit. If immediate final credit is decided, the dispute case progresses through the workflow to determine whether to initiate a chargeback, write off the amount, or deny credit and reverse the chargeback, returning the credit to the cardholder.
-   Provisional credit: This decision provides temporary credit to the cardholder. If the merchant refuses the dispute, the case undergoes manual investigation.
-   No credit: This decision provides no credit. If the merchant refuses the dispute, the case undergoes manual investigation.

In this stage, agents can also work on transactions identified as friendly fraud. For more information, see [Detect friendly fraud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/dispute-management/resolve-friendly-fraud.md).

## Chargeback

This stage applies for each disputed transaction in a case. You can access this stage by opening a disputed transaction in the Processing stage of the playbook.

During the Chargeback stage, the dispute is forwarded to the card network. The card network then forwards the dispute to the acquirer.

In this stage, the following actions take place:

-   The fraudulent transaction is reported to the card network.
-   A chargeback is initiated. There is a wait period to see if there is a representment. At the Review Representment task, the agent determines if the proof is sufficient and accepts or rejects the representment.
-   If the agent accepts the representment and provisional credit has been issued, reverse provisional credit to refund the merchant if a chargeback has been initiated with the acquiring bank.
-   In card dispute playbooks integrated with Visa, agents can also progress a disputed transaction through pre-arbitration, arbitration, and appeal in the Chargeback stage. They can review responses to each of these, and create filings in response as required.

The block card or reissue card flows run in parallel with the rest of the dispute management flow running for the various transactions being disputed.

## Closure

After a case is processed according to the final determinations for all dispute transactions associated with the case, the case progresses to Closure.

If the evaluated policy rules deny the transaction, it will move directly to Closure.

Agents can enter the Resolution code and any Resolution notes before the case is moved to Closed Complete state.

**Parent Topic:**[Understanding Dispute Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/dispute-management/disputes-overview.md)

**Parent Topic:**[Dispute Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/dispute-management/dispute-management.md)

