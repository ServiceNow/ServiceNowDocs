---
title: Configuration tables and prerequisites for Tax integration
description: Use the configuration tables to enable tax integration with third-party tax engines.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tax Engine Integration, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Configuration tables and prerequisites for Tax integration

Use the configuration tables to enable tax integration with third-party tax engines.

Configure the following mentioned tables for tax integration with a third-party tax engine.

|Configuration table|Description|
|-------------------|-----------|
|S2P Custom Configurations \[sn\_fin\_s2p\_custom\_config\]|Set condition for tax integration for incoming invoices.|
|S2P Custom Configuration Type \[sn\_fin\_s2p\_custom\_config\_type\]|Set condition for configuring type of responses from tax engine.|
|ERP sources \[sn\_fin\_erp\_source\]|Review ERP source for tax engine.|
|Tax type \[sn\_fin\_tax\_type\]|Match the tax type returned by the external tax engine and associate them with the appropriate ERP source.|
|Tax integration field mappings \[sn\_spend\_intg\_tax\_field\_map\]|Review the mapping between APO field and external tax engine field|
|Tax attributes for recalculation|Specify the invoice data attributes that must be present to create taxes in the [Accounts Payable Operations properties](../reference/acc-pay-properties.md).|

## Prerequisites for Third-party Tax integration

To enable third‑party tax integration, customers must include the following:

The required plugins for third-party tax integration are:

-   app-accounts-payable
-   app-spend-workspace
-   app-spend-catalog
-   app-spend-integrations
-   app-tax-integration-vertex \(if vertex is used as the tax engine\)

-   Configure connection and credential details for the external tax engine.
-   Configure tax management properties and mapping rules.

For configuring tax management properties, see [Accounts Payable Operations properties](../reference/acc-pay-properties.md).

