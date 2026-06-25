---
title: Invoice line stage table
description: The invoice line stage \[sn\_ap\_ic\_invoice\_line\_stage\] table stores line-level invoice data extracted by Document Intelligence.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/invoice-line-staging-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Accounts Payable Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Invoice line stage table

The invoice line stage \[sn\_ap\_ic\_invoice\_line\_stage\] table stores line-level invoice data extracted by Document Intelligence.

## Invoice line inbound stage table

The following table lists the fields for the invoice line \[sn\_ap\_ic\_invoice\_line\_stage\] stage table.

|Field|Data type|Description|
|-----|---------|-----------|
|Number|string|Auto-generated identifier for the line staging record.|
|Line description|string|Item or service description extracted from the invoice line.|
|Line quantity|string|Quantity billed on this line.|
|Line unit price|string|Unit price per item on this line.|
|Line amount \(transaction currency\)|string|Total line amount, calculated as quantity multiplied by unit price.|
|Tax amount|string|Tax amount applied to this line.|
|Invoice stage|reference|Reference to the parent invoice stage record \(`sn_ap_ic_invoice_stage`\).|
|Related invoice line|reference|Reference to the invoice line record created from this staging record.|

**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table]()

[Import error staging table]()

[Invoice line import inbound staging table]()

[Invoice payment detail import inbound table]()

[Organization tax details inbound staging table]()

[Invoice tax line staging table]()

[Invoice staging table]()

