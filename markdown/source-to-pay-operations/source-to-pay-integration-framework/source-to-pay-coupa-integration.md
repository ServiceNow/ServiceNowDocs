---
title: Source-to-Pay integration with Coupa
description: The Source-to-Pay integration with Coupa enables you to handle business spend and automate approvals, contracts, inventory, purchase orders, requisitions, suppliers, and user management in Coupa from your ServiceNow instance.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-01-29"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay integration with Coupa

The Source-to-Pay integration with Coupa enables you to handle business spend and automate approvals, contracts, inventory, purchase orders, requisitions, suppliers, and user management in Coupa from your ServiceNow instance.

## Key Features

With this application, you can perform the following:

-   Perform Integration hub actions for loading primary data, supplier management, PR, PO, receipt, invoice, and sourcing.
-   Look up Legal Entity details from Coupa to Source-to-Pay integration framework
-   Look up Currency details from Coupa to Source-to-Pay integration framework
-   Look up Supplier details from Coupa to Source-to-Pay integration framework

![Overview of Source-to-pay integration with Coupa](../image/coupa-integration-overview.png "Overview of the Source-to-Pay integration with Coupa")

## Prerequisites

Activate the Source-to-Pay integration with the Coupa application from the ServiceNow Store to activate the Coupa Spoke automatically. Next you must set up [Coupa Spoke](https://www.servicenow.com/docs/csh?topicname=setup-coupa-spoke-v4&version=yokohama&pubname=yokohama-integrate-applications).

ServiceNow Store app plugins: sn\_coupa\_spoke.

**Note:** The Source-to-Pay integration with Coupa depends on the [Coupa Spoke](https://www.servicenow.com/docs/csh?topicname=coupa-spoke&version=yokohama&pubname=zurich-integrate-applications).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## How it works

The subflows enable a plug-and-play experience for the integration scenarios. Integration Hub Actions provide the building blocks for Source-to-Pay subflows and connects to the Coupa system through REST APIs.

