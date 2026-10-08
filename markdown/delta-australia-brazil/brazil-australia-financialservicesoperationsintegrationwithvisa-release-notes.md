---
title: Combined Financial Services Operations Integration with Visa release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Financial Services Operations Integration with Visa from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-financialservicesoperationsintegrationwithvisa-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Financial Services Operations Integration with Visa release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Financial Services Operations Integration with Visa from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Financial Services Operations Integration with Visa release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Financial Services Operations Integration with Visa to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Financial Services Operations Integration with Visa.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Visa allocation batch queue support**

The Process Incoming Acceptance Batch Queue subflow captures and processes updates from the `INCOMING_BQ_ACCEPTANCES_RECEIVED` batch queue for Visa disputes in the Fraud and Authorization allocation workflow: cases where an acquirer accepts full liability on an issuer's chargeback, or on a pre-arbitration response filed or submitted by the issuer. The system polls this subflow separately from the existing Batch Queues Flows Adapter, so these acceptances are less likely to be missed during allocation processing.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Financial Services Operations Integration with Visa features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Updated questionnaire field labels and validation**

Renamed the question "Explain why credit presented does not apply" to "Provide the Transaction Identifier\(s\) or Acquirer Reference Number\(s\) and the Transaction Date that the credit\(s\) was applied to and why the credit\(s\) does not resolve the Dispute," and renamed "Certification that the merchant facilities were withdrawn" to "Certification that the facilities were withdrawn." The **Name** field is no longer required, and **Key Factors** now accepts up to 200 characters.

-   **Updated Spoke action wiring for new questionnaire fields**

Added the **Date facilities were withdrawn** and **Date cardholder checked out from hotel** fields to the **Submit Dispute Questionnaire** and **Look up Dispute Details Response Parser** spoke actions, and added **CE Transaction Details** as a read-back field on **Look up Dispute Details Response Parser**. See [Financial Services Card Operations 2026 September Monthly release notes](https://www.servicenow.com/docs/access?context=financial-services-card-operations-rn-2026-09&family=australia&ft:locale=en-US) for the corresponding questionnaire questions.

-   **Processing code field values updated for Visa compliance**

The `processing_code` field choice values in the Financial transaction table have been updated to align with current Visa data field specifications. Existing choice values have been updated with refined labels and descriptions; new choice values have been added to support additional transaction types.

The updated choice values include:

    -   `00` — Goods/Service Purchase - Debit
    -   `01` — Cash Disbursement \(for example, withdrawal or cash advance\) - Debit
    -   `02` — Adjustment - Debit
    -   `10` — Account Funding or Card Absent Account Funding
    -   `11` — Quasi-Cash Transaction - Debit or Internet Gambling Transaction
    -   `19` — Fee Collection - Debit
    -   `20` — Return of Goods - Credit, Credit Transaction, Credit Voucher
    -   `22` — Adjustment - Credit
    -   `26` — Original Credit
    -   `28` — Activation and Load / Load
    -   `29` — Funds Disbursement - Credit
    -   `30` — Available Funds Inquiry
    -   `39` — Eligibility Inquiry
    -   `50` — Bill Payment \(U.S. only\)
    -   `53` — Payment \(U.S. only\)
    -   `72` — Activation \(POS\)
Dispute agents and administrators see these updated labels and descriptions in transaction UI drop-down lists and data entry forms. Existing transactions require no action. Existing choice values not listed here remain unchanged.


 -   **[Updated subflows](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=australia&ft:locale=en-US)**

The following subflows have been updated to support integration with the Card data security application:

    -   Look up Associated Transactions
    -   Look up Dispute Pre Arbitration Details
    -   Look up Dispute Filing Details
    -   Look up Dispute Response Details
    -   Look up Dispute Pre Arbitration Response Details

</td></tr><tr><td>

Brazil

</td><td>

-   **Processing code field values updated for Visa compliance**

Updated `processing_code` field choice values in the Financial transaction table align with current Visa data field specifications. Existing choice values have been updated with refined labels and descriptions; new choice values have been added to support additional transaction types.

The updated choice values include:

    -   `00` — Goods/Service Purchase - Debit
    -   `01` — Cash Disbursement \(for example, withdrawal or cash advance\) - Debit
    -   `02` — Adjustment - Debit
    -   `10` — Account Funding / Card Absent Account Funding
    -   `11` — Quasi-Cash Transaction - Debit or Internet Gambling Transaction
    -   `19` — Fee Collection - Debit
    -   `20` — Return of Goods - Credit, Credit Transaction, Credit Voucher
    -   `22` — Adjustment - Credit
    -   `26` — Original Credit
    -   `28` — Activation and Load / Load
    -   `29` — Funds Disbursement - Credit
    -   `30` — Available Funds Inquiry
    -   `39` — Eligibility Inquiry
    -   `50` — Bill Payment \(U.S. only\)
    -   `53` — Payment \(U.S. only\)
    -   `72` — Activation \(POS\)
Dispute agents and administrators see these updated labels and descriptions in transaction UI drop-down lists and data entry forms. No action is required on existing transactions. Existing choice values not listed here remain unchanged.


 -   **Updated questionnaire field labels and validation**

Renamed the question "Explain why credit presented does not apply" to "Provide the Transaction Identifier\(s\) or Acquirer Reference Number\(s\) and the Transaction Date that the credit\(s\) was applied to and why the credit\(s\) does not resolve the Dispute," and renamed "Certification that the merchant facilities were withdrawn" to "Certification that the facilities were withdrawn." The Name field is no longer required, and Key Factors now accepts up to 200 characters.

-   **Updated Spoke action wiring for new questionnaire fields**

Added the Date facilities were withdrawn and Date cardholder checked out from hotel fields to the `Submit Dispute Questionnaire` and `Look up Dispute Details Response Parser` spoke actions, and added CE Transaction Details as a read-back field on `Look up Dispute Details Response Parser`. See [Financial Services Card Operations 2026 September Monthly release notes](https://www.servicenow.com/docs/access?context=financial-services-card-operations-rn-2026-09&family=brazil&ft:locale=en-US) for the corresponding questionnaire questions.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Financial Services Operations Integration with Visa features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Financial Services Operations Integration with Visa features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Financial Services Operations Integration with Visa.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Financial Services Operations Integration with Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Financial Services Operations Integration with Visa is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Financial Services Operations Integration with Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Financial Services Operations Integration with Visa we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Financial Services Operations Integration with Visa we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Financial Services Operations Integration with Visa, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Financial Services Operations Integration with Visa we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Financial Services Operations Integration with Visa we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

Use updated subflows to help prevent storage or transmission of Payment Card Industry \(PCI\) data for card disputes within your ServiceNow instance.

 See [Visa](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-visa-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Provides the framework for supporting dispute resolution use cases on ServiceNow which requires integration with VROL.
-   Use predefined subflows to address primary integrations such as creating a dispute case, reporting fraud, and submitting a dispute questionnaire.

 See [Visa](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-visa-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

