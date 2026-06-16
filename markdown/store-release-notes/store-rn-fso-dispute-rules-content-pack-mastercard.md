---
title: Dispute Rules Content Pack for Mastercard release notes
description: Version history for the Dispute Rules Content Pack for Mastercard application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-dispute-rules-content-pack-mastercard.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Dispute Rules Content Pack for Mastercard release notes

Version history for the Dispute Rules Content Pack for Mastercard application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.1.0 - June 2026 \(Zurich\)**
    -   Changed:
        -   Updated the ineligibility reason for Mastercard reason code 4871 \(Chip Liability Shift - Lost/Stolen/Never Received Issue Fraud\) to clarify that this reason code is not applicable for transactions reported as lost, stolen, or never received to the fraud and loss database within three days of the chargeback date, in accordance with Mastercard's fraud and loss database reporting requirements.
        -   Refined decision table rules and subflow logic for Mastercard reason code 4871 to ensure accurate eligibility determination based on updated Mastercard guidelines.
-   **Version 4.0.1 - May 2026 \(Zurich\)**
    -   New:
        -   Added Mastercard chargeback eligibility rules for Reason Code 4808 - RANO \(Request Authorization Not Obtained\) in the Authorization dispute category, helping determine when chargebacks can be filed for unauthorized transactions
        -   Added Mastercard chargeback eligibility rules for Reason Code 4808 - SIXCAID \(Subsequent Installment Charges After Account Identification\) in the Authorization dispute category for contactless transit transactions and other scenarios
        -   Added Mastercard chargeback eligibility rules for Reason Code 4808 - TFRR \(Transaction Fraud Reporting Requirement\) in the Authorization dispute category
        -   Added Mastercard chargeback eligibility rules for Reason Code 4808 - CAT3D \(Category 3 Devices\) in the Authorization dispute category with enhanced conditions for device-based transactions
        -   Added Mastercard chargeback eligibility rules for Reason Code 4808 - ECPP \(EMV Chip and PIN Processing\) in the Authorization dispute category
        -   Added Mastercard chargeback eligibility rules for Reason Code 4853 - Failed Travel for Intra-EEA and Domestic European transactions
        -   Added Mastercard chargeback eligibility rules for Fraud dispute category covering multiple reason codes:
            -   Reason Code 4870 \(Chip Liability Shift\)
            -   Reason Code 4871 \(Chip/PIN Liability Shift\)
            -   Reason Code 4837 \(No Cardholder Authorization\)
            -   Reason Code 4849 \(Questionable Merchant Activity\)
-   **Version 3.1.0 - March 2026**
    -   New:
        -   Added L1 &amp; L2 questions for RC 4808 Stand-in or X-Code Approval after Issuer Decline.
        -   Added Mastercard Chargeback eligibility rules for RC 4834 - Cash was not properly provided.
        -   Added L1 &amp; L2 questions for RC 4834 - Cash was not properly provided from either a Purchase with Cash Back transaction or a Cash Back transaction without an Accompanying Purchase.
    -   Changed:
        -   Updated Mastercard 4834 chargeback eligibility conditions for TAD.
        -   Updated L2 questionnaire mapping logic for Mastercard chargeback reason codes 4870/4871 based on card possession status.
        -   Updated L1 &amp; L2 decision table for the below Mastercard chargeback reason codes based on transactional data fields 'Response Code' and 'Processing Code'.
            -   RC4808
            -   RC 4834
        -   Updated 4834 Cash not properly provided from cash-back purchase or cash-back only transaction DT and Subflow Names.
    -   Fixed:
        -   Fixed missing RC 4834 prefix to an existing reason code message.
        -   Fixed chargeback eligibility logic for the Yes case in the relevant subflows.
-   **Version 3.0.0 - December 2025**
    -   New:
        -   Chargeback Eligibility Rules: Expanded Mastercard Chargeback eligibility rules for multiple reason codes.
        -   Decision Table Enhancements: Added new subflows, decision tables, and transaction count validation for specific dispute scenarios, enhancing automation and accuracy in dispute handling.
    -   Changed: Eligibility Rule Updates: Updated Mastercard Chargeback eligibility rules for various reason codes to reflect latest requirements, including changes to condition logic, input types, and message clarity.
    -   Fixed:
        -   Duplicate and Unused Conditions: Removed duplicate and unused conditions and files from decision tables, streamlining logic and reducing maintenance overhead.
        -   Processing Logic Issues: Fixed issues with processing code conditions, field mappings, and output results in subflows to ensure accurate and reliable system behavior.
-   **Version 2.3.0 - August 2025**

    New: As part of this release, Deny ACLs were introduced on the existing tables. These Deny ACLs will restrict access for unauthenticated users on CRUD operations.

-   **Version 2.2.0 - March 2025**
    -   Fixed: Fixed chargeback eligibility reason NULL issue for single result
    -   New: Added type filter for flows/subflows querying Dispute intake to query only Dispute Request type intake
-   **Version 2.1.0 - February 2025**

     Changed : Updated references of old questionnaire tables with new intake tables from Financial Services Card Operations. 

-   **Version 2.0.0 - November 2024**

    Changed: Updated references of old questionnaire tables with new intake tables from Card operations.

-   **Version 1.0.3 - October 2024**

    Updated: Enabled app visibility on store.

-   **Version 1.0.0 - August 2024**

    The application provides questionnaire for intake of dispute related information under various dispute categories as per Mastercard guidelines.. Embed auto-updated rules in yourdisputes process​


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

