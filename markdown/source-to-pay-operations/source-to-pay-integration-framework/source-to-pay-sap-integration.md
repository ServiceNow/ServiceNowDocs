---
title: Source-to-Pay integration with SAP
description: The Source-to-Pay integration with SAP enables you to send purchase orders, receipts, and invoices created on the SAP from your ServiceNow instance. This integration helps in looking up or extracting primary data objects from SAP into ServiceNow.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay integration with SAP

The Source-to-Pay integration with SAP enables you to send purchase orders, receipts, and invoices created on the SAP from your ServiceNow instance. This integration helps in looking up or extracting primary data objects from SAP into ServiceNow.

## Key features

With this application, you can perform the following:

-   Integration hub actions for purchase requisition, purchase order, receipt, and invoices.
-   Create or update purchase orders in SAP.
-   Cancel purchase orders in SAP.
-   Create good receipts in SAP.
-   Create invoices in SAP.

![Overview of the Source-to-Pay integration with SAP ECC and SAP S4 HANA Public Cloud and OData](../image/source-to-pay-integration-sap-overview.png "Overview of the Source-to-Pay integration with SAP")

## Prerequisites

First, you must activate the Source-to-Pay integration with the SAP application from the ServiceNow Store. This automatically activates the SAP ECC, SAP S4 Public, and SAP S4 HANA OData Spoke. Next you must set up the following SAP ECC or SAP S4 HANA based on your requirement:

-   [SAP ECC RFC Spoke](https://www.servicenow.com/docs/csh?topicname=sap-ecc-rfc-spoke&amp;amp;version=yokohama&amp;amp;pubname=yokohama-integrate-applications)
-   [SAP S4 HANA Public Cloud Spoke](https://www.servicenow.com/docs/csh?topicname=sap-s4-hana-cloud-spk&amp;amp;version=yokohama&amp;amp;pubname=yokohama-integrate-applications)
-   [SAP S4 HANA OData Spoke](https://www.servicenow.com/docs/csh?topicname=sap-s4-odata-spoke&amp;version=yokohama&amp;pubname=yokohama-integrate-applications)

The following are the ServiceNow Store app plugins:

-   sn\_sap\_ecc\_rfc\_spo.SAP\_ECC
-   sn\_s4\_hana\_cld\_spk.SAP\_S4\_HANA\_Cloud
-   sn\_hana\_odata\_spk.SAP\_S4\_HANA\_OData

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## How it works

The subflows enable a plug-and-play experience for the integration scenarios. Integration Hub Actions provide the building blocks for Source-to-Pay subflows and connects to the SAP system through REST APIs.

