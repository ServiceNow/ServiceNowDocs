---
title: Combined Dispute Rules Content Pack for Mastercard release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Dispute Rules Content Pack for Mastercard from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-disputerulescontentpackformastercard-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 27
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

-   **[July Store Release: New data field for Mastercard chargeback ineligibility rule assessment](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

A new Mastercard data field `programRegistrationId` has been added to the Financial Transaction table to support chargeback ineligibility rule evaluation for RC 4853 Cardholder Disputes sub-categories. The field is sourced from the Mastercard clearing API.

This field identifies the program registration associated with a clearing transaction. The field displays both the program code and its description. Supported values include codes for person-to-person transfers, business disbursements, government and non-profit disbursements, merchant-presented QR transactions, and other Mastercard Send program types.

-   **[July Store Release: New input variables for Mastercard chargeback ineligibility rule assessment decision tables](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

New input variables have been added to support updated chargeback ineligibility rule evaluation for RC 4808 Authorization sub-categories. The following computed values are used as decision inputs across the Required Authorization Not Obtained, Expired Chargeback Protection Period, Stand-in or X-Code Approval after Issuer Decline, CAT 3 Devices, and Transit First Ride Risk Framework Claims decision tables:

    -   `transit_clearing_amount_sum` — the sum of local transaction amounts for matching transit clearing transactions, used to evaluate UK domestic contactless transit split-clearing ineligibility conditions.
    -   `cpd_minus_declined_transit_auth_date_time` — the number of days between a declined transit authorization and the chargeback protection date \(CPD\), used to assess TFRR/FRIL eligibility windows.
    -   `financial_local_txn_amt_minus_auth_local_txn_amt` — the difference between the financial and authorization local transaction amounts, used for RANO authorization amount difference conditions.
-   **[July Store Release: New Mastercard dispute sub-categories](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

The following new Mastercard dispute sub-categories are available:

    -   Installment Billing Dispute-Participating Countries \(RC 4850\)
    -   Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(RC 4854\)

 -   **[New data fields for Mastercard chargeback eligibility rules](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

New data fields sourced from the Mastercard authorization API and Mastercard clearing API have been added to support the expanded eligibility rules. Fields sourced from the Mastercard authorization API are available on the Financial Transaction Authorization table. Fields sourced from the Mastercard clearing API are available on the Financial Transaction table.


 -   **[Decision tables for Mastercard dispute processing](https://www.servicenow.com/docs/access?context=dispute-decision-tables&family=zurich&ft:locale=en-US)**

Streamline dispute processing by validating Mastercard transaction details and questionnaire answers against the eligibility rules in this application's decision tables.


</td></tr><tr><td>

Australia

</td><td>

-   **New choice values for Mastercard transactional data fields**

Use the new **processing\_code** and **merchant\_advice\_code** choice values on the Financial Transaction Authorization table to align with the current authorization data requirements of Mastercard.

**processing\_code** values:

    -   00 Purchase
    -   01 Withdrawal
    -   02 Debit Adjustment
    -   09 Purchase with Cash Back
    -   10 Visa Only. Account Funding
    -   17 Cash Disbursement
    -   18 Scrip Issue
    -   20 Purchase Return/Refund
    -   21 Deposit
    -   22 Credit Adjustment
    -   28 Payment Transaction
    -   30 Balance Inquiry
    -   40 Account Transfer
    -   90 Reserved for Future Use
    -   91 PIN Unblock
    -   92 PIN Change
**merchant\_advice\_code** values:

    -   01 New account information available
    -   02 Cannot approve at this time, try again later
    -   03 Do not try again
    -   04 Token requirements not fulfilled for this token type
    -   05 Negotiated value not approved
    -   06 Original Transaction Approved
    -   07 Original Transaction Declined
    -   08 Original Transaction Approval Status Unknown
    -   21 Payment Cancellation
    -   22 Merchant does not qualify for product code
    -   24 Retry after 1 hour
    -   25 Retry after 24 hours
    -   26 Retry after 2 days
    -   27 Retry after 4 days
    -   28 Retry after 6 days
    -   29 Retry after 8 days
    -   30 Retry after 10 days
    -   40 Consumer non-reloadable prepaid card
    -   41 Consumer single-use virtual card number
    -   42 Sanctions score limit exceeded
    -   43 Consumer multi-use virtual card number
    -   44 Processing in progress
    -   blank \(no value\) Retry with PIN
    -   90 Issuer decisioned
    -   99 Mastercard decisioned

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

 -   **[May Store Release: New data fields for Mastercard chargeback eligibility rules](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

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

</td></tr><tr><td>

Brazil

</td><td>

-   **New choice values for Mastercard transactional data fields**

Use the new **processing\_code** and **merchant\_advice\_code** choice values on the Financial Transaction Authorization table to align with the current authorization data requirements of Mastercard.

**processing\_code** values:

    -   00 Purchase
    -   01 Withdrawal
    -   02 Debit Adjustment
    -   09 Purchase with Cash Back
    -   10 Visa Only. Account Funding
    -   17 Cash Disbursement
    -   18 Scrip Issue
    -   20 Purchase Return/Refund
    -   21 Deposit
    -   22 Credit Adjustment
    -   28 Payment Transaction
    -   30 Balance Inquiry
    -   40 Account Transfer
    -   90 Reserved for Future Use
    -   91 PIN Unblock
    -   92 PIN Change
**merchant\_advice\_code** values:

    -   01 New account information available
    -   02 Cannot approve at this time, try again later
    -   03 Do not try again
    -   04 Token requirements not fulfilled for this token type
    -   05 Negotiated value not approved
    -   06 Original Transaction Approved
    -   07 Original Transaction Declined
    -   08 Original Transaction Approval Status Unknown
    -   21 Payment Cancellation
    -   22 Merchant does not qualify for product code
    -   24 Retry after 1 hour
    -   25 Retry after 24 hours
    -   26 Retry after 2 days
    -   27 Retry after 4 days
    -   28 Retry after 6 days
    -   29 Retry after 8 days
    -   30 Retry after 10 days
    -   40 Consumer non-reloadable prepaid card
    -   41 Consumer single-use virtual card number
    -   42 Sanctions score limit exceeded
    -   43 Consumer multi-use virtual card number
    -   44 Processing in progress
    -   blank \(no value\) Retry with PIN
    -   90 Issuer decisioned
    -   99 Mastercard decisioned

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


 -   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


 -   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

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
-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

Updated the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard by adding new questions and updating existing questions.


</td></tr><tr><td>

Australia

</td><td>

-   **Updated Mastercard chargeback ineligibility decision tables for fraud \(RC 4870 and RC 4871\)**

The ineligibility condition for RC 4871 \(Chip Liability Shift, Lost, Stolen, or Never Received Issue \(NRI\) Fraud\) in the **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision table reverses the comparison for the fraud-report timing window. Before this release, a dispute was ineligible when it was raised fewer than three days after the transaction was reported lost, stolen, or never received in the fraud and loss database. A dispute is ineligible when it is raised more than three days after the report. The condition also requires a fraud report ID to be present; this requirement is unchanged. The associated chargeback ineligibility reason text is updated to match the current wording in the Mastercard Chargeback Guide.

The **Mastercard 4870 - Chip Liability Shift** and **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision tables each change the ineligibility condition for repeat fraud chargebacks on the same Mastercard card account. Before this release, a dispute was ineligible when the **Chargeback transactions count** was three or more. The count included chargebacks under RC 4837, RC 4870, or RC 4871, regardless of when they were submitted. The condition uses a new input, **Fraud CB count before auth date**, and a dispute is ineligible when the count is two or more. The new count includes only chargebacks that were submitted before the authorization date of the disputed transaction. The chargeback ineligibility reason text in both decision tables is updated to specify fraud chargebacks.

-   **Updated Mastercard chargeback ineligibility decision table for Refund Not Processed \(RC 4853\)**

The **Mastercard 4853 - Credit Not Processed** decision table adds a condition to the ineligibility rule for RC 4853 \(Refund Not Processed\). Before this release, a dispute was ineligible when the transaction had one of the merchant category codes \(MCCs\) 3000 through 3999, 4411, 4511, 4722, 6513, 7011, 7512, 7519, or 7922. The MCC list is unchanged. A dispute with one of these MCCs is ineligible only when the merchant provided a voucher for future use and disclosed it in its terms and conditions. The new condition checks that the answer to the merchant voucher question in the dispute questionnaire is Yes. The chargeback ineligibility reason text is updated to describe the voucher condition.


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


 -   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

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
-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

Benefit from the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard with some modified questions and added hard stop alerts.


</td></tr><tr><td>

Brazil

</td><td>

-   **Updated Mastercard chargeback ineligibility decision tables for Colombian reversion of payment claims \(RC 4837, RC 4870, and RC 4871\)**

Review updated chargeback eligibility for Mastercard fraud disputes on Colombian transactions. Eligibility now depends on the dispute agent's answer to the reversion of payment claim question in the dispute questionnaire. The question asks whether the cardholder filed a reversion of payment claim \(RP-Reg\) under Law 1480 of 2011, Article 51, and Decree 587 of 2016. Under the Mastercard guide, RC 4837, RC 4870, and RC 4871 do not apply to a Colombian domestic transaction that the reversion of payments regulation addresses.

The following decision tables each change the ineligibility condition for their Colombia rule:

    -   **Mastercard 4837 - No Cardholder Authorization**
    -   **Mastercard 4870 - Chip Liability Shift**
    -   **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud**
Before this release, each rule decided that a dispute was ineligible from the authorization data alone. A dispute was ineligible when the authorization had a fee collection function code or the original message type identifier 1740, the acceptor country was Colombia, and the cardholder billing currency was Colombian Peso \(170\). A dispute is now ineligible when the answer to the **This dispute is due to \(Mastercard\)** question on the dispute intake record matches the reason code of the decision table and the answer to the reversion of payment claim question is Yes. When the answer is No, this rule does not make the dispute ineligible.

The location and currency checks now apply to the question rather than to the rule. The dispute questionnaire asks the question only for Mastercard disputes with RC 4837, 4870, or 4871 when the acceptor country is Colombia and the cardholder billing currency is Colombian Peso. The dispute questionnaire change is described in the Financial Services Card Operations release notes.

-   **Updated Mastercard chargeback ineligibility decision tables for fraud report checks \(RC 4837, RC 4849, RC 4870, and RC 4871\)**

Review updated chargeback eligibility for Mastercard fraud disputes. Eligibility now depends on whether the transaction was reported as fraud before the chargeback. This reflects the Mastercard requirement that the issuer report the transaction as fraud on or before the date of the chargeback. The following decision tables each change the fraud report ID condition:

    -   **Mastercard 4837 - No Cardholder Authorization** for Mainland China domestic transactions and for all other transactions
    -   **Mastercard 4849 - Questionable Merchant Activity** for Mainland China domestic transactions and for all other transactions
    -   **Mastercard 4870 - Chip Liability Shift** for Mainland China domestic transactions
    -   **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** for the fraud report timing rule
Before this release, the RC 4837 conditions made a dispute ineligible when a fraud report ID was present, and the RC 4849 conditions made a dispute ineligible when both a fraud report ID and a Mastercard fraud type were present. A dispute is now ineligible when the fraud report ID is empty, and the RC 4849 conditions no longer check the fraud type. For RC 4870, a dispute for a Mainland China domestic transaction was ineligible when the fraud type was not 04 and a fraud report ID was present. The dispute is now ineligible when the fraud type is not 04 or the fraud report ID is empty. The chargeback ineligibility reason text for RC 4837 is updated to say that the transaction was not reported on or before initiating a chargeback.

For RC 4871, the rule that makes a dispute ineligible after the fraud report no longer requires a fraud report ID. A dispute is ineligible when the fraud type is 00, 01, or 02 and the dispute is raised more than three days after the fraud report date.

-   **Updated Mastercard chargeback ineligibility decision table for Credit Posted as a Purchase \(RC 4853\)**

Review the updated **Mastercard 4853 - Credit Posted as a Purchase** decision table, which changes the ineligibility condition for the **Refund posted as a purchase** dispute reason. Before this release, a dispute was ineligible when the disputed amount was not equal to twice the original transaction amount. A dispute is now ineligible when the disputed amount is more than twice the original transaction amount. The chargeback ineligibility reason text is updated to say that the disputed amount should not exceed twice the original transaction amount.

The decision input for the condition is renamed from **dispute\_amount\_neq\_twice\_transaction\_amount** to **dispute\_amount\_gt\_twice\_transaction\_amount**. If you reference the input in a customization, update the reference.

-   **Updated Mastercard chargeback ineligibility decision table for repeat fraud chargebacks and digital goods \(RC 4837\)**

Review two updated ineligibility conditions in the **Mastercard 4837 - No Cardholder Authorization** decision table.

The condition for repeat fraud chargebacks on the same Mastercard card account uses the **Fraud CB count before auth date** input. Before this release, a dispute was ineligible when the **Chargeback transactions count** was three or more, regardless of when the chargebacks were submitted. A dispute is now ineligible when the count is two or more. The new count includes only chargebacks that were submitted before the authorization date of the disputed transaction.

The condition for digital goods purchases of USD 25 or less now evaluates card data input mode S or R and the merchant category codes \(MCCs\) 5815, 5816, 5817, and 5818.

-   **Removed Mastercard chargeback ineligibility rules \(RC 4837, RC 4849, and RC 4871\)**

Review the following updated ineligibility rules, which no longer apply. Disputes that previously matched them are no longer ineligible on that basis:

    -   The **Mastercard 4849 - Questionable Merchant Activity** decision table no longer includes the rule that made a dispute ineligible when the cardholder had neither attempted to file a police complaint nor completed a coercion claim affidavit.
    -   The **Mastercard 4837 - No Cardholder Authorization** decision table no longer includes the rule for transactions with wallet identifier 101 and e-commerce indicator 221, 222, or 225.
    -   The **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision table no longer includes the rule that made a dispute ineligible when the POS card data terminal input capability was not 2, or when the cardholder authentication method was PIN and the response code was 00. The rule applied to all regions.
The removals apply to new and existing installations.


 -   **Updated Mastercard chargeback ineligibility decision tables for fraud \(RC 4870 and RC 4871\)**

The ineligibility condition for RC 4871 \(Chip Liability Shift, Lost, Stolen, or Never Received Issue \(NRI\) Fraud\) in the **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision table reverses the comparison for the fraud-report timing window. Before this release, a dispute was ineligible when it was raised fewer than three days after the transaction was reported lost, stolen, or never received in the fraud and loss database. A dispute is ineligible when it is raised more than three days after the report. The condition also requires a fraud report ID to be present; this requirement is unchanged. The associated chargeback ineligibility reason text is updated to match the current wording in the Mastercard Chargeback Guide.

The **Mastercard 4870 - Chip Liability Shift** and **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision tables each change the ineligibility condition for repeat fraud chargebacks on the same Mastercard card account. Before this release, a dispute was ineligible when the **Chargeback transactions count** was three or more. The count included chargebacks under RC 4837, RC 4870, or RC 4871, regardless of when they were submitted. The condition uses a new input, **Fraud CB count before auth date**, and a dispute is ineligible when the count is two or more. The new count includes only chargebacks that were submitted before the authorization date of the disputed transaction. The chargeback ineligibility reason text in both decision tables is updated to specify fraud chargebacks.

-   **Updated Mastercard chargeback ineligibility decision table for Refund Not Processed \(RC 4853\)**

The **Mastercard 4853 - Credit Not Processed** decision table adds a condition to the ineligibility rule for RC 4853 \(Refund Not Processed\). Before this release, a dispute was ineligible when the transaction had one of the merchant category codes \(MCCs\) 3000 through 3999, 4411, 4511, 4722, 6513, 7011, 7512, 7519, or 7922. The MCC list is unchanged. A dispute with one of these MCCs is ineligible only when the merchant provided a voucher for future use and disclosed it in its terms and conditions. The new condition checks that the answer to the merchant voucher question in the dispute questionnaire is Yes. The chargeback ineligibility reason text is updated to describe the voucher condition.


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


**Important:** Dispute Rules Content Pack for Mastercard is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Dispute Rules Content Pack for Mastercard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Dispute Rules Content Pack for Mastercard is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

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

