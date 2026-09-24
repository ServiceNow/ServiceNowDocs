---
title: Dispute Rules Content Pack for Mastercard release notes
description: Dispute Rules Content Pack for Mastercard supports the intake of dispute-related information under various dispute categories according to Mastercard guidelines.Maintain compliance with the latest Mastercard chargeback rules. This release updates fraud and authorization dispute assessments to align with Mastercard's October 2026 rule changes, adds support for transit transaction types, and introduces time-based rule evaluation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/dispute-rules-content-pack-for-mastercard-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Mastercard disputes, chargeback rules, dispute management, Mastercard, chargeback, dispute rules, fraud, authorization, transit transactions]
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Dispute Rules Content Pack for Mastercard release notes

Dispute Rules Content Pack for Mastercard supports the intake of dispute-related information under various dispute categories according to Mastercard guidelines.

## About Dispute Rules Content Pack for Mastercard

Dispute Rules Content Pack for Mastercard enables you to manage and resolve Mastercard disputes, determine chargeback eligibility based on Mastercard rules, and categorize disputes using predefined criteria for accurate processing.

See [Dispute Rules Content Pack for Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-rules-content-pack-for-mastercard-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Dispute Rules Content Pack for Mastercard from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html). to install it on your instance.

-   **Additional requirements**

    Requires Financial Services Card Operations \(sn\_bom\_credit\_card\).


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/financial-services-operations-rn-landing.md)

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


