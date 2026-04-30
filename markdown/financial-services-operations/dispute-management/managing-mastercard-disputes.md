---
title: Managing Mastercard disputes
description: The Dispute Rules Content Pack for Mastercard leverages guided data collection and maps the data entered to a dispute reason code to ensure the proper categorization and processing of disputes.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Managing Mastercard disputes

The Dispute Rules Content Pack for Mastercard leverages guided data collection and maps the data entered to a dispute reason code to ensure the proper categorization and processing of disputes.

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


## Dispute reason

Reason codes indicate the reason for a dispute.

## Dispute questionnaire

When a dispute agent or cardholder opens a dispute, they are presented with a corresponding set of questions. Designing clear, simple questions streamlines information gathering, helping customers or front-office agents understand and respond easily. For more details on configuring the questionnaire, see [Processing dispute intake](dispute-questionnaire.md).

## Dispute decision tables

The following table lists the decision tables used in Dispute Rules Content Pack for Mastercard.

|Decision table|Description|
|--------------|-----------|
|Mastercard Chargeback Eligibility Rules Subflow Mapping|Determines which chargeback eligibility subflow to call.|
|Determine Mastercard chargeback dispute reason code message|Determines the chargeback reason code for Mastercard disputes.|

For more information on the Decision tables that provide the logic for processing card disputes, see [Configuring dispute decision tables](dispute-decision-tables.md)

## Chargeback reason code

Data captured in Dispute Management is used to determine a reason code. These codes help the issuing bank decide if the dispute is eligible for a chargeback.

Reason codes are sent to Mastercard, which uses this information to process disputes through Mastercom.

Using ServiceNow to access all dispute details allows for more efficient management of disputes with Visa, saving time and money by reducing incorrectly processed cases.

## About the Dispute Rules Content Pack for Mastercard

The Dispute Rules Content Pack for Mastercard provides your agents with questionnaires that they can use to intake dispute-related information for various dispute categories as per the Mastercard guidelines.

-   **[Dispute Rules Content Pack for Mastercard](../../dispute-content-pack-for-mastercard/concept/dispute-rules-content-pack-for-mastercard-landing-page.md)**  
The ServiceNow® Dispute Rules Content Pack for Mastercard application provides your agents with questionnaires that they can use to intake dispute-related information for various dispute categories as per the Mastercard guidelines.

**Parent Topic:**[Dispute Management](../../fso-deposit-operations/concept/dispute-management.md)

