---
title: Dispute Rules Content Pack for Visa release notes
description: The ServiceNow Dispute Rules Content Pack for Visa application provides questionnaires for dispute-related information intake under various dispute categories according to Visa guidelines. Dispute Rules Content Pack for Visa was enhanced and updated in the Australia release.This release keeps Visa chargeback dispute evaluation accurate by updating eligibility rules for eight reason codes to match the April 2026 Visa Chargeback Guide. It adds 38 new transaction data fields to support the updated criteria. This release also introduces a new price-discrepancy ineligibility condition for reason code 13.3.The ServiceNow Dispute Rules Content Pack for Visa application provides questionnaires for dispute-related information intake under various dispute categories according to Visa guidelines. Dispute Rules Content Pack for Visa was enhanced and updated in the Australia release.The ServiceNow Dispute Rules Content Pack for Visa application provides questionnaires for dispute-related information intake under various dispute categories according to Visa guidelines. Dispute Rules Content Pack for Visa was enhanced and updated in the Australia release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/dispute-rules-content-pack-for-visa-rn.html
release: australia
topic_type: topic
last_updated: "2026-04-04"
reading_time_minutes: 6
keywords: [Visa, chargeback, dispute rules, reason codes, eligibility rules, transaction data, fraud, AVS, Address Verification Service, authorization, financial services]
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Dispute Rules Content Pack for Visa release notes

The ServiceNow® Dispute Rules Content Pack for Visa application provides questionnaires for dispute-related information intake under various dispute categories according to Visa guidelines. Dispute Rules Content Pack for Visa was enhanced and updated in the Australia release.

## About Dispute Rules Content Pack for Visa

Applied Visa Resolve Online \(VROL\) release 26.1 revision changes to the Dispute Rules Content Pack for Visa questionnaireand updated chargeback rules based on the Visa Chargeback Guide v1.1.

See [Dispute Rules Content Pack for Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md) for more information.

## Activation and other requirements

**Important:** Dispute Rules Content Pack for Visa is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Dispute Rules Content Pack for Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/financial-services-operations-rn-landing.md)

## Version 7.1.1

This release keeps Visa chargeback dispute evaluation accurate by updating eligibility rules for eight reason codes to match the April 2026 Visa Chargeback Guide. It adds 38 new transaction data fields to support the updated criteria. This release also introduces a new price-discrepancy ineligibility condition for reason code 13.3.

### What's new

