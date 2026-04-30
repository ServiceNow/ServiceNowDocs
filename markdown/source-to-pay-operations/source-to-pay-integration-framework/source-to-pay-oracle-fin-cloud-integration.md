---
title: Source-to-Pay integration with Oracle Financial Cloud
description: The Source-to-Pay integration with Oracle Financial Cloud enables you to manage sales orders, procurement, finance, and so on, in Oracle Financial Cloud from your ServiceNow instance.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 1
breadcrumb: [Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay integration with Oracle Financial Cloud

The Source-to-Pay integration with Oracle Financial Cloud enables you to manage sales orders, procurement, finance, and so on, in Oracle Financial Cloud from your ServiceNow instance.

## Key features

With this application, you can perform the following:

-   Look up Currencies, General Ledger \(GL\) accounts, Legal entities, Payment terms details, Plant Address, Cost Center, Purchasing Orgs, and Purchasing Groups from Oracle Financial Cloud.
-   Create or update Supplier locations in Oracle Financial Cloud
-   Create or update Supplier payment details in Oracle Financial Cloud
-   Create, update, or deactivate Suppliers in Oracle Financial Cloud

![Overview of the Source-to-Pay integration with Oracle Financial Cloud](../image/oracle-fin-integration-overview.png "Overview of the Source-to-Pay integration with Oracle Financial Cloud")

## Prerequisites

First, you must activate the Source-to-Pay integration with the Oracle Financial Cloud application from the ServiceNow Store. This automatically activates the Oracle Financial Cloud Spoke. Next you must set up [Oracle Financial Cloud Spoke](https://www.servicenow.com/docs/csh?topicname=setup-oracle-fin-cloud&version=zurich&pubname=zurich-integrate-applications).

ServiceNow Store app plugins: sn\_Oracle Financial Cloud\_spoke.

**Note:** The Source-to-Pay integration with Oracle Financial Cloud depends on the [Oracle Financial Cloud Spoke](https://www.servicenow.com/docs/csh?topicname=oracle-fin-cloud&version=zurich&pubname=zurich-integrate-applications).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## How it works

The subflows enable a plug-and-play experience for the integration scenarios. Integration Hub Actions provide the building blocks for Source-to-Pay subflows and connects to the Oracle Financial Cloud system through REST APIs.

