---
title: Source-to-Pay integration framework
description: As part of the Source-to-Pay \(S2P\) integration framework, customers can install an optional third-party ERP integration application that enables primary data, fixed assets, purchase order, receipt, invoice, and tax integration capabilities between S2P and the third-party ERP application.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay integration framework

As part of the Source-to-Pay \(S2P\) integration framework, customers can install an optional third-party ERP integration application that enables primary data, fixed assets, purchase order, receipt, invoice, and tax integration capabilities between S2P and the third-party ERP application.

Primary data entities include:

-   Supplier
-   Profit center
-   Cost center
-   Ledger accounts
-   Purchase organizations
-   Asset category
-   Material mapping
-   Unit of measure

While the third-party application is the system of record for primary data, S2P is the system of record for purchase orders and receipts. Invoices are either created manually in S2P or through an external supplier portal \(for example, Ariba\). For tax calculation and integration, see [Tax calculations](../../sourcing-procurement-operations/reference/tax-calculations.md).

The integration between S2P and the third-party application requires settings on both sides so that these applications function properly together.

-   [Integration settings on Source-to-Pay side](integration-settings-psm-side.md)
-   Integration setting on the third-party side.

## Applications required for third-party integration

The integration requires the Finance – ERP Integration store application.

## Permissions and roles for third-party integration

The following ServiceNow roles are required for integration:

-   System administrator \(admin\) for installation of the integration application.
-   Procurement Specialist \(sn\_shop.procurement\_specialist\) for defining the ERP source.
-   FCA Integration user \(sn\_fcms\_intg.integration\_user\) for ERP source configurations such as web service authorization, web services for Park and Post, Reverse, and User and Role mapping.

    Add the following roles to the FCA Integration user:

    -   Import\_transformer
    -   Soap

## MID Server required for third-party integration

This integration requires an installed and configured MID Server in your ServiceNow instance to connect to the ERP system server. See [Installing the MID Server](https://www.servicenow.com/docs/access?context=mid-server-installation&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for details.

**Note:** The MID Server integration is required only for an ERP integration using SOAP services.

