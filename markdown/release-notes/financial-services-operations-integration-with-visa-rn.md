---
title: Financial Services Operations Integration with Visa release notes
description: The ServiceNow Financial Services Operations Integration with Visa application enables easier integration with workflow applications, such as the card operations dispute management playbook with Visa Resolve Online \(VROL\) subflows. Financial Services Operations Integration with Visa was enhanced and updated in the Australia release.Align the Visa dispute questionnaire subflows with Visa Interface Elements Specification \(IES\) release 26.2, revisions 1 and 2. Dispute agents see accurate field labels, validation, and Spoke action wiring.The ServiceNow Financial Services Operations Integration with Visa application enables easier integration with workflow applications, such as the card operations dispute management playbook with Visa Resolve Online \(VROL\) subflows. Financial Services Operations Integration with Visa was enhanced and updated in the Australia release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/financial-services-operations-integration-with-visa-rn.html
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Visa, dispute questionnaire, IES, Interface Elements Specification, subflows, field labels, validation, Spoke actions, financial services]
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Financial Services Operations Integration with Visa release notes

The ServiceNow® Financial Services Operations Integration with Visa application enables easier integration with workflow applications, such as the card operations dispute management playbook with Visa Resolve Online \(VROL\) subflows. Financial Services Operations Integration with Visa was enhanced and updated in the Australia release.

## About Financial Services Operations Integration with Visa

Use updated subflows to help prevent storage or transmission of Payment Card Industry \(PCI\) data for card disputes within your ServiceNow instance.

See [Financial Services Operations Integration with Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-operations-integration-with-visa-landing-page.md) for more information.

## Activation and other requirements

**Important:** Financial Services Operations Integration with Visa is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Financial Services Operations Integration with Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/financial-services-operations-rn-landing.md)

## Version 5.1.1

Align the Visa dispute questionnaire subflows with Visa Interface Elements Specification \(IES\) release 26.2, revisions 1 and 2. Dispute agents see accurate field labels, validation, and Spoke action wiring.

### What's changed

-   **Updated questionnaire field labels and validation**

    Renamed the question "Explain why credit presented does not apply" to "Provide the Transaction Identifier\(s\) or Acquirer Reference Number\(s\) and the Transaction Date that the credit\(s\) was applied to and why the credit\(s\) does not resolve the Dispute," and renamed "Certification that the merchant facilities were withdrawn" to "Certification that the facilities were withdrawn." The **Name** field is no longer required, and **Key Factors** now accepts up to 200 characters.

-   **Updated Spoke action wiring for new questionnaire fields**

    Added the **Date facilities were withdrawn** and **Date cardholder checked out from hotel** fields to the **Submit Dispute Questionnaire** and **Look up Dispute Details Response Parser** spoke actions, and added **CE Transaction Details** as a read-back field on **Look up Dispute Details Response Parser**. See [Financial Services Card Operations 2026 September Monthly release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/financial-services-card-operations-rn.md) for the corresponding questionnaire questions.

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


## Australia

The ServiceNow® Financial Services Operations Integration with Visa application enables easier integration with workflow applications, such as the card operations dispute management playbook with Visa Resolve Online \(VROL\) subflows. Financial Services Operations Integration with Visa was enhanced and updated in the Australia release.

### What's changed

-   **[Updated subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/components-installed-with-the-financial-services-operations-integration-with-visa.md)**

    The following subflows have been updated to support integration with the Card data security application:

    -   Look up Associated Transactions
    -   Look up Dispute Pre Arbitration Details
    -   Look up Dispute Filing Details
    -   Look up Dispute Response Details
    -   Look up Dispute Pre Arbitration Response Details

