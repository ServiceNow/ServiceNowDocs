---
title: Combined Source-to-Pay Operations Integrations release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Source-to-Pay Operations Integrations from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-sourcetopayoperationsintegrations-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Source-to-Pay Operations Integrations release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Source-to-Pay Operations Integrations from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Source-to-Pay Operations Integrations release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Source-to-Pay Operations Integrations to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

**Important:** Due to a performance issue identified with the upgrade fix script, the sourcing fix script has been modified. This script will no longer execute automatically during the upgrade process. Instead, it is now delivered as an on-demand job. Administrators must manually execute this job outside of business hours after the upgrade is complete.

</td></tr><tr><td>

Australia

</td><td>

**Important:** Due to a performance issue identified with the upgrade fix script, the sourcing fix script has been modified. This script will no longer execute automatically during the upgrade process. Instead, it is now delivered as an on-demand job. Administrators must manually execute this job outside of business hours after the upgrade is complete.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Source-to-Pay Operations Integrations.

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

-   **[Source-to-Pay integration with SAP](https://www.servicenow.com/docs/access?context=source-to-pay-sap-integration&family=zurich&ft:locale=en-US)**
    -   You can use this integration to perform Integration Hub actions for purchase requisition, purchase order, receipt, and invoices.
    -   You can also perform the following:
        -   Create, update, or cancel purchase orders in SAP ECC and SAP S4 HANA.
        -   Create good receipts in SAP ECC and SAP S4 HANA.
        -   Create invoices in SAP ECC and SAP S4 HANA.
-   **[Source-to-Pay integration with Oracle EBS](https://www.servicenow.com/docs/access?context=source-to-pay-oracle-ebs-integration&family=zurich&ft:locale=en-US)**
    -   You can use this integration to perform Integration Hub actions for Invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.
    -   You can also perform the following:
        -   Create, update, or cancel purchase orders in Oracle EBS.
        -   Create good receipts in Oracle EBS.
        -   Create invoices in Oracle EBS.
-   **[Source-to-Pay integration with Coupa](https://www.servicenow.com/docs/access?context=source-to-pay-coupa-integration&family=zurich&ft:locale=en-US)**

You can use this integration to perform Integration Hub actions for loading primary data, supplier management, purchase requisition, purchase order, receipt, invoice, and sourcing. You can also look up Legal Entity, Currency, and Supply details respectively.

-   **[Source-to-Pay integration with SAP Ariba](https://www.servicenow.com/docs/access?context=source-to-pay-integration-sap-ariba&family=zurich&ft:locale=en-US)**

You can use this integration to perform Integration Hub actions for invoices, cost centers, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, and legal entities. You can also create good receipts in SAP Ariba.


</td></tr><tr><td>

Australia

</td><td>

-   **[Source-to-Pay integration with Oracle Financial Cloud](https://www.servicenow.com/docs/access?context=source-to-pay-oracle-fin-cloud-integration&family=australia&ft:locale=en-US)**
    -   You can use this integration to perform Integration Hub actions for invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.
    -   You can also fetch currencies, GL accounts, legal entities, and payment terms information from Oracle Financial Cloud.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Source-to-Pay Operations Integrations features.

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

-   **[Source-to-Pay integration with SAP](https://www.servicenow.com/docs/access?context=source-to-pay-sap-integration&family=australia&ft:locale=en-US)**
    -   Enhanced integration to support data retrieval from SAP ECC, SAP OData, and SAP HANA RFC using the updated Buyer Group staging process.
    -   Enhanced integration to support Read-Only security directives to strengthen data protection, applying required field-level changes in alignment with the Read-only field remediation guidelines to ensure compliance and consistency across integrations.
    -   Updated entity naming convention from Department to Buyer Groups for improved standardization.
-   **[Source-to-Pay integration with SAP Ariba](https://www.servicenow.com/docs/access?context=source-to-pay-integration-sap-ariba&family=australia&ft:locale=en-US)**
    -   Enhanced integration to support fetch shipment details from SAP Ariba.
    -   Updated entity naming convention from Department to Buyer Groups for improved standardization.
-   **[Source-to-Pay integration framework](https://www.servicenow.com/docs/access?context=source-to-pay-integration-framework&family=australia&ft:locale=en-US)**
    -   Enhanced the Purchase Requisition Line \(PRL\) outbound staging table to improve data completeness and consistency for outbound Purchase Requisition integrations.
    -   Performance optimizations have been applied to the Purchase Order \(PO\) transform map to improve efficiency and scalability when processing high‑volume PO data.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Source-to-Pay Operations Integrations features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Source-to-Pay Operations Integrations features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Source-to-Pay Operations Integrations.

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

Install Source-to-Pay Operations with third-party applications by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Source-to-Pay Operations Integrations we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Source-to-Pay Operations Integrations we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Source-to-Pay Operations Integrations, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Source-to-Pay Operations Integrations we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Source-to-Pay Operations Integrations we have noted them here.

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

-   Send purchase orders, receipts, and invoices created in SAP ECC and SAP S4 HANA from your ServiceNow instance using the Source-to-Pay integration with SAP ECC and S4 HANA.
-   Handle sales orders, procurement, finance, and so on, in Oracle EBS from your ServiceNow instance using the Source-to-Pay integration with Oracle EBS.
-   Handle business spends and automate approvals, contracts, inventory, purchase orders, requisitions, suppliers, and user management in Coupa from your ServiceNow instance using the Source-to-Pay integration with Coupa.
-   Handle sales orders, procurement, finance, and so on, in SAP Ariba from your ServiceNow instance using the Source-to-Pay integration with SAP Ariba.

 See [Integration with third-party applications](https://www.servicenow.com/docs/access?context=source-to-pay-third-party-integration&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Handle sales orders, procurement, finance, and so on, in Oracle Financial Cloud from your ServiceNow instance using the Source-to-Pay integration with Oracle Financial Cloud.
-   Added enhancements to the Purchase Requisition Line \(PRL\) outbound staging table.
-   Performance optimizations applied to the Purchase Order \(PO\) transform map.

 See [Integration with third-party applications](https://www.servicenow.com/docs/access?context=source-to-pay-third-party-integration&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

