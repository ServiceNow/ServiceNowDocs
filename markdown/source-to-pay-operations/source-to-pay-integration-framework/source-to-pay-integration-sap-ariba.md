---
title: Source-to-Pay integration with SAP Ariba
description: The Source-to-Pay integration with SAP Ariba enables you to handle sales orders, procurement, finance, and so on, in SAP Ariba from your ServiceNow instance.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay integration with SAP Ariba

The Source-to-Pay integration with SAP Ariba enables you to handle sales orders, procurement, finance, and so on, in SAP Ariba from your ServiceNow instance.

## Key features

With this application, you can perform the following:

-   Integration hub actions for invoices, cost centers, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, and legal entities.
-   Create goods receipts in SAP Ariba.

## Prerequisites

-   Activate the Source-to-Pay integration with the SAP Ariba application from the ServiceNow Store. This automatically activates the SAP Ariba Spoke.
-   Set up [SAP Ariba Spoke](https://www.servicenow.com/docs/bundle/yokohama-integrate-applications/page/administer/integrationhub-store-spokes/concept/sap-ariba-spoke.html).

![Overview of Source-to-Pay integration with SAP Ariba](../../source-to-pay-operations/image/sap-ariba-overview.png "Overview of the Source-to-Pay integration with SAP Ariba")

ServiceNow Store app plugins: sn\_sap\_ariba\_spoke.

**Note:** The Source-to-Pay integration with SAP Ariba depends on the [SAP Ariba Spoke](https://www.servicenow.com/docs/bundle/yokohama-integrate-applications/page/administer/integrationhub-store-spokes/concept/sap-ariba-spoke.html).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## How it works

The subflows enable a plug-and-play experience for the integration scenarios. Integration Hub Actions provide the building blocks for Source-to-Pay subflows and connects to the SAP Ariba system through REST APIs.

