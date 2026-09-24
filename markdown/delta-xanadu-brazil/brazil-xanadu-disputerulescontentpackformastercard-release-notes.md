---
title: Combined Dispute Rules Content Pack for Mastercard release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Dispute Rules Content Pack for Mastercard from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-disputerulescontentpackformastercard-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Dispute Rules Content Pack for Mastercard release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Dispute Rules Content Pack for Mastercard from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Dispute Rules Content Pack for Mastercard release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Dispute Rules Content Pack for Mastercard to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

The Australia release adds new data fields to the Authorization and Financial Transaction tables to support the new eligibility rules. The `transactionAmountLocal` field already exists in the Financial Transaction table but is being extended to the Financial Transaction Authorization table in this release. No other pre-existing fields are affected. After upgrading, confirm that the new fields are available and populated on your instance.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Dispute Rules Content Pack for Mastercard.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Decision tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&family=xanadu&ft:locale=en-US)**

Streamline dispute processing by validating Mastercard transaction details and questionnaire answers against the eligibility rules in the decision tables that are included in this application.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[New data fields for Mastercard chargeback eligibility rules](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

New data fields sourced from the Mastercard authorization API and Mastercard clearing API have been added to support the expanded eligibility rules. Fields sourced from the Mastercard authorization API are available on the Financial Transaction Authorization table. Fields sourced from the Mastercard clearing API are available on the Financial Transaction table.


</td></tr><tr><td>

Australia

</td><td>

-   **[July Store Release: New data field for Mastercard chargeback ineligibility rule assessment](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

A new Mastercard data field `programRegistrationId` has been added to the Financial Transaction table to support chargeback ineligibility rule evaluation for RC 4853 Cardholder Disputes sub-categories. The field is sourced from the Mastercard clearing API.

This field identifies the program registration associated with a clearing transaction. The field displays both the program code and its description. Supported values include codes for person-to-person transfers, business disbursements, government and non-profit disbursements, merchant-presented QR transactions, and other Mastercard Send program types.

-   **[July Store Release: New input variables for Mastercard chargeback ineligibility rule assessment decision tables](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

New input variables have been added to support updated chargeback ineligibility rule evaluation for RC 4808 Authorization sub-categories. The following computed values are used as decision inputs across the Required Authorization Not Obtained, Expired Chargeback Protection Period, Stand-in or X-Code Approval after Issuer Decline, CAT 3 Devices, and Transit First Ride Risk Framework Claims decision tables:

    -   `transit_clearing_amount_sum` — the sum of local transaction amounts for matching transit clearing transactions, used to evaluate UK domestic contactless transit split-clearing ineligibility conditions.
    -   `cpd_minus_declined_transit_auth_date_time` — the number of days between a declined transit authorization and the chargeback protection date \(CPD\), used to assess TFRR/FRIL eligibility windows.
    -   `financial_local_txn_amt_minus_auth_local_txn_amt` — the difference between the financial and authorization local transaction amounts, used for RANO authorization amount difference conditions.
-   **[July Store Release: New Mastercard dispute sub-categories](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

The following new Mastercard dispute sub-categories are available:

    -   Installment Billing Dispute-Participating Countries \(RC 4850\)
    -   Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(RC 4854\)

</td></tr><tr><td>

Brazil

</td><td>

-   **New data field for Mastercard transit chargeback eligibility rules**

Assess transit chargeback eligibility using the transit transaction type indicator on the Financial Transaction table. The field is sourced from the **transitProgramCode** field of the Mastercard clearing API and supports Mastercard-defined values 01 through 10.

-   **New input variable for Mastercard chargeback ineligibility rule assessment decision tables**

Evaluate chargeback ineligibility conditions against a fixed Mastercard rule effective date without editing decision tables. The **days\_until\_mastercard\_rule\_effective\_date** parameter calculates the number of days until the rule takes effect. The parameter is used as a decision input across the reason code \(RC\) 4808 Authorization and RC 4837, RC 4849, RC 4870, and RC 4871 Fraud decision tables.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Dispute Rules Content Pack for Mastercard features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Updated references from questionnaire tables to intake tables in Card Operations](https://www.servicenow.com/docs/access?context=components-installed-with-dispute-rules-content-pack-for-mastercard&family=xanadu&ft:locale=en-US)**

Updated references from the old questionnaire tables to the new intake tables in Card Operations.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Processing Errors](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

Ineligibility rule conditions have been updated across the RC 4834 Processing Errors sub-categories to align with the latest Mastercard Chargeback Guide. Updated sub-categories include Transaction Amount Differs, Currency Errors, Cardholder Debited More than Once for the Same Goods or Services, ATM Funds Not Dispensed, Charges for Loss, Theft, or Damages, Merchant Refund Correcting Error Resulted in Cardholder Currency Exchange Loss, Improper Merchant Surcharge, Unreasonable Amount, and Cash was not properly provided from a Purchase with Cash Back transaction.

For Currency Errors: A new ineligibility condition has been added. CE is not applicable for ATM transactions \(MCC 6011\) where either the card was issued outside Europe or the terminal is located outside Europe.

For Transaction Amount Differs: The documentation requirements for this sub-category have been updated. For Maestro cards issued in Europe used at terminals outside Europe, no documentation is required. Brazil domestic disputes involving gratuity amounts now have explicit documentation requirements.

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Cardholder Disputes](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

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


</td></tr><tr><td>

Australia

</td><td>

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Processing Errors](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

Ineligibility rule conditions have been updated across the RC 4834 Processing Errors sub-categories to align with the latest Mastercard Chargeback Guide. Updated sub-categories include Transaction Amount Differs, Currency Errors, Cardholder Debited More than Once for the Same Goods or Services, ATM Funds Not Dispensed, Charges for Loss, Theft, or Damages, Merchant Refund Correcting Error Resulted in Cardholder Currency Exchange Loss, Improper Merchant Surcharge, Unreasonable Amount, and Cash was not properly provided from a Purchase with Cash Back transaction.

For Currency Errors: A new ineligibility condition has been added. CE is not applicable for ATM transactions \(MCC 6011\) where either the card was issued outside Europe or the terminal is located outside Europe.

For Transaction Amount Differs: The documentation requirements for this sub-category have been updated. For Maestro cards issued in Europe used at terminals outside Europe, no documentation is required. Brazil domestic disputes involving gratuity amounts now have explicit documentation requirements.

-   **[July Store Release: Build and update Mastercard chargeback ineligibility rules — Cardholder Disputes](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

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


</td></tr><tr><td>

Brazil

</td><td>

-   **Updated Mastercard chargeback ineligibility rules for fraud**

Ineligibility rule conditions are updated for the following reason codes:

    -   RC 4837 \(No Cardholder Authorization\)
    -   RC 4849 \(Questionable Merchant Activity\)
    -   RC 4870 \(Chip Liability Shift\)
    -   RC 4871 \(Chip Liability Shift, Lost, Stolen, or Never Received Issue \(NRI\) Fraud\)
The Mastercard Commercial Payments Account ineligibility condition and its associated formula apply only until the Mastercard rule effective date of October 23, 2026. The same condition applies across all four reason codes. The chargeback ineligibility reason text for RC 4849 is also updated to match the wording in the Mastercard Chargeback Guide.

-   **Updated Mastercard chargeback ineligibility rules for authorization**

Ineligibility rule conditions are added or updated for the following RC 4808 Authorization sub-categories:

    -   Required Authorization Not Obtained \(RANO\). A new ineligibility condition applies to automated fuel dispenser transactions under merchant category code 5542 in Japan. The condition applies to transactions up to JPY 15,000 at CAT 1, CAT 2, and CAT 6 terminals. This condition takes effect after October 23, 2026.
    -   Transit First Ride Risk Framework Claims \(TFRR\) and Transit First Ride Issuer Liability Framework Claims \(FRIL\). Two conditions and their associated formula read the transit transaction type indicator from the Financial Transaction table instead of the Financial Transaction Authorization table.
-   **Transit transaction type indicator values**

The transit transaction type indicator values on the Financial Transaction Authorization table match the current Mastercard specification. Value 02 reads Deferred retail like, and values 09 and 10 are available for selection.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Dispute Rules Content Pack for Mastercard features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Dispute Rules Content Pack for Mastercard features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

For July store release, the sub-category RC 4834 — Late Presentment has been removed.

</td></tr><tr><td>

Australia

</td><td>

For July store release, the sub-category RC 4834 — Late Presentment has been removed.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Dispute Rules Content Pack for Mastercard.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Dispute Rules Content Pack for Mastercard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Dispute Rules Content Pack for Mastercard by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Dispute Rules Content Pack for Mastercard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Dispute Rules Content Pack for Mastercard from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US). to install it on your instance.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Dispute Rules Content Pack for Mastercard we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Additional requirements**

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.


</td></tr><tr><td>

Australia

</td><td>

-   **Additional requirements**

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.


</td></tr><tr><td>

Brazil

</td><td>

-   **Additional requirements**

Requires Financial Services Card Operations \(sn\_bom\_credit\_card\).


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Dispute Rules Content Pack for Mastercard we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Dispute Rules Content Pack for Mastercard, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Dispute Rules Content Pack for Mastercard we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Dispute Rules Content Pack for Mastercard we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Run chargeback eligibility rules based on Mastercard rules.
-   Determine the chargeback eligibility for Mastercard transactions by using the provided decision tables. The eligibility is based on the reason code, intake responses, and transaction data from the dispute.

 See [Dispute Rules Content Pack for Mastercard](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Developed and refined chargeback eligibility rules to validate dispute cases against Mastercard core rules.
-   Updated the intake questionnaire for various dispute categories.

 See [Dispute Rules Content Pack for Mastercard](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Keep Mastercard dispute assessments compliant with updated chargeback ineligibility rules across the Authorization, Processing Errors, and Cardholder Disputes categories.
-   Assess chargeback eligibility accurately using new data fields sourced from the Mastercard authorization and clearing APIs.

 See [Dispute Rules Content Pack for Mastercard](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

Dispute Rules Content Pack for Mastercard enables you to manage and resolve Mastercard disputes, determine chargeback eligibility based on Mastercard rules, and categorize disputes using predefined criteria for accurate processing.

 See [Dispute Rules Content Pack for Mastercard](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

