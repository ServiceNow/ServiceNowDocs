---
title: Processing dispute intake
description: The dispute intake process is designed to capture the relevant information required for capturing card dispute details.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Understanding Dispute Management, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Processing dispute intake

The dispute intake process is designed to capture the relevant information required for capturing card dispute details.

## About dispute intake

The dispute intake form is designed to gather all necessary information before submitting a claim to the card network. This form includes a variety of questions that help identify the dispute reason code based on the case type and responses to specific questions such as "What is incorrect about this transaction?" or "Did you authorize the transaction?".

The Event Inquiry application provides a comprehensive overview of the events that led to the dispute. To understand how the Event Inquiry application works and how to customize the dispute intake form, see [Configuring additional questions for dispute Intake](../task/configuring-additional-questions-for-dispute-intake.md).

The intake process simplifies data collection, making it easier for dispute agents to complete the intake, map reason codes, and assess chargeback eligibility. This streamlined approach ensures that all relevant information is captured efficiently, enhancing the overall dispute resolution process.

## About Event Inquiry application

The Event Inquiry application stores all questions and automates the intake process, which helps gather detailed information for each dispute. This streamlines processing and improves efficiency.

Key tables in Event Inquiry include:

-   **Intake Form \[sn\_evnt\_inq\_qtn\]**

    Serves as the base table for the dispute intake tables in FSO Card Operations.

-   **Intake Form Label \[sn\_evnt\_inq\_question\]**

    Provides the labels for a specific field on a specific table, and admins can do that mapping.


## Questionnaire data model

The Dispute Intake form has been extended into the Dispute Intake table. The table includes both cardholder and agent related questions, while the Dispute Cardholder Intake table addresses cardholder-related questions. Previously, these tables were part of the Dispute Rules Content Pack for Visa, but that dependency has now been removed. They are now available under Financial Services Card Operations, so any customer who installs this application automatically has access tp the questionnaire.

![Shows the questionnaire data model tables.](../image/questionnaire-data-model.png "Questionnaire data model")

## Advantages of a generic questionnaire design

Using a generic questionnaire design streamlines the dispute resolution process across different card networks. Each card network has unique questions for specific transactions. When a customer initiates a dispute and selects their transactions, the system triggers a set of generic questions in the case playbook. For disputes involving multiple transactions in a single case, a generic questionnaire provides a unified approach for gathering insights into the dispute. During multiple transaction disputes, the system updates this set with transaction-specific questions, ensuring that only relevant questions for the appropriate Network ID of the transaction are asked. Originally, only Visa had a questionnaire process, but we have repurposed this for other card networks.

A generic questionnaire design:

-   Improves the experience for both customers and agents by asking only the necessary questions relevant to the Network ID of the transaction.
-   Allows for seamless collection of standardized questions across different transaction networks, with easy updates as needed for each network.
-   Simplifies the data model across multiple transaction networks, optimizing the dispute processing regardless of the network involved.

-   **[Configuring additional questions for dispute Intake](../task/configuring-additional-questions-for-dispute-intake.md)**  
Configure the questionnaire that appears for dispute agents or cardholders when they intiate a dispute.

**Parent Topic:**[Understanding Dispute Management](../../fso-deposit-operations/concept/disputes-overview.md)

