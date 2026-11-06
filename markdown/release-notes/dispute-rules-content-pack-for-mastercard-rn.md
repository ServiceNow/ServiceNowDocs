---
title: Dispute Rules Content Pack for Mastercard release notes
description: Dispute Rules Content Pack for Mastercard supports the intake of dispute-related information under various dispute categories according to Mastercard guidelines.Stay current with Mastercard chargeback rules. This update refines the chargeback eligibility conditions in the decision tables for reason codes \(RCs\) 4837, 4849, 4853, 4870, and 4871, including Colombian transactions subject to the reversion of payment regulation, and removes several ineligibility rules.Maintain compliance with the latest Mastercard chargeback rules. This release adds new transactional data field values for Mastercard authorization processing and refines the chargeback eligibility conditions in the decision tables for reason codes \(RCs\) 4853, 4870, and 4871.Maintain compliance with the latest Mastercard chargeback rules. This release updates fraud and authorization dispute assessments to align with Mastercard's October 2026 rule changes, adds support for transit transaction types, and introduces time-based rule evaluation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/dispute-rules-content-pack-for-mastercard-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 11
keywords: [Mastercard disputes, chargeback rules, dispute management, Mastercard, chargeback, dispute rules, fraud, reason codes, Colombia, reversion of payment, Mastercard, chargeback, dispute rules, fraud, reason codes, transaction data, Mastercard, chargeback, dispute rules, fraud, authorization, transit transactions]
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Dispute Rules Content Pack for Mastercard release notes

Dispute Rules Content Pack for Mastercard supports the intake of dispute-related information under various dispute categories according to Mastercard guidelines.

## About Dispute Rules Content Pack for Mastercard

Dispute Rules Content Pack for Mastercard enables you to manage and resolve Mastercard disputes, determine chargeback eligibility based on Mastercard rules, and categorize disputes using predefined criteria for accurate processing.

See [Dispute Rules Content Pack for Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Dispute Rules Content Pack for Mastercard from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html). to install it on your instance.

-   **Additional requirements**

    Requires Financial Services Card Operations \(sn\_bom\_credit\_card\).


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/financial-services-operations-rn-landing.md)

## Version 5.3.1

Stay current with Mastercard chargeback rules. This update refines the chargeback eligibility conditions in the decision tables for reason codes \(RCs\) 4837, 4849, 4853, 4870, and 4871, including Colombian transactions subject to the reversion of payment regulation, and removes several ineligibility rules.

### What's changed

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


## Version 5.2.2

Maintain compliance with the latest Mastercard chargeback rules. This release adds new transactional data field values for Mastercard authorization processing and refines the chargeback eligibility conditions in the decision tables for reason codes \(RCs\) 4853, 4870, and 4871.

### What's new

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

### What's changed

-   **Updated Mastercard chargeback ineligibility decision tables for fraud \(RC 4870 and RC 4871\)**

    The ineligibility condition for RC 4871 \(Chip Liability Shift, Lost, Stolen, or Never Received Issue \(NRI\) Fraud\) in the **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision table reverses the comparison for the fraud-report timing window. Before this release, a dispute was ineligible when it was raised fewer than three days after the transaction was reported lost, stolen, or never received in the fraud and loss database. A dispute is ineligible when it is raised more than three days after the report. The condition also requires a fraud report ID to be present; this requirement is unchanged. The associated chargeback ineligibility reason text is updated to match the current wording in the Mastercard Chargeback Guide.

    The **Mastercard 4870 - Chip Liability Shift** and **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision tables each change the ineligibility condition for repeat fraud chargebacks on the same Mastercard card account. Before this release, a dispute was ineligible when the **Chargeback transactions count** was three or more. The count included chargebacks under RC 4837, RC 4870, or RC 4871, regardless of when they were submitted. The condition uses a new input, **Fraud CB count before auth date**, and a dispute is ineligible when the count is two or more. The new count includes only chargebacks that were submitted before the authorization date of the disputed transaction. The chargeback ineligibility reason text in both decision tables is updated to specify fraud chargebacks.

-   **Updated Mastercard chargeback ineligibility decision table for Refund Not Processed \(RC 4853\)**

    The **Mastercard 4853 - Credit Not Processed** decision table adds a condition to the ineligibility rule for RC 4853 \(Refund Not Processed\). Before this release, a dispute was ineligible when the transaction had one of the merchant category codes \(MCCs\) 3000 through 3999, 4411, 4511, 4722, 6513, 7011, 7512, 7519, or 7922. The MCC list is unchanged. A dispute with one of these MCCs is ineligible only when the merchant provided a voucher for future use and disclosed it in its terms and conditions. The new condition checks that the answer to the merchant voucher question in the dispute questionnaire is Yes. The chargeback ineligibility reason text is updated to describe the voucher condition.


## Version 5.1.0

Maintain compliance with the latest Mastercard chargeback rules. This release updates fraud and authorization dispute assessments to align with Mastercard's October 2026 rule changes, adds support for transit transaction types, and introduces time-based rule evaluation.

### What's new

-   **New data field for Mastercard transit chargeback eligibility rules**

    Assess transit chargeback eligibility using the transit transaction type indicator on the Financial Transaction table. The field is sourced from the **transitProgramCode** field of the Mastercard clearing API and supports Mastercard-defined values 01 through 10.

-   **New input variable for Mastercard chargeback ineligibility rule assessment decision tables**

    Evaluate chargeback ineligibility conditions against a fixed Mastercard rule effective date without editing decision tables. The **days\_until\_mastercard\_rule\_effective\_date** parameter calculates the number of days until the rule takes effect. The parameter is used as a decision input across the reason code \(RC\) 4808 Authorization and RC 4837, RC 4849, RC 4870, and RC 4871 Fraud decision tables.


### What's changed

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


