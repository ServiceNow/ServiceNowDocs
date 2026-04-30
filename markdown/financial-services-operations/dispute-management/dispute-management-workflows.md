---
title: Dispute workflows
description: As a card dispute agent or agent connector, you can work on a credit or debit card dispute cases by investigating and resolving dispute requests for cardholders.
locale: en-US
release: xanadu
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [About Dispute Management, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Dispute workflows

As a card dispute agent or agent connector, you can work on a credit or debit card dispute cases by investigating and resolving dispute requests for cardholders.

When an agent disputes a transaction on behalf of a customer, it initiates a dispute service case and triggers the dispute card transactions flow. This flow includes various tasks specific to the case details.

For credit or debit card dispute management cases, tasks are generated for each transaction that has a dispute request. The playbook guides you through these tasks, ensuring you effectively manage and fulfill them based on investigations and decisions made by parties involved, such as the cardholder, card network, or merchant. With input or decisions from these parties, you, as a dispute agent, will complete activities and tasks within the Initiate, Review,Investigation, Chargeback, and Closure stages of a dispute case.

## Initiate

When a dispute agent initiates a case, the case begins in the Initiate stage.

During this phase, you can identify the disputed transaction, add more transactions \(if the dispute category is Fraud\), complete the dispute questionnaire, and upload any supporting documentation.

When a transaction is selected for dispute, you can obtain additional information about the transaction with an integration, such as [Ethoca Consumer Clarity](https://www.servicenow.com/docs/access?context=ethoca-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) and [Order Insight Digital Management](https://www.servicenow.com/docs/access?context=visa-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

The system evaluates decision rules and determines policy rules for each transaction in the case \(for example, which transaction qualifies for a provisional credit as opposed to a final credit\).

The system generates tasks based on the policy rules that are evaluated when a case is submitted. For instance, when a case has a dispute category of Fraud, the system creates a task to block and reissue the card.

For information about configuring business rules, see [Exploring decision tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Review

If a dispute case was submitted by a customer via a service portal, the case begins at the Review stage. If the case was initiated by an agent, this stage will be skipped.

The dispute agent reviews the dispute intake, including the disputed transactions, the dispute amount, and the reasons for dispute.

The agent provides answers to any additional questions not answered by the cardholder and to any questions they are expected to address. If the dispute category changes, the system will produce a questionnaire for the newly selected category, which is then filled out by the agent.

After review, the agent submits the case and continues with the subsequent lanes and activities in the case.

The system generates tasks based on the policy rules that are evaluated when a case is submitted. For instance, when a case has a dispute category of Fraud, the system creates a task to block and reissue the card.

## Investigation

During this stage of the case, the card network, card issuing bank, merchant bank or acquirer, and merchant engage in review processes to make final determinations for each transaction. In this stage, you can [alert the merchant to a card transaction dispute](../task/alert-merchant-regarding-dispute.md). If a merchant refuses a transaction dispute, [the case may also move to the manual investigation task](../task/manually-investigate-disputed-transaction.md).

The business rules engine initiates decisions for the transaction such as:

-   Deny: The dispute for the transaction is denied.
-   Immediate final credit: This decision provides final credit immediately to the cardholder. For example, if the disputed transaction amount is below $25 USD, a bank's business rule may choose to initiate immediate final credit. If immediate final credit is decided, the dispute case progresses through the workflow to determine whether to initiate a chargeback, write off the amount, or deny credit and reverse the chargeback, returning the credit to the cardholder.
-   Provisional credit: This decision provides temporary credit to the cardholder. If the merchant refuses the dispute, the case undergoes manual investigation.
-   No credit: This decision provides no credit. If the merchant refuses the dispute, the case undergoes manual investigation.

## Chargeback

During the Chargeback stage, the dispute is forwarded to the card network. The card network then forwards the dispute to the acquirer.

In this stage, the following actions take place:

-   The fraudulent transaction is reported to the card network.
-   A chargeback is initiated. There is a wait period to see if there is a representment. At the Review Representment task, the agent determines if the proof is sufficient and accepts or rejects the representment.
-   If the agent accepts the representment and provisional credit has been issued, reverse provisional credit to refund the merchant if a chargeback has been initiated with the acquiring bank.

The block card or reissue card flows run in parallel with the rest of the dispute management flow running for the various transactions being disputed.

## Closure

After a case is processed according to the final determinations for all dispute transactions associated with the case, the case progresses to Closure.

If the evaluated policy rules deny the transaction, it will move directly to Closure.

Agents can enter the Resolution code and any Resolution notes before the case is moved to Closed Complete state.

**Parent Topic:**[About Dispute Management](../../fso-deposit-operations/concept/disputes-overview.md)

