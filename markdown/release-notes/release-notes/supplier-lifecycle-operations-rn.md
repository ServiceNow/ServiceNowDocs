---
title: Supplier Lifecycle Operations release notes
description: The ServiceNow Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Supplier Lifecycle Operations release notes

The ServiceNow® Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Xanadu release.

## Supplier Lifecycle Operations highlights for the Xanadu release

-   View the summarized details of supply-related records to keep the supplier managers and fulfillers informed about their progress and action items.
-   Manage supplier relationship and performance to optimize the value and quality of the products and services delivered by suppliers.
-   Exchange supplier data accurately with external ERP systems using additional fields in the inbound and outbound tables.
-   View supplier details such as supplier products, contracts, purchase orders, and invoices directly from the Source-to-Pay Workspace and the Supplier Collaboration Portal.
-   Support for many-to-many \(M2M\) mapping between supplier contact and suppliers: A single supplier contact can be the contact for multiple suppliers, if the suppliers share a parent-subsidiary relationship. M2M mapping between supplier contact and suppliers is available from the Xanadu December 2024 release onwards.

See [Supplier Lifecycle Operations](https://www.servicenow.com/docs/access?context=supp-mgmt-landing-page&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US) for more information.

**Note:**

You can experience a longer upgrade time if you’re upgrading from Vancouver or an older release to Washington DC or any latest release. This delay is due to a mandatory script that runs for restructuring the Supplier Task \[sn\_slm\_task\] table and the duration of upgrade depends on the number of records in this table.

**Important:** Supplier Lifecycle Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    With the Now Assist for Supplier Lifecycle Operations \(SLO\) application, supplier managers and fulfillers can summarize the details of supply-related records to keep them informed about their progress and action items.

-   **[Supplier Relationship and Performance Management](https://www.servicenow.com/docs/access?context=supplier-performance-management-overview&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**
    -   Manage supplier relationship and performance to optimize the value and quality of the products and services delivered by suppliers.
    -   Establish clear expectations and criteria for measuring supplier performance, monitor and assess their performance against those criteria, provide feedback and recognition, and implement corrective actions and improvement plans when needed.
-   **[Supplier Lifecycle Operations integration framework](https://www.servicenow.com/docs/access?context=slo-int-framework&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Exchange supplier data with any third-party ERP system using enhanced transform maps and inbound and outbound integration tables.

-   **[View supplier details in the Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=supp-ws-details-page&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**
    -   View supplier details such as contracts and supplier products in the Related Links section on the **About** tab of the Source-to-Pay Workspace supplier page.
    -   View supplier details such as purchase orders and invoices on the **Related work** tab of the Source-to-Pay Workspace supplier page.
-   **[View supplier details in the Supplier Collaboration Portal](https://www.servicenow.com/docs/access?context=supplier-central&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    View supplier details in the following tiles in the My active items widget:

    -   Contracts
    -   Supplier Products
    -   Purchase Orders
    -   Invoices
    **Note:** These new tiles are displayed if you have installed the Sourcing and Purchasing Automation \(com.snc.sn\_pr\) and Source-to-Pay Common Architecture \(com.snc.sn\_shop\) plugins.


## Deprecations

-   **[Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=supplier-manager-workspace&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

    Starting with the Washington DC release, Supplier Manager Workspace is being prepared for future deprecation. It will be hidden and no longer be activated on new instances but will continue to be supported. Source-to-Pay Workspace provides the latest experience for this functionality.


## Activation information

Install Supplier Lifecycle Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Source-to-Pay Operations release notes](source-to-pay-operations-rn-landing.md)

