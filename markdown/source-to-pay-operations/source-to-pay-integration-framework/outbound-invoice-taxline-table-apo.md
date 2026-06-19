---
title: Outbound invoice tax line staging table
description: Field descriptions and data types for the Outbound invoice tax line \[sn\_spend\_intg\_outbound\_invoice\_tax\_line\] staging table used to export invoice tax line data to third-party ERP systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/outbound-invoice-taxline-table-apo.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, ERP integration, staging table, outbound integration, tax]
breadcrumb: [Outbound staging tables for Accounts Payable Operations, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Outbound invoice tax line staging table

Field descriptions and data types for the Outbound invoice tax line \[sn\_spend\_intg\_outbound\_invoice\_tax\_line\] staging table used to export invoice tax line data to third-party ERP systems.

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

