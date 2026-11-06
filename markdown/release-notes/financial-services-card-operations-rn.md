---
title: Financial Services Card Operations release notes
description: The ServiceNow Financial Services Card Operations application streamlines, digitizes, and automates card operations from the front to back office in your financial institution, and enables dispute agents to expedite dispute resolutions. See the following sections for release notes by version.Financial Services Card Operations version 15.4.1 adds Mastercard fraud type options and a Colombia-specific claim question to the card dispute intake questionnaire.Use Dispute Summarization from the Now Assist context menu \(NACM\) component on the dispute record page. The AI Summary Card component is deprecated. Answer the merchant voucher question in the dispute questionnaire for Refund Not Processed disputes.Add new dispute intake questions for Visa hotel and facilities-withdrawal disputes, and provide read-back visibility into compelling-evidence transaction details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/financial-services-card-operations-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [card operations, financial services, credit card management, dispute resolution, card blocking, credit limit, debit card, ACH dispute, dispute cases, card opening, card closing, financial institution, dispute agents, Mastercard, dispute intake questionnaire, fraud type, dispute summarization, NACM, AI Summary Card, dispute record page, Now Assist, card operations, financial services, Visa, dispute intake, consumer disputes, cardholder, compelling evidence, hotel disputes, price discrepancy, card operations, financial services]
audience: [administrator, user]
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Financial Services Card Operations release notes

The ServiceNow® Financial Services Card Operations application streamlines, digitizes, and automates card operations from the front to back office in your financial institution, and enables dispute agents to expedite dispute resolutions. See the following sections for release notes by version.

## About Financial Services Card Operations

-   Manage credit card openings and closings on one platform.
-   Simplify credit card blocking and credit ​limit processes.
-   Enable agents to create and manage dispute cases for both personal and business, debit and credit card accounts, and ACH dispute cases.
-   Enhanced user experience through guided workflows and real-time visibility.

See [Financial Services Card Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/card-ops-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/financial-services-operations-rn-landing.md)

## Version 15.4.1

Financial Services Card Operations version 15.4.1 adds Mastercard fraud type options and a Colombia-specific claim question to the card dispute intake questionnaire.

### What's new

-   **Additional Mastercard fraud type options**

    Classify Mastercard fraud disputes more precisely by selecting from three additional fraud type options during card dispute intake:

    -   53 - Testing-issuer
    -   54 - Undetermined
    -   57 - First-party misuse
-   **Colombia payment reversion claim question**

    Capture the information that Colombian regulations require for Mastercard fraud disputes. When a Mastercard dispute uses reason code 4837, 4870, or 4871, the merchant is located in Colombia, and the cardholder billing currency is the Colombian Peso, the dispute intake form asks whether the cardholder has filed a reversion of payment claim under Colombian law. An answer is required.


## Version 15.3.3

Use Dispute Summarization from the Now Assist context menu \(NACM\) component on the dispute record page. The AI Summary Card component is deprecated. Answer the merchant voucher question in the dispute questionnaire for Refund Not Processed disputes.

### What's changed

-   **Dispute Summarization component update**

    The Now Assist context menu \(NACM\) component replaces the AI Summary Card component that generated Dispute Summarization on the dispute record page. Dispute agents can generate an AI-generated summary of a dispute from the dispute record page.

    Dispute agents can share a generated summary to the claim's work notes from the summary component. Selecting **Share** opens an editable work notes dialog, where agents can edit the summary text before selecting **Save to work notes**.

    Activate the Dispute Summarization skill configuration for the summary component to appear. If the skill configuration isn't active, the component doesn't display on the dispute record page.

-   **UI policy update for the merchant voucher question on Refund Not Processed disputes**

    The Mastercard-specific merchant voucher question in the dispute questionnaire displays for Refund Not Processed disputes when the transaction has one of the following merchant category codes \(MCCs\): 3000 through 3999, 4411, 4511, 4722, 6513, 7011, 7512, 7519, or 7922. The UI policy **Field: TransactionMerchantVoucherFutureUseInd - Show/Hide/Mandatory \(Consumer\)** controls this display. Before this release, the UI policy displayed the question for Goods or Services Not Provided disputes and for Travel and Entertainment disputes where the merchant issued a voucher. The question and the MCC list are unchanged. Dispute agents answer whether the merchant provided a voucher for future use and disclosed it in its terms and conditions. When Dispute Rules Content Pack for Mastercard is installed, the answer determines whether a chargeback for reason code \(RC\) 4853 is eligible.


## Version 15.2.1

Add new dispute intake questions for Visa hotel and facilities-withdrawal disputes, and provide read-back visibility into compelling-evidence transaction details.

### What's new

-   **Date facilities were withdrawn**

    Dispute agents and cardholders can now record the date facilities were withdrawn by answering the question "Date of the facilities were withdrawn." This question displays only after answering Yes to "Certification that the facilities were withdrawn," and supports chargeback eligibility evaluation for reason code 13.2 \(Cancelled Recurring Transaction\).

-   **Date cardholder checked out from hotel**

    Dispute agents and cardholders can now record the date a cardholder checked out from a hotel by answering the question "Date cardholder checked out from hotel." This question displays only for disputes filed as Not as Described \(reason code 13.3\) or for a services dispute, where the merchant is categorized under a hotel or lodging merchant category code \(MCC 7011, or the 3501-3856 hotel-chain range\).

-   **CE Transaction Details**

    View compelling-evidence transaction details as a read-back field when reviewing Visa dispute details.


### What's changed

-   **Price-discrepancy question for Visa consumer disputes**

    An existing question, originally used under the Processing Errors dispute category, has been repurposed for consumer disputes filed under reason code 13.3 \(Not as Described or Defective Merchandise/Services\). Dispute agents are asked "Is the dispute due to the difference between the quoted price and the actual charges made by the merchant?" and cardholders are asked "Is the dispute related to a discrepancy between the quoted price and the actual charges made by the merchant?" A Yes answer marks the dispute ineligible for reason code 13.3, since a price discrepancy is not a valid basis for that reason code under the Visa Chargeback Guide.


### What's deprecated or removed

-   **Now LLM Service deprecation notice**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


