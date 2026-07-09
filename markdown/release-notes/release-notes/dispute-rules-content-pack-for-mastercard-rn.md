---
title: Dispute Rules Content Pack for Mastercard release notes
description: The ServiceNow Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories according to Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 6
---

# Dispute Rules Content Pack for Mastercard release notes

The ServiceNow® Dispute Rules Content Pack for Mastercard application supports the intake of dispute-related information under various dispute categories according to Mastercard guidelines. Dispute Rules Content Pack for Mastercard was enhanced and updated in the Australia release.

## Dispute Rules Content Pack for Mastercard highlights for the Australia release

-   Keep Mastercard dispute assessments compliant with updated chargeback ineligibility rules across the Authorization, Processing Errors, and Cardholder Disputes categories.
-   Assess chargeback eligibility accurately using new data fields sourced from the Mastercard authorization and clearing APIs.

See [Dispute Rules Content Pack for Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md) for more information.

**Important:** Dispute Rules Content Pack for Mastercard is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Dispute Rules Content Pack for Mastercard to Australia

The Australia release adds new data fields to the Authorization and Financial Transaction tables to support the new eligibility rules. The `transactionAmountLocal` field already exists in the Financial Transaction table but is being extended to the Financial Transaction Authorization table in this release. No other pre-existing fields are affected. After upgrading, confirm that the new fields are available and populated on your instance.

## New in the Australia release

-   **[May Store Release: New data fields for Mastercard chargeback eligibility rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    New data fields sourced from the Mastercard authorization API and Mastercard clearing API have been added to support the expanded eligibility rules. Fields sourced from the Mastercard authorization API are available on the Financial Transaction Authorization table. Fields sourced from the Mastercard clearing API are available on the Financial Transaction table.

    New fields on the Financial Transaction Authorization table:

    -   `adviceReasonCode`
    -   `banknetDate`
    -   `merchantAdviceCode`
    -   `originalMessageTypeIdentifier`
    -   `pinServiceCode`
    -   `retrievalReferenceNumber`
    -   `stan`
    -   `transactionAmountLocal`

        **Note:** This field already exists in the Financial Transaction table and is being extended to the Financial Transaction Authorization table in this release.

    -   `transactionAmountUsd`
    -   `transmissionDateAndTime`
    New fields on the Financial Transaction table:

    -   `businessServiceIdCode`
    -   `cardDataInputCapability`
    -   `cardholderAuthenticationCapability`
    -   `servicecode`
-   **[July Store Release: New data field for Mastercard chargeback ineligibility rule assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    A new Mastercard data field `programRegistrationId` has been added to the Financial Transaction table to support chargeback ineligibility rule evaluation for RC 4853 Cardholder Disputes sub-categories. The field is sourced from the Mastercard clearing API.

    This field identifies the program registration associated with a clearing transaction. The field displays both the program code and its description. Supported values include codes for person-to-person transfers, business disbursements, government and non-profit disbursements, merchant-presented QR transactions, and other Mastercard Send program types.

-   **[July Store Release: New input variables for Mastercard chargeback ineligibility rule assessment decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    New input variables have been added to support updated chargeback ineligibility rule evaluation for RC 4808 Authorization sub-categories. The following computed values are used as decision inputs across the Required Authorization Not Obtained, Expired Chargeback Protection Period, Stand-in or X-Code Approval after Issuer Decline, CAT 3 Devices, and Transit First Ride Risk Framework Claims decision tables:

    -   `transit_clearing_amount_sum` — the sum of local transaction amounts for matching transit clearing transactions, used to evaluate UK domestic contactless transit split-clearing ineligibility conditions.
    -   `cpd_minus_declined_transit_auth_date_time` — the number of days between a declined transit authorization and the chargeback protection date \(CPD\), used to assess TFRR/FRIL eligibility windows.
    -   `financial_local_txn_amt_minus_auth_local_txn_amt` — the difference between the financial and authorization local transaction amounts, used for RANO authorization amount difference conditions.
-   **[July Store Release: New Mastercard dispute sub-categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    The following new Mastercard dispute sub-categories are available:

    -   Installment Billing Dispute-Participating Countries \(RC 4850\)
    -   Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(RC 4854\)

## Changed in this release

-   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    Determine the eligibility of a selected transaction for chargeback through chargeback eligibility rules transformed into technical formulas.

    For May Store release, new ineligibility conditions have been added across all five existing RC 4808 Authorization sub-categories:

    -   Required Authorization Not Obtained \(RANO\)
    -   Expired Chargeback Protection Period \(ECPP\)
    -   Stand-in or X-Code Approval after Issuer Decline \(SIXCAID\)
    -   CAT 3 Devices \(CAT3D\)
    -   Transit First Ride Risk Framework Claims \(TFRR\)
    For May Store release, expanded eligibility rules for the following fraud dispute reason codes:

    -   RC 4837 \(No Cardholder Authorization\)
    -   RC 4849 \(Questionable Merchant Activity\)
    -   RC 4870 \(Chip Liability Shift\)
    -   RC 4871 \(Chip Liability Shift – Lost/Stolen/Never Received Issue \(NRI\) Fraud\)
-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    Benefit from the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard with some modified questions and added hard stop alerts.

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Processing Errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

    Ineligibility rule conditions have been updated across the RC 4834 Processing Errors sub-categories to align with the latest Mastercard Chargeback Guide. Updated sub-categories include Transaction Amount Differs, Currency Errors, Cardholder Debited More than Once for the Same Goods or Services, ATM Funds Not Dispensed, Charges for Loss, Theft, or Damages, Merchant Refund Correcting Error Resulted in Cardholder Currency Exchange Loss, Improper Merchant Surcharge, Unreasonable Amount, and Cash was not properly provided from a Purchase with Cash Back transaction.

    For Currency Errors: A new ineligibility condition has been added. CE is not applicable for ATM transactions \(MCC 6011\) where either the card was issued outside Europe or the terminal is located outside Europe.

    For Transaction Amount Differs: The documentation requirements for this sub-category have been updated. For Maestro cards issued in Europe used at terminals outside Europe, no documentation is required. Brazil domestic disputes involving gratuity amounts now have explicit documentation requirements.

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Cardholder Disputes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md)**

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


## Removed in this release

For July store release, the sub-category RC 4834 — Late Presentment has been removed.

## Activation information

Install Dispute Rules Content Pack for Mastercard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.

## Related ServiceNow applications and features

-   **[Financial Services Card Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/card-ops-landing-page.md)**

    The ServiceNow® Financial Services Card Operations application digitizes and automates the card operations of your financial institution, enabling quick processing of credit card applications and card transaction disputes.

-   **[Financial Services Credit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-credit-operations-landing-page.md)**

    The ServiceNow® Financial Services Credit Operations application enables the management of credit cases and tasks that are used in ServiceNow® Financial Services Operations workflows.

-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md)**

    Enable the extension of tables from the Customer Service Management \(CSM\) application into the Financial Services Card Operations application.

-   **[Playbook capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-playbooks.md)**

    Visualize business process workflows in a simple, task-oriented view with the Playbooks for Customer Service Management \(CSM\) to verify consistent responses to commonly encountered situations.


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/financial-services-operations-rn-landing.md)