-   **[New transaction data fields for chargeback rule evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

    Added 38 new fields to the Financial Transaction record to support the updated Visa chargeback eligibility rules for reason codes 10.4 and 11.3.

    Reason code 10.4 fields:

    -   Account funding source
    -   Type of cryptogram received
    -   Authentication solution indicator
    -   Issuer BIN country code
    -   Purchase order number from 3-D Secure
    -   Order ID from merchant
    -   Device fingerprint
    -   Customer account login ID from merchant
    -   Customer account login ID from 3-D Secure
    -   Customer account login ID from agentic
    -   Shipping address 1 from 3-D Secure
    -   Shipping address 2 from 3-D Secure
    -   Shipping address 3 from 3-D Secure
    -   Shipping city from 3-D Secure
    -   Shipping country code from 3-D Secure
    -   Shipping postal code from 3-D Secure
    -   Shipping state from 3-D Secure
    -   Shipping address line 1 from merchant
    -   Shipping address line 2 from merchant
    -   Shipping street name from merchant
    -   Shipping building number from merchant
    -   Shipping postal code from merchant
    -   Shipping city from merchant
    -   Shipping country code from merchant
    -   Shipping address 1 from agentic
    -   Shipping address 2 from agentic
    -   Shipping address 3 from agentic
    -   Shipping city from agentic
    -   Shipping country code from agentic
    -   Shipping postal code from agentic
    -   Shipping state from agentic
    Reason code 11.3 fields:

    -   Partial authorization eligible
    -   Source settlement amount \(USD\)
    -   Authorization amount \(USD\)
    -   Initiating party indicator
    -   Merchant initiated transaction class
    -   Local cashback amount
    -   PAN reference ID

### What's changed

-   **Updated reason code 10.4 fraud and address verification eligibility conditions**

    Refined the invalid-dispute conditions for reason code 10.4 \(Other Fraud – Card-Absent Environment\), including new region-specific Address Verification Service \(AVS\) conditions phased in for Canada, US, and UK domestic transactions through October 23, 2026, then extended to Europe and select Latin America and Caribbean countries, and to Australia, New Zealand, and Singapore starting April 24, 2027. Added a Kazakhstan-specific condition for transactions initiated by reading a QR code, and a new condition \(effective October 24, 2026\) that evaluates device fingerprint, login ID, and delivery address matches across prior undisputed transactions.

-   **Updated reason code 11.3 authorization and clearing timeframe rules**

    Revised the No Authorization/Late Presentment conditions for ATM deposit and cash disbursement adjustments, removing outdated timeframe conditions and adding country-specific processing windows for India, Nepal, Japan, and Malaysia domestic transactions. Added new permitted-variance rules between authorization and clearing amounts for specific merchant category codes, including restaurants, cruise lines, lodging, and vehicle rental merchants, and for card-absent cardholder-initiated transactions. Added deferred-authorization timeframe conditions, including a Denmark-specific rule.

-   **Added reason code 13.3 price-discrepancy ineligibility condition**

    Added a new condition marking reason code 13.3 \(Not as Described or Defective Merchandise/Services\) disputes ineligible when the dispute is based on a price discrepancy rather than a description or defect issue.

-   **Refined chargeback documentation messages**

    Updated the required-documentation messages shown to dispute agents for reason codes 12.6 \(Duplicate Processing/Paid by Other Means\), 13.1 \(Merchandise/Services Not Received\), 13.2 \(Cancelled Recurring Transaction\), 13.5 \(Misrepresentation\), and 13.6 \(Credit Not Processed\) to align with the April 2026 Visa Chargeback Guide wording.


## Australia General Availability

The ServiceNow® Dispute Rules Content Pack for Visa application provides questionnaires for dispute-related information intake under various dispute categories according to Visa guidelines. Dispute Rules Content Pack for Visa was enhanced and updated in the Australia release.

### What's changed

-   **[Updated chargeback eligibility rules for Visa reason codes 10.1, 10.2, 10.3, 10.4, 13.1, 13.2, 13.3, and 13.4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

    The chargeback eligibility rules for eight Visa reason codes have been updated to reflect Visa Chargeback Guide v1.1. The rules engine evaluates disputes automatically against the updated criteria; no manual configuration is required. Disputes that do not meet the updated eligibility criteria are flagged as ineligible before submission.

-   **[Updated dispute intake questionnaire for fraud disputes involving non-fiat currency and NFTs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

    The fraud dispute intake questionnaire now includes a conditional question for disputes involving non-fiat currency or NFT transactions, such as cryptocurrency and digital token purchases. When the transaction is identified as a digital asset purchase, dispute agents and cardholders are asked to confirm whether the cardholder claims they were deceived into sending the asset to a fraudulent recipient. If confirmed, this claim supports accurate eligibility evaluation. The question is shown only when relevant and is cleared automatically when it does not apply. This supports accurate eligibility evaluation without requiring agents to manually identify digital asset transaction types.

-   **[Updated dispute intake questionnaire for RC 13.3 \(Not as Described\) disputes involving non-fiat currency and NFTs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

    The consumer dispute intake questionnaire for RC 13.3 now includes an additional question for disputes involving non-fiat currency or NFT purchases. After confirming whether the asset received matched the description at the time of purchase, dispute agents and cardholders are asked whether there is evidence that the merchant guaranteed or promised the asset would increase in value. This question determines whether a specific dispute right applies, and appears only after the preceding NFT description question is answered.


## Australia

The ServiceNow® Dispute Rules Content Pack for Visa application provides questionnaires for dispute-related information intake under various dispute categories according to Visa guidelines. Dispute Rules Content Pack for Visa was enhanced and updated in the Australia release.

### What's new

-   **[Special Condition Indicator field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

    A new **Special Condition Indicator** field on the Financial Transaction record identifies transactions involving non-fiat currency, non-fungible tokens \(NFTs\), and related digital assets. The chargeback eligibility rules engine uses this field to apply the correct dispute conditions for RC 10.4, RC 13.1, and RC 13.3.

-   **[New dispute intake questions for digital asset transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

    Two new questions have been added to the Visa dispute intake questionnaire to support the updated eligibility rules for non-fiat currency and NFT transactions.

    -   For fraud disputes where the Special Condition Indicator is 2, 3, 4, or 7: ask whether the cardholder claims they were deceived into sending non-fiat currency or an NFT to a fraudulent recipient.
    -   For consumer disputes filed under RC 13.3 \(Not as Described\) involving a non-fiat currency or NFT purchase: ask whether the cardholder has evidence that the merchant guaranteed or promised the asset would increase in value.

### What's changed

-   **[Updated questions for the dispute questionnaire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/exploring-the-dispute-rules-content-pack-for-visa.md)**

    Added four new agent-facing questions to the dispute questionnaire under the authorization \(11\) and consumer disputes \(13\) categories. These questions map to the following reason codes:

    -   11.1 - Card recovery bulletin or exception file
    -   11.2 - Declined authorization
    -   11.3 - No authorization or late presentment
    -   13.6 - Credit not processed
    -   13.7 - Cancelled merchandise or services
-   **[Visa Resolve Online \(VROL\) version 26.1 updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

    Updated the dispute questionnaire provided through the Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 26.1 revision changes.


