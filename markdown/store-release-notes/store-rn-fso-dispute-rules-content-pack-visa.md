---
title: Dispute Rules Content Pack for Visa release notes
description: Version history for the Dispute Rules Content Pack for Visa application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-dispute-rules-content-pack-visa.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Dispute Rules Content Pack for Visa release notes

Version history for the Dispute Rules Content Pack for Visa application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.0.0 - May 2026**
    -   New:
        -   Added Visa chargeback eligibility rules for fraud dispute categories including:
            -   Reason Code 10.2 \(EMV Liability Shift – Non-Counterfeit Fraud\)
            -   Reason Code 10.3 \(Other Fraud – Card-Present Environment\)
-   **Version 5.5.1 - March 2026**

    Fixed: Fixed chargeback eligibility logic for the Yes case in the subflows

-   **Version 5.5.0 - December 2025**

    New: Visa - Determine Chargeback Reason Code and Dispute Category: Introduced an automated decision table and subflow that intelligently derives chargeback reason codes and dispute categories for Visa transactions based on dispute intake questions. This enhancement streamlines the dispute resolution process by eliminating manual categorization and ensuring consistent application of Visa's dispute rules.

-   **Version 5.3.0 - April 2025**

    Removed chargeback eligibility rules that are no longer required to align with Visa's business updates effective April 2025.

-   **Version 5.2.0 - March 2025**
    -   Fixed: Chargeback eligibility reason NULL issue for single result
    -   New: Added type filter for flows/subflows querying Dispute intake to query only Dispute Request type intake
-   **Version 5.1.0 - February 2025**
    -   Removed: Removed Visa Dispute Intake, Visa Dispute Cardholder Intake and CRB region tables.
    -   Changed: Updated references of old intake tables with new intake tables from Financial Services Card Operations.
-   **Version 5.0.0 - November 2024**
    -   Changed: Updated references of Visa Dispute Intake table with Dispute Intake table
    -   Removed: Removed Visa Dispute Intake, Visa Dispute Cardholder Intake and CRB region tables.
-   **Version 4.1.1 - October 2024**
    -   Updated:
        -   Enabled app visibility on store
        -   Updated chargeback rules to support Visa 24.2 revision
        -   Migrated 12.1 chargeback rules to 11.3
-   **Version 4.0.3 - September 2024**
    -   Fixed:
        -   Updated the trigger condition to avoid conflict with a business rule and published "Populate dispute transaction to questionnaire" flow
        -   Updated sys\_policy for cardholder script includes to make them readonly
-   **Version 4.0.1 - August 2024**
    -   New:
        -   Added chargeback eligibility rules for new questions and chargeback eligibility rules for reason codes 13.1 / 13.5 / 10.1 / 10.3
        -   Added a new table for Visa disputes cardholder intakeModified the type of the below fields from Boolean to String
    -   Changed:
        -   Changed label of table 'Visa Dispute Questionnaire' to 'Visa Dispute Intake' and limited edit access only to agents
        -   Changed the type of the below fields from Boolean to String
            -   authorization\_request\_declined\_valid\_data\_ind
            -   cardholder\_deceased
            -   cardholder\_denies\_authorizing\_ind
            -   cardholder\_opt\_in\_ind
            -   contact\_method\_merchant\_call\_center\_ind
            -   contact\_method\_merchant\_email\_ind
            -   contact\_method\_merchant\_in\_person\_ind
            -   contact\_method\_merchant\_mail\_ind
            -   contact\_method\_merchant\_sms\_ind
            -   contact\_method\_merchant\_webform\_ind
            -   contact\_method\_with\_merchant\_ind
            -   does\_credit\_transaction\_exist
            -   merchant\_facilities\_withdrawn
            -   other\_form\_of\_payment\_ind
            -   two\_transaction\_exist\_with\_same\_authcode
-   **Version 2.0.0 - May 2024**
    -   New:
        -   Added a new Visa Dispute Questionnaire table
        -   Integrated visa questionnaire for all the categories \(Fraud, Authorization, Processing Error, and Consumer Dispute\) in the Card dispute flow
        -   Added chargeback eligibility rules for Fraud and Authorization and reason codes 13.7 and 13.9
    -   Changed:
        -   Modified existing chargeback eligibility rules for reason codes in Processing error and Consumer dispute categories
        -   Replaced decision trees with Visa Dispute Questionnaire table for questionnaires
        -   Modified the decision tables for chargeback eligiblity rules and made it read-only
        -   Modified configuration for localization support
-   **Version 1.0.0 - February 2024**

    The application provides questionnaire for intake of dispute related information under various dispute categories as per Visa guidelines. Evaluate dispute condition rules based on the Visa core rules and visa product and services rules.


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

