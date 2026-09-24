---
title: Dispute Rules Content Pack for Visa release notes
description: The ServiceNow Dispute Rules Content Pack for Visa application supports the intake of dispute-related information under various dispute categories according to Visa guidelines. See the following sections for release notes by version.This release keeps Visa chargeback dispute evaluation accurate by updating eligibility rules for eight reason codes to match the April 2026 Visa Chargeback Guide. It adds 38 new transaction data fields to support the updated criteria. This release also introduces a new price-discrepancy ineligibility condition for reason code 13.3.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/dispute-rules-content-pack-for-visa-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Dispute Rules Content Pack for Visa, Visa disputes, chargeback eligibility, Visa Core Rules, Visa Product and Service Rules, dispute categories, transaction processing, Financial Services Card Operations, release notes, activation, installation, Visa, chargeback, dispute rules, reason codes, eligibility rules, transaction data, fraud, AVS, Address Verification Service, authorization, financial services]
audience: [administrator, administrator]
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Dispute Rules Content Pack for Visa release notes

The ServiceNow® Dispute Rules Content Pack for Visa application supports the intake of dispute-related information under various dispute categories according to Visa guidelines. See the following sections for release notes by version.

## About Dispute Rules Content Pack for Visa

-   Effectively manage and resolve Visa disputes.
-   Determine chargeback eligibility for the disputed transactions based on the Visa Core Rules and Visa Product and Service Rules.
-   Categorize disputes for accurate transaction processing.

See [Dispute Rules Content Pack for Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Dispute Rules Content Pack for Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    Requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/financial-services-operations-rn-landing.md)

## Version 7.1.1

This release keeps Visa chargeback dispute evaluation accurate by updating eligibility rules for eight reason codes to match the April 2026 Visa Chargeback Guide. It adds 38 new transaction data fields to support the updated criteria. This release also introduces a new price-discrepancy ineligibility condition for reason code 13.3.

### What's new

-   **[New transaction data fields for chargeback rule evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-rules-content-pack-for-visa-landing-page-1.md)**

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


