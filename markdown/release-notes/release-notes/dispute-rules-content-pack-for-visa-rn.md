---
title: Dispute Rules Content Pack for Visa release notes
description: The ServiceNow Dispute Rules Content Pack for Visa application provides questionnaires for dispute-related information intake under various dispute categories according to Visa guidelines. Dispute Rules Content Pack for Visa was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-04"
reading_time_minutes: 4
---

# Dispute Rules Content Pack for Visa release notes

The ServiceNow® Dispute Rules Content Pack for Visa application provides questionnaires for dispute-related information intake under various dispute categories according to Visa guidelines. Dispute Rules Content Pack for Visa was enhanced and updated in the Australia release.

## Dispute Rules Content Pack for Visa highlights for the Australia release

Applied Visa Resolve Online \(VROL\) release 26.1 revision changes to the Dispute Rules Content Pack for Visa questionnaireand updated chargeback rules based on the Visa Chargeback Guide v1.1.

See [Dispute Rules Content Pack for Visa](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US) for more information.

**Important:** Dispute Rules Content Pack for Visa is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Special Condition Indicator field](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    A new **Special Condition Indicator** field on the Financial Transaction record identifies transactions involving non-fiat currency, non-fungible tokens \(NFTs\), and related digital assets. The chargeback eligibility rules engine uses this field to apply the correct dispute conditions for RC 10.4, RC 13.1, and RC 13.3.

-   **[New dispute intake questions for digital asset transactions](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    Two new questions have been added to the Visa dispute intake questionnaire to support the updated eligibility rules for non-fiat currency and NFT transactions.

    -   For fraud disputes where the Special Condition Indicator is 2, 3, 4, or 7: ask whether the cardholder claims they were deceived into sending non-fiat currency or an NFT to a fraudulent recipient.
    -   For consumer disputes filed under RC 13.3 \(Not as Described\) involving a non-fiat currency or NFT purchase: ask whether the cardholder has evidence that the merchant guaranteed or promised the asset would increase in value.

## Changed in this release

-   **[Updated questions for the dispute questionnaire](https://www.servicenow.com/docs/access?context=exploring-the-dispute-rules-content-pack-for-visa&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    Added four new agent-facing questions to the dispute questionnaire under the authorization \(11\) and consumer disputes \(13\) categories. These questions map to the following reason codes:

    -   11.1 - Card recovery bulletin or exception file
    -   11.2 - Declined authorization
    -   11.3 - No authorization or late presentment
    -   13.6 - Credit not processed
    -   13.7 - Cancelled merchandise or services
-   **[Visa Resolve Online \(VROL\) version 26.1 updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    Updated the dispute questionnaire provided through the Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 26.1 revision changes.

-   **[Updated chargeback eligibility rules for Visa reason codes 10.1, 10.2, 10.3, 10.4, 13.1, 13.2, 13.3, and 13.4](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    The chargeback eligibility rules for eight Visa reason codes have been updated to reflect Visa Chargeback Guide v1.1. The rules engine evaluates disputes automatically against the updated criteria; no manual configuration is required. Disputes that do not meet the updated eligibility criteria are flagged as ineligible before submission.

-   **[Updated dispute intake questionnaire for fraud disputes involving non-fiat currency and NFTs](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    The fraud dispute intake questionnaire now includes a conditional question for disputes involving non-fiat currency or NFT transactions, such as cryptocurrency and digital token purchases. When the transaction is identified as a digital asset purchase, dispute agents and cardholders are asked to confirm whether the cardholder claims they were deceived into sending the asset to a fraudulent recipient. The question is shown only when relevant and is cleared automatically when it does not apply. This supports accurate eligibility evaluation without requiring agents to manually identify digital asset transaction types.

-   **[Updated dispute intake questionnaire for RC 13.3 \(Not as Described\) disputes involving non-fiat currency and NFTs](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    The consumer dispute intake questionnaire for RC 13.3 now includes an additional question for disputes involving non-fiat currency or NFT purchases. After confirming whether the asset received matched the description at the time of purchase, dispute agents and cardholders are asked whether there is evidence that the merchant guaranteed or promised the asset would increase in value. This question determines whether a specific dispute right applies, and appears only after the preceding NFT description question is answered.


## Activation information

Install Dispute Rules Content Pack for Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Playbooks for Customer Service Management](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

    ServiceNow® Playbooks for Customer Service Management provides a way to visualize business process workflows in a simple, task-oriented view for consistent responses to commonly encountered situations.

-   **[Financial Services Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    The ServiceNow® Financial Services Card Operations application digitizes and automates the card operations of your financial institution, enabling quick processing of credit card applications and card transaction disputes.

-   **[Financial Services Credit Operations](https://www.servicenow.com/docs/access?context=fso-credit-operations-landing-page&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

    The ServiceNow® Financial Services Credit Operations application enables the management of credit cases and tasks that are used in Financial Services Operations workflows.

-   **[Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    Automate integration tasks by using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations.

-   **[Integration Hub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

    Activate spokes to improve your Workflow Studio experience with integration-specific content. Use prebuilt flows and actions to automate your integrations or create your own integration automation.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

