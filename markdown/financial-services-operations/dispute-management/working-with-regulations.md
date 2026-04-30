---
title: Working with Regulations
description: This page provides dispute agents with the information they need to handle dispute cases effectively and allows dispute managers to monitor case progress and take necessary actions to ensure compliance. The integration with the Dispute Content Pack for US Regulations application helps issuers track dispute cases governed by US regulations \(Reg E and Reg Z\).
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Working with Regulations

This page provides dispute agents with the information they need to handle dispute cases effectively and allows dispute managers to monitor case progress and take necessary actions to ensure compliance. The integration with the Dispute Content Pack for US Regulations application helps issuers track dispute cases governed by US regulations \(Reg E and Reg Z\).

## Creating card dispute case

Agents can manage dispute cases for their customers by using the dispute service case and its tasks. To learn on how to create a card dispute case, see[Creating a card dispute case](../task/create-dispute-service-case.md).

This process includes various stages. For more details on these stages, see [Managing dispute workflows](dispute-management-workflows.md).

## Dispute categories

Dispute categories include Fraud, Authorization, Processing Error, and Consumer Disputes. Each card network has its own set of rules and reason codes, but they generally fit into the following dispute categories:

-   **Fraud**

    This applies when the cardholder did not authorize or participate in the transaction.

-   **Authorization**

    This applies when a transaction required authorization but the merchant completed it without receiving it.

-   **Processing Error**

    This applies when a transaction is processed incorrectly due to a technical or operational mistake by the merchant, or when it’s processed correctly but not according to card network rules.

-   **Consumer**

    This applies when the cardholder disputes an issue with a merchant regarding the quality or receipt of goods or services.


## Dispute questionnaire

When a dispute agent or cardholder opens a dispute, they are presented with a corresponding set of questions. Designing clear, simple questions streamlines information gathering, helping customers or front-office agents understand and respond easily. For more details on configuring the questionnaire, see [Processing dispute intake](dispute-questionnaire.md).

## Dispute decision tables

The following table lists the decision tables used in Dispute Rules Content Pack for Mastercard.

|Decision table|Description|
|--------------|-----------|
|Reg E resolution days |Determines the Reg E resolution days for a Case based on transaction type and country. The default duration is set to 45 days.|

For more information on the Decision tables that provide the logic for processing card disputes, see [Configuring dispute decision tables](dispute-decision-tables.md)

## About the Dispute Content Pack for US Regulations

The Dispute Content Pack for US Regulations designed to help financial institutions comply with US regulatory requirements for dispute management. This content pack includes predefined rules and workflows that align with US regulations, ensuring that all necessary steps are taken to handle disputes in accordance with the law.

-   **[Dispute Content Pack for US Regulations](../../dispute-content-pack-US-regulation/concept/dispute-content-pack-for-us-regulation-landing-page.md)**  
The ServiceNow® Dispute Content Pack for US Regulations enables issuers in the United States \(US\) to track dispute cases and conform with regulatory guidelines.

**Parent Topic:**[Dispute Management](../../fso-deposit-operations/concept/dispute-management.md)

