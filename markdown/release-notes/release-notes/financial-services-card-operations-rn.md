---
title: Financial Services Card Operations release notes
description: The ServiceNow Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Financial Services Card Operations release notes

The ServiceNow® Financial Services Card Operations application supports dispute agents by providing the necessary data to expedite dispute resolutions and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Yokohama release.

## Financial Services Card Operations highlights for the Yokohama release

-   Resolve friendly fraud disputes by incorporating friendly fraud detection and resolution in the existing dispute flow for Visa transactions. You can take actions such as crediting the customer, denying the dispute, or initiating an exception process.
-   The Financial Services Card Operations data model is updated in this release with reparented tables to align the data and manage the dispute transactions more effectively. See [Financial Services Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US) for more information.
-   Enhance the card disputes process with an updated end-to-end Visa disputes playbook that now includes support for reviewing associated transactions and handling pre-arbitration, arbitration, and appeals.
-   Manage and work on multiple disputed transactions for a case with individual playbooks for each disputed transaction.
-   Integrate new VROL subflows into the enhanced Visa card disputes playbook.

**Important:** Financial Services Card Operations is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Financial Services Card Operations to Yokohama

During the upgrade to Yokohama, the Financial Services Card Operations plugin reparents the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] to the Financial Task table \[sn\_bom\_task\] in Financial Services Operations Core.

Reparenting leverages the benefits and advancements of ServiceNow® Financial Services Operations Core while preserving the functionality of existing applications.

**Note:** If your instance uses the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] and it contains a large amount of data, you may experience increased upgrade times.

## New in the Yokohama release

-   **[Detect friendly fraud](https://www.servicenow.com/docs/access?context=resolve-friendly-fraud&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

    Resolve friendly fraud disputes with predefined rules to ensure consistent and precise detection of friendly fraud in Visa disputed transactions. Agents can decline requests, issue credits, or proceed with chargebacks, allowing for tailored responses based on the situation.

-   **[Enhanced Visa disputes playbook](https://www.servicenow.com/docs/access?context=managing-card-disputes&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

    Leverage an updated card disputes processing flow to associate additional transactions, manage multiple transaction disputes, and handle pre-arbitration, arbitration, and appeal requests to Visa for allocation and collaboration chargeback workflows.


## Changed in this release

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=card-operations-reference&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

    Updated the following columns to align with release 25.1 revision changes:

    -   The **is\_parcelado** column has been removed from the dispute intake table.
    -   The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.

## Activation information

Install Financial Services Card Operations by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Financial Services Operations Core](https://www.servicenow.com/docs/access?context=financial-services-operations-core-data-model&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

    Enables the extension of tables from Financial Services Operations Core to the Financial Services Card Operations application.

-   **[Dispute Rules Content Pack for Visa](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)**

    Run chargeback eligibility rules and determine the reason code for a dispute as part of the Visa disputes playbook.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

