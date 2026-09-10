---
title: Dispute Rules Content Pack for Mastercard release notes
description: The ServiceNow Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories per Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Zurich release.The ServiceNow Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories per Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Zurich release.The ServiceNow Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories per Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Zurich release.The ServiceNow Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories per Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-10-31"
reading_time_minutes: 5
---

# Dispute Rules Content Pack for Mastercard release notes

The ServiceNow® Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories per Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Zurich release.

## About Dispute Rules Content Pack for Mastercard

-   Developed and refined chargeback eligibility rules to validate dispute cases against Mastercard core rules.
-   Updated the intake questionnaire for various dispute categories.

See [Dispute Rules Content Pack for Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md) for more information.

## Activation and other requirements

**Important:** Dispute Rules Content Pack for Mastercard is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Dispute Rules Content Pack for Mastercard by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.


## Accessibility and localization

-   **Accessibility information**
    -   **Dark theme**

        The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/financial-services-operations-rn-landing.md)

## July 2026

The ServiceNow® Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories per Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Zurich release.

### What's new

-   **[July Store Release: New data field for Mastercard chargeback ineligibility rule assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    A new Mastercard data field `programRegistrationId` has been added to the Financial Transaction table to support chargeback ineligibility rule evaluation for RC 4853 Cardholder Disputes sub-categories. The field is sourced from the Mastercard clearing API.

    This field identifies the program registration associated with a clearing transaction. The field displays both the program code and its description. Supported values include codes for person-to-person transfers, business disbursements, government and non-profit disbursements, merchant-presented QR transactions, and other Mastercard Send program types.

-   **[July Store Release: New input variables for Mastercard chargeback ineligibility rule assessment decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    New input variables have been added to support updated chargeback ineligibility rule evaluation for RC 4808 Authorization sub-categories. The following computed values are used as decision inputs across the Required Authorization Not Obtained, Expired Chargeback Protection Period, Stand-in or X-Code Approval after Issuer Decline, CAT 3 Devices, and Transit First Ride Risk Framework Claims decision tables:

    -   `transit_clearing_amount_sum` — the sum of local transaction amounts for matching transit clearing transactions, used to evaluate UK domestic contactless transit split-clearing ineligibility conditions.
    -   `cpd_minus_declined_transit_auth_date_time` — the number of days between a declined transit authorization and the chargeback protection date \(CPD\), used to assess TFRR/FRIL eligibility windows.
    -   `financial_local_txn_amt_minus_auth_local_txn_amt` — the difference between the financial and authorization local transaction amounts, used for RANO authorization amount difference conditions.
-   **[July Store Release: New Mastercard dispute sub-categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    The following new Mastercard dispute sub-categories are available:

    -   Installment Billing Dispute-Participating Countries \(RC 4850\)
    -   Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(RC 4854\)

### What's changed

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Processing Errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    Ineligibility rule conditions have been updated across the RC 4834 Processing Errors sub-categories to align with the latest Mastercard Chargeback Guide. Updated sub-categories include Transaction Amount Differs, Currency Errors, Cardholder Debited More than Once for the Same Goods or Services, ATM Funds Not Dispensed, Charges for Loss, Theft, or Damages, Merchant Refund Correcting Error Resulted in Cardholder Currency Exchange Loss, Improper Merchant Surcharge, Unreasonable Amount, and Cash was not properly provided from a Purchase with Cash Back transaction.

    For Currency Errors: A new ineligibility condition has been added. CE is not applicable for ATM transactions \(MCC 6011\) where either the card was issued outside Europe or the terminal is located outside Europe.

    For Transaction Amount Differs: The documentation requirements for this sub-category have been updated. For Maestro cards issued in Europe used at terminals outside Europe, no documentation is required. Brazil domestic disputes involving gratuity amounts now have explicit documentation requirements.

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Cardholder Disputes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    Ineligibility rule conditions have been added or updated across the following RC 4853 Cardholder Disputes sub-categories to align with the latest Mastercard Chargeback Guide:

    -   Addendum Dispute
    -   Cardholder Dispute of a Recurring Transaction
    -   Counterfeit Goods
    -   Digital Goods Purchase of USD/EUR 25 or Less
    -   Goods or Services Not Provided
    -   Goods or Services Were Either Not as Described or Defective
    -   No-Show Hotel Charge
    -   Refund Not Processed
    -   Refund Posted as a Purchase
    -   Timeshares
    -   Transaction Did Not Complete
    -   Travel/Entertainment Services Not Provided/Not as Described and Merchant Voucher Issued
    New ineligibility rule conditions have also been added for the Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(RC 4854\) sub-category.


### What's deprecated or removed

For July store release, the sub-category RC 4834 — Late Presentment has been removed.

## May 2026

The ServiceNow® Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories per Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Zurich release.

### What's new

-   **[New data fields for Mastercard chargeback eligibility rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    New data fields sourced from the Mastercard authorization API and Mastercard clearing API have been added to support the expanded eligibility rules. Fields sourced from the Mastercard authorization API are available on the Financial Transaction Authorization table. Fields sourced from the Mastercard clearing API are available on the Financial Transaction table.


## Zurich

The ServiceNow® Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories per Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Zurich release.

### What's new

-   **[Decision tables for Mastercard dispute processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-decision-tables.md)**

    Streamline dispute processing by validating Mastercard transaction details and questionnaire answers against the eligibility rules in this application's decision tables.


### What's changed

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


-   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    Transformed chargeback eligibility rules into technical formulas to determine the eligibility or ineligibility of a selected transaction for chargeback.

    New ineligibility conditions have been added across all five existing RC 4808 Authorization sub-categories:

    -   Required Authorization Not Obtained \(RANO\)
    -   Expired Chargeback Protection Period \(ECPP\)
    -   Stand-in or X-Code Approval after Issuer Decline \(SIXCAID\)
    -   CAT 3 Devices \(CAT3D\)
    -   Transit First Ride Risk Framework Claims \(TFRR\)
    Expanded eligibility rules for the following fraud dispute reason codes:

    -   RC 4837 \(No Cardholder Authorization\)
    -   RC 4849 \(Questionable Merchant Activity\)
    -   RC 4870 \(Chip Liability Shift\)
    -   RC 4871 \(Chip Liability Shift – Lost/Stolen/NRI Fraud\)
-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    Updated the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard by adding new questions and updating existing questions.


