---
title: Financial Services Card Operations release notes
description: The ServiceNow Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.The ServiceNow Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.The ServiceNow Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.The ServiceNow Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Financial Services Card Operations release notes

The ServiceNow® Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.

## About Financial Services Card Operations

-   Resolve friendly fraud disputes by incorporating friendly fraud detection and resolution in the existing dispute flow for Visa transactions. You can take actions such as crediting the customer, denying the dispute, or initiating an exception process.
-   The Financial Services Card Operations data model is updated in this release with reparented tables to align the data and manage the dispute transactions more effectively. See [Financial Services Card Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/card-ops-landing-page.md) for more information.
-   Enhance the card disputes process with an updated end-to-end Visa disputes playbook that now includes support for reviewing associated transactions and handling pre-arbitration, arbitration, and appeals.
-   Manage and work on multiple disputed transactions for a case with individual playbooks for each disputed transaction.
-   Integrate new VROL subflows into the enhanced Visa card disputes playbook.

## Activation and other requirements

**Important:** Financial Services Card Operations is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Financial Services Card Operations by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    During the upgrade to Yokohama, the Financial Services Card Operations plugin reparents the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] to the Financial Task table \[sn\_bom\_task\] in Financial Services Operations Core.

    Reparenting leverages the benefits and advancements of ServiceNow® Financial Services Operations Core while preserving the functionality of existing applications.

    **Note:** If your instance uses the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] and it contains a large amount of data, you may experience increased upgrade times.


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/financial-services-operations-rn-landing.md)

## May 2025

The ServiceNow® Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.

### What's new

-   **[Detect friendly fraud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/resolve-friendly-fraud.md)**

    Resolve friendly fraud disputes with predefined rules to ensure consistent and precise detection of friendly fraud in Visa disputed transactions. Agents can decline requests, issue credits, or proceed with chargebacks, allowing for tailored responses based on the situation.


## Yokohama General Availability

The ServiceNow® Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.

### What's new

-   **[Enhanced Visa disputes playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/managing-card-disputes.md)**

    Leverage an updated card disputes processing flow to associate additional transactions, manage multiple transaction disputes, and handle pre-arbitration, arbitration, and appeal requests to Visa for allocation and collaboration chargeback workflows.


## Yokohama

The ServiceNow® Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.

### What's changed

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/card-operations-reference.md)**

    Updated the following columns to align with release 25.1 revision changes:

    -   The **is\_parcelado** column has been removed from the dispute intake table.
    -   The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.

