---
title: About dispute intake
description: The dispute intake process is designed to capture the relevant information required for capturing dispute details. This can be through the customer or consumer service portal, agent workspace, or via Disputes intake via Virtual Agent.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# About dispute intake

The dispute intake process is designed to capture the relevant information required for capturing dispute details. This can be through the customer or consumer service portal, agent workspace, or via Disputes intake via Virtual Agent.

## About dispute intake form

The dispute intake form is designed to gather all necessary information before submitting a claim to the card network or processing an ACH dispute. The field questionnaire includes a variety of questions that help identify the dispute reason code based on the case type and responses to specific questions such as "Did you authorize this transaction?".

The Event Inquiry application provides a comprehensive overview of the events that led to the dispute. To understand how the Event Inquiry application works and how to customize the dispute intake form, see [Configure intake questionnaire](../task/configuring-additional-questions-for-dispute-intake.md).

The intake process simplifies data collection, making it easier for dispute agents to complete the intake and assess chargeback eligibility. This streamlined approach ensures that all relevant information is captured efficiently, enhancing the overall dispute resolution process.

## About Event Inquiry application

The Event Inquiry application stores all questions and automates the intake process, which helps gather detailed information for each dispute. This streamlines processing and improves efficiency.

Key tables in Event Inquiry include:

-   **Intake Form \[sn\_evnt\_inq\_qtn\]**

    Serves as the base table for the dispute intake tables in FSO Card Operations.

-   **Intake Form Label \[sn\_evnt\_inq\_question\]**

    Provides the labels for a specific field on a specific table, and admins can do that mapping.


## Questionnaire data model

The Dispute Intake form has been extended into the Dispute Intake table. The table includes both cardholder and agent related questions, while the Dispute Cardholder Intake table addresses cardholder-related questions. These tables are available in Financial Services Card Operations.

![Shows the questionnaire data model tables.](../image/questionnaire-data-model.png "Questionnaire data model")

## Unified intake experience with a generic questionnaire design

The dispute intake process provides a unified experience enabling cardholders, account holders, contributors, and agents to raise disputes for both card and non-card \(ACH\) transactions seamlessly.

Using a generic questionnaire design streamlines the dispute resolution process across different card and non-card networks. Each network has unique questions for specific transactions. When a customer initiates a dispute and selects a transaction, the system triggers a set of generic questions in the case workflow. If the case involves only one transaction, a single dispute questionnaire activity will include all required questions.

For disputes involving multiple transactions in a single case, a common questionnaire provides a unified approach for gathering insights into the dispute. The system updates this set with transaction-specific questions, ensuring that only relevant questions for the appropriate Network ID of the transaction are asked. These responses are automatically applied to the disputed transactions. Users can review and update them under the Fill Additional Questionnaire activity when adding transaction-specific details.

A generic questionnaire design:

-   Improves the experience for both customers and agents by asking only the necessary questions relevant to the Network ID of the transaction.
-   Enables for seamless collection of standardized questions across different transaction networks, with easy updates as needed for each network.
-   Simplifies the data model across multiple transaction networks, optimizing the dispute processing regardless of the network involved.

-   **[Create a dispute case with Dispute Intake in Portal](creating-an-onboarding-case-with-dispute-playbook-for-portal.md)**  
Whether you're a contact or a consumer, you can create a dispute case with a step-by-step guidance for the case flow process in either the Customer Service Portal or Consumer Service Portal, respectively.
-   **[Create a case with Disputes intake via Virtual Agent](create-a-case-with-virtual-agent.md)**  
Disputes intake via Virtual Agent streamlines the card dispute submission process for cardholders by providing a chat interface.
-   **[Initiate a dispute](../task/create-case-with-intake-workspace.md#)**  
Create a dispute case and initiate the dispute for a transaction associated with an account. You can enter dispute information, fill out the dispute questionnaire, upload supporting documentation, and submit the case for investigation.
-   **[Create a card disputes case request from the service catalog](../task/create-an-onboarding-request-from-the-service-catalog.md)**  
Create a card disputes case request from the Customer or Consumer Service Portals by navigating to the service catalog.

**Parent Topic:**[Managing dispute service requests](managing-card-disputes.md)

