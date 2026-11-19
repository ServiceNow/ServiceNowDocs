---
title: Financial Services Operations Core release notes
description: The ServiceNow Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Australia release.Update processing\_code field choice values in the Financial transaction table to align with current Visa data field specifications.The ServiceNow Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Australia release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/financial-services-operations-core-rn.html
release: australia
topic_type: topic
last_updated: "2026-04-06"
reading_time_minutes: 3
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Financial Services Operations Core release notes

The ServiceNow® Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Australia release.

## About Financial Services Operations Core

The case type selector in Financial Services Operations now uses the predefined Customer Service Management \(CSM\) implementation, replacing the previous FSO-specific override.

See [Case type selector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-type-select-modals.md) for more information.

## Activation and other requirements

**Important:** Financial Services Operations Core is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Financial Services Operations Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/financial-services-operations-rn-landing.md)

## Version 12.6.0

Update **processing\_code** field choice values in the Financial transaction table to align with current Visa data field specifications.

### What's changed

-   **Processing code field values updated for Visa compliance**

    The `processing_code` field choice values in the Financial transaction table have been updated to align with current Visa data field specifications. Existing choice values have been updated with refined labels and descriptions; new choice values have been added to support additional transaction types.

    The updated choice values include:

    -   `00` — Goods/Service Purchase - Debit
    -   `01` — Cash Disbursement \(for example, withdrawal or cash advance\) - Debit
    -   `02` — Adjustment - Debit
    -   `10` — Account Funding or Card Absent Account Funding
    -   `11` — Quasi-Cash Transaction - Debit or Internet Gambling Transaction
    -   `19` — Fee Collection - Debit
    -   `20` — Return of Goods - Credit, Credit Transaction, Credit Voucher
    -   `22` — Adjustment - Credit
    -   `26` — Original Credit
    -   `28` — Activation and Load / Load
    -   `29` — Funds Disbursement - Credit
    -   `30` — Available Funds Inquiry
    -   `39` — Eligibility Inquiry
    -   `50` — Bill Payment \(U.S. only\)
    -   `53` — Payment \(U.S. only\)
    -   `72` — Activation \(POS\)
    Dispute agents and administrators see these updated labels and descriptions in transaction UI drop-down lists and data entry forms. Existing transactions require no action. Existing choice values not listed here remain unchanged.


## Australia

The ServiceNow® Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Australia release.

### What's changed

-   **[Case type selector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-type-select-modals.md)**

    Filter service definitions using the case type selector in FSO with the predefined CSM implementation. For upgraded instances, existing agent criteria and customer condition data is automatically migrated from the deprecated FSO tables to the CSM tables during upgrade. No manual migration is required.

    To configure agent criteria or customer conditions for the case type selector, use the following CSM tables:

    -   `sn_csm_case_types_service_user_criteria`: for agent criteria
    -   `sn_csm_case_types_service_customer_criteria`: for customer conditions

### What's deprecated or removed

-   The FSO tables `sn_bom_m2m_service_definition_user_criteria` and `sn_bom_m2m_service_definition_customer_condition` are deprecated. If you're on an upgraded instance, you can continue to reference these tables, but they're no longer maintained. Use `sn_csm_case_types_service_user_criteria` and `sn_csm_case_types_service_customer_criteria` instead. For more information, see [FSO Core Banking tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-core-banking-tables.md).
-   The **Show in Interceptor** field \(`show_in_interceptor`\) on the `sn_bom_service_definition` table is deprecated. Use agent criteria in the `sn_csm_case_types_service_user_criteria` table to control which service definitions appear in the case type selector.

    User criteria mappings control the visibility of new service definitions. To hide a service definition, map it to the **No User** user criteria. To make it visible, map it to the **Users with sn\_bom.service\_definition\_read** user criteria. Both user criteria records are predefined in Financial Services Operations Core.

    For more information, see [Components installed with case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/service-definitions-components.md).


