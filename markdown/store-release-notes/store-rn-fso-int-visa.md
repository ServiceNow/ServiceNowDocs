---
title: Financial Services Operations Integration with Visa release notes
description: Version history for the Financial Services Operations Integration with Visa application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-int-visa.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Operations Integration with Visa release notes

Version history for the Financial Services Operations Integration with Visa application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.9.0 - May 2026**

    Changed: Updated Visa transaction lookup flow to properly update field values when retrieving transaction details

-   **Version 3.5.1 - May 2026 \(Zurich\)**

    Changed: Updated Visa transaction lookup subflow to update the field values when retrieving transaction details

-   **Version 3.8.0 - April 2026**
    -   Updated:
        -   Updated spokes, subflows and script include based on recent Visa 26.1 revision changes, improving compatibility and accuracy in dispute processing.
        -   Improved the process for showing initiate dispute options for Visa IFC CDRN not eligible scenarios, making user actions clearer.
        -   Updated localization artifacts to provide improved translations and support for more regions.
-   **Version 3.5.0 - April 2026 \(Zurich\)**

    Updated: Updated spokes, subflows and script include based on recent Visa revision changes, improving compatibility and accuracy in dispute processing.

-   **Version 3.6.0 - March 2026**
    -   Changed:
        -   Updated the 'Look up Associated Transactions' subflow to use the Builder and Parser Action.
        -   Updated the 'Look up Dispute Pre Arbitration Details' subflow to store the tokenized document ID.
        -   Updated the 'Look up Dispute Pre Arbitration Response Details' subflow to store the tokenized document ID.
        -   Updated the 'Look up Dispute Response Details' subflow to store the tokenized document ID.
        -   Updated the 'Look up Dispute Filing Details' subflow to store the tokenized document ID.
-   **Version 3.4.0 - December 2025**
    -   New:
        -   Property for Cardholder Purchase Inquiry: Added a new property to support cardholder purchase inquiry, enhancing the ability to retrieve and process purchase information.
        -   Spoke Selector for VROL Transaction Inquiry: Introduced a spoke selector definition for VROL transaction inquiry and associated transaction, enabling more flexible integration and automation.
    -   Removed:
        -   Unnecessary Spoke Selector Request Definition: Removed an unnecessary spoke selector request definition and its associated adapter, reducing system complexity.
        -   Get Associated Transactions BR Inactive: Made the "Get associated transactions" business rule inactive, preventing unintended rule execution.
-   **Version 3.3.1 - August 2025**

    Changed: Added two parameters in the Visa token service template.

-   **Version 3.2.0 - May 2025**
    -   Changed:
        -   Modified cardholder purchase inquiry subflow to map the shipping address to financial transaction.
        -   Modified integration subflows to use Network Transaction ID for Visa Transaction ID.
-   **Version 3.1.0 - April 2025**

    Changed

    Updated the integration subflows in accordance with the Visa 25.1 revision.

-   **Version 3.0.0 - March 2025**
    -   New:
        -   Added new integration subflows
        -   Added UI actions and activity actions for Card Disputes Task to call Visa integration flows
-   **Version 2.5.3 - February 2025**
    -   Changed:
        -   Updated references of Visa Dispute Intake table with Dispute Intake table.
        -   Updated reference of Dispute amount modification reason field to read it from intake instead of dispute case.
-   **Version 2.4.0 - November 2024**
    -   Changed:
        -   Updated references of Visa Dispute Intake table with Dispute Intake table.
        -   Updated reference of Dispute amount modification reason field to read it from intake instead of dispute case.
-   **Version 2.2.1 - October 2024**
    -   New: Added documentation files for connection attributes
    -   Updated:
        -   Updated subflows to select resource path prefix dynamically
        -   Updated sub-flows to support Visa 24.2 revision
    -   Fixed: Fixed submit dispute questionnaire subflow for 'fraud' category
-   **Version 2.0.1 - August 2024**

    Changed: Modified Get questionnaire answer subflow to handle questions not answered by the agents.

-   **Version 2.0.0 - May 2024**
    -   New: Created subflows for:
        -   Look up associated transactions
        -   Select associated transactions
        -   Submit Transaction Inquiry
        -   Change dispute status
    -   Changed:
        -   Updated Submit Dispute Questionnaire subflow to align with the Visa Dispute Questionnaire table, replacing the inputs from decision trees
        -   Modified configuration for localization support
-   **Version 1.0.0 - February 2024**
    -   Visa Inc is a world leader in digital payment technology that connects individuals and businesses. Visa Resolve Online \(VROL\) is Visa’s end to end dispute management platform. The ServiceNow Financial Services Operations Integration with Visa enables financial institutions to integrate with VROL APIs using the Visa Spoke Actions to manage various dispute lifecycle events for e.g., perform transaction search, create dispute case, submit dispute questionnaire, fraud reporting.
    -   This application lays down the framework for supporting any dispute resolution use case on ServiceNow which requires integration with Visa’s VROL. Although out of box sub-flows address certain primary integrations like creating Visa case, Visa dispute and submission of Visa questionnaire, customers can still expand the integration layer to support any business need.
    -   The integration app provides an adapter layer to plug into the dispute workflows and effectively manage dispute resolution, making it a simple, effective, and efficient solution.

