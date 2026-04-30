---
title: Source-to-Pay integration with Oracle EBS
description: The Source-to-Pay integration with Oracle EBS enables you to handle sales orders, procurement, finance, and so on, in Oracle EBS from your ServiceNow instance.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay integration with Oracle EBS

The Source-to-Pay integration with Oracle EBS enables you to handle sales orders, procurement, finance, and so on, in Oracle EBS from your ServiceNow instance.

## Key features

With this application, you can perform the following:

-   Integration hub actions for invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.
-   Create or update purchase orders in Oracle EBS.
-   Cancel purchase orders in Oracle EBS.
-   Create good receipts in Oracle EBS.
-   Create invoices in Oracle EBS.

![Overview of the Source-to-Pay integration with Oracle EBS](../image/oracle-ebs-integration-overview.png "Overview of the Source-to-Pay integration with Oracle EBS")

## Prerequisites

First, you must activate the Source-to-Pay integration with the Oracle EBS application from the ServiceNow Store. This automatically activates the Oracle EBS Spoke. Next you must set up [Oracle EBS Spoke](https://www.servicenow.com/docs/csh?topicname=setup-oebs-spoke&version=yokohama&pubname=yokohama-integrate-applications).

ServiceNow Store app plugins: sn\_Oracle EBS\_spoke.

**Note:** The Source-to-Pay integration with Oracle EBS depends on the [Oracle EBS Spoke](https://www.servicenow.com/docs/csh?topicname=oebs-spoke&version=yokohama&pubname=yokohama-integrate-applications).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## How it works

The subflows enable a plug-and-play experience for the integration scenarios. Integration Hub Actions provide the building blocks for Source-to-Pay subflows and connects to the Oracle EBS system through REST APIs.

