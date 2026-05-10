---
title: Source-to-Pay Operations Integrations release notes
description: he ServiceNow Source-to-Pay Operations extends its capabilities by integrating with third-party applications. The Source-to-Pay Operations integration with SAP, Oracle EBS, Coupa, SAP Ariba, and Oracle Financial Cloud are new applications in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Source-to-Pay Operations Integrations release notes

he ServiceNow® Source-to-Pay Operations extends its capabilities by integrating with third-party applications. The Source-to-Pay Operations integration with SAP, Oracle EBS, Coupa, SAP Ariba, and Oracle Financial Cloud are new applications in the Australia release.

## Source-to-Pay Operations Integrations highlights for the Australia release

-   Handle sales orders, procurement, finance, and so on, in Oracle Financial Cloud from your ServiceNow instance using the Source-to-Pay integration with Oracle Financial Cloud.
-   Added enhancements to the Purchase Requisition Line \(PRL\) outbound staging table.
-   Performance optimizations applied to the Purchase Order \(PO\) transform map.

See [Source-to-Pay integration with third-party applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-third-party-integration.md) for more information.

**Important:** Source-to-Pay Operations Integrations with third-party apps is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Source-to-Pay Operations Integration with third-party apps to Australia

**Important:** Due to a performance issue identified with the upgrade fix script, the sourcing fix script has been modified. This script will no longer execute automatically during the upgrade process. Instead, it is now delivered as an on-demand job. Administrators must manually execute this job outside of business hours after the upgrade is complete.

## New in the Australia release

-   **[Source-to-Pay integration with Oracle Financial Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-oracle-fin-cloud-integration.md)**
    -   You can use this integration to perform Integration Hub actions for invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.
    -   You can also fetch currencies, GL accounts, legal entities, and payment terms information from Oracle Financial Cloud.

## Changed in this release

-   **[Source-to-Pay integration with SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-sap-integration.md)**
    -   Enhanced integration to support data retrieval from SAP ECC, SAP OData, and SAP HANA RFC using the updated Buyer Group staging process.
    -   Enhanced integration to support Read-Only security directives to strengthen data protection, applying required field-level changes in alignment with the Read-only field remediation guidelines to ensure compliance and consistency across integrations.
    -   Updated entity naming convention from Department to Buyer Groups for improved standardization.
-   **[Source-to-Pay integration with SAP Ariba](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integration-sap-ariba.md)**
    -   Enhanced integration to support fetch shipment details from SAP Ariba.
    -   Updated entity naming convention from Department to Buyer Groups for improved standardization.
-   **[Source-to-Pay integration framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integration-framework.md)**
    -   Enhanced the Purchase Requisition Line \(PRL\) outbound staging table to improve data completeness and consistency for outbound Purchase Requisition integrations.
    -   Performance optimizations have been applied to the Purchase Order \(PO\) transform map to improve efficiency and scalability when processing high‑volume PO data.

## Related ServiceNow applications and features

-   **[Integrate Sourcing and Procurement Operations with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/integrating-spo.md)**

    Extend the capabilities of Sourcing and Procurement Operations and connect with other departments by integrating with other applications.

-   **[Integrate Supplier Lifecycle Operations with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/integrate-slo.md)**

    Extend the capabilities of Supplier Lifecycle Operations by integrating with other applications.

-   ****

    Extend the capabilities of APO by integrating with other applications.


**Parent Topic:**[Source-to-Pay Operations release notes](source-to-pay-operations-rn-landing.md)

