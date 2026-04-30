---
title: Overview of the Dispute Management workflow
description: ServiceNow Dispute Management enables efficient card and non-card transaction dispute resolution, enhanced compliance, and streamlined customer experiences.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Overview of the Dispute Management workflow

ServiceNow® Dispute Management enables efficient card and non-card transaction dispute resolution, enhanced compliance, and streamlined customer experiences.

When a dispute service case is initiated, the dispute transaction flow triggers. This flow includes various tasks specific to the case details.

For card or non-card dispute management cases, tasks are generated for each transaction that has a dispute request. The Dispute Workspace guides you through each task in the dispute. With input or decisions from each party, you as a dispute agent work through the Initiate, Review,Processing, and Closure stages of a dispute case.

## Initiate

When a dispute is initiated, the case begins in the Initiate stage.

Dispute cases can be initiated from the Dispute Workspace by contributors on behalf of the customer, or by customers through the portal or through virtual agent disputes with Now Assist for Financial Services Operations \(FSO\) with the Virtual Agent  skill. Dispute agents can also create cases when needed.

During this phase, the system identifies the initial transaction. You’re then guided through the "Select dispute reason" activity, which involves a tiered questioning process \(Level 1, Level 2, and optionally Level 3\) to accurately determine the dispute category and its corresponding reason code.

You can then add more transactions \(if the dispute category is Fraud\),  and select associated transactions \(if Visa network\). You also complete the dispute questionnaire and upload any supporting documentation.  Dispute cases created using  disputes intake via Virtual Agent  are populated with information from the customer's responses in the Virtual Agent chat.

When a transaction is selected for a card dispute, you can obtain additional information about the transaction with an integration, such as [Order Insight Digital Management](https://www.servicenow.com/docs/access?context=visa-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

**Note:** Additional integrations such as [Ethoca Consumer Clarity](https://www.servicenow.com/docs/access?context=ethoca-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) are available to retrieve additional information on a transaction.

The system evaluates decision rules and determines policy rules for each transaction in the case. For example, determining which transaction qualifies for a provisional credit, as opposed to a final credit. However, if the dispute is initiated by a contributor or customer, the evaluation of decision rules occurs only after the Review task has been submitted. For more information on these rules, see [Dispute decision tables](dispute-decision-tables.md).

The system generates tasks based on the policy rules that are evaluated when a case is submitted. For instance, when a case has a dispute category of Fraud, the system creates a task to block and reissue the card.

Chargeback eligibility rules depend on the dispute category \(for card disputes\). In cases of fraud, these rules are evaluated during the Investigate stage, specifically after the Fraud Report task is submitted. For non-fraud categories, the evaluation happens at the Submit action, whether from Initiate or Review. For ACH disputes, the eligibility for chargeback is evaluated during investigation and can be assisted by Now Assist agents.

For information about Now Assist for FSO, see [Now Assist for Financial Services Operations \(FSO\)](../../fso-common/concept/now-assist-for-financial-services-operations.md).

For information about configuring business rules, see [Exploring Decision Tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Review

If a dispute case was submitted by a customer via a service portal or a user with a contributor persona via Dispute Workspace, the case progresses to the Review stage. If the case was initiated by an agent, this stage is skipped.

The dispute agent reviews the dispute intake, including the disputed transactions, the dispute amount, and the reasons for the dispute.

The agent provides answers to any additional questions not answered by the customer as required. If the dispute category changes, the system produces a questionnaire for the newly selected category, which is then filled out by the agent. For ACH disputes, the agent then must review the previously attached and signed Written Statement of Unauthorized Debit \(WSUD\) document, which they can either verify or reject.

After review, the agent submits the case and continues with the subsequent lanes and activities in the case.

The system generates tasks based on the policy rules that are evaluated when a case is submitted. For instance, when a case has a dispute category of Fraud, the system creates a task to block and reissue the card.

**Note:** If the Dispute Rules Content Pack for Visa, Mastercard, or Nacha are installed, the system automatically provides both the dispute category and reason code. Without these content packs, only the dispute category is determined. For networks other than Visa, Mastercard, or ACH, customers must manually map their network-specific reason codes to the system's decision tables.

## Processing

After a card dispute case is submitted, an agent can monitor and progress the disputed transactions in the Processing stage. This stage presents an overview of the overall case and tracks the status of each transaction and its related tasks.

Each disputed transaction in the case is displayed in this view as a separate card. Each card contains the following information:

-   Card disputes transaction number
-   Stage of processing \(Investigate, Chargeback, or Complete\)
-   Card present or card not present indicator
-   Dispute amount
-   Transaction date
-   Merchant type
-   Transaction state
-   Current activity
-   Activity service level agreement \(SLA\)

## Investigate

This stage applies for each disputed transaction in a case. You can access this stage by opening a disputed transaction in the Processing stage of the playbook.

Each transaction is opened in the **Dispute Workspace**, represented as a process-based layout. This layout visually represents the distinct stages of the investigation workflow for that specific transaction: Investigate, Chargeback, and Closure.

During this stage, the card network, card issuing bank, merchant bank or acquirer, and merchant engage in review processes to make final determinations for each transaction. In this stage, the merchant gets alerted of a card dispute transaction. If a merchant declines a disputed transaction, then a task to [Investigate transactions](../task/manually-investigate-disputed-transaction.md) is created.

**Note:** Issuer banks don’t contact merchants directly about disputed transactions. However, merchants enrolled in Ethoca Alerts or Verifi CDRN receive notifications of potential disputes, enabling them to work with cardholders to resolve issues and help prevent chargebacks.

In this stage, agents can also work on transactions identified as friendly fraud. For more information, see [Detect friendly fraud](../task/resolve-friendly-fraud.md).

## Chargeback

This stage applies for each disputed transaction in a case. You can access this stage by opening a disputed transaction in the Processing stage of the playbook.

During the chargeback stage, the agent submits the card dispute and the chargeback workflow begins between the involved parties. For non-card disputes, the agent files the ACH return.

For card fraud disputes, the block card or reissue card flows run in parallel with the rest of the dispute management flow for the disputed transactions.

Chargeback workflows differ between card and non-card disputes, as well as between card networks. See [Managing Disputes](managing-disputes.md) for more information.

## Closure

After a case is processed according to the final determinations for all dispute transactions associated with the case, the case progresses to Closure.

If there are more than one disputed transactions associated with a case, the case remains open until the workflows for each transaction are completed and closed.

If the evaluated policy rules deny the transaction, it moves directly to Closure.

Agents can enter the Resolution code and any Resolution notes before the case is moved to Closed Complete state.

**Parent Topic:**[Managing dispute service requests](managing-card-disputes.md)

**Related topics**  


[Card Disputes data model](../reference/dispute-data-model.md)

[Set up Dispute Management](../../fso-deposit-operations/concept/setting-up-disputes-management.md)

[About dispute intake](dispute-intake-overview.md)

[Review a dispute from portal or workspace intake](../task/review-a-dispute-from-cardholder-intake.md)

[Managing Disputes](managing-disputes.md)

