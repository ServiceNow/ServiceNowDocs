---
title: Outbound invoice tax line staging table
description: The Outbound invoice tax line \[sn\_spend\_intg\_outbound\_invoice\_tax\_line\] staging table stores important invoice line data so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables for Accounts Payable Operations, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Outbound invoice tax line staging table

The Outbound invoice tax line \[sn\_spend\_intg\_outbound\_invoice\_tax\_line\] staging table stores important invoice line data so that an ERP integrator can export this data to a third-party ERP system.

## Outbound invoice tax line staging table

The following table lists both the mandatory and optional fields for the outbound invoice tax line \[sn\_spend\_intg\_outbound\_invoice\_tax\_line\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Final tax|String|Final tax amount paid for this invoice.|
|Integration status|String|Current status of the outbound invoice tax line integration process.|
|Invoice|Reference|Invoice for which this tax is applicable.|
|Invoice line|Reference|Invoice line for which the tax is applicable.|
|Number|String|A unique system-generated number, which identifies the tax line.|
|Processing message|String|A message that describes the current processing status.|
|Supplier tax|String|Amount of tax charged by the supplier.|
|Supplier tax rate|String|Tax rate charged by the supplier.|
|Tax type|Reference|Type of the tax applicable on the invoice.|
|Taxable amount|String|Amount of tax applicable on an invoice.|

