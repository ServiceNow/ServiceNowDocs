---
title: Tax status
description: The tax status field in the invoice record is used to track the current status of tax validation processing throughout the tax integration workflow.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tax lines, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Tax status

The tax status field in the invoice record is used to track the current status of tax validation processing throughout the tax integration workflow.

## Invoice tax status fields

The following table displays the tax status \[tax\_status\] fields in the invoice record \[sn\_shop\_invoice\]:

|Field|Description|
|-----|-----------|
|Invoice table|
|In progress|Tax calculation request sent to third party tax engine and awaiting response.|
|Failed|Tax calculation failed due to tax engine integration failure.|
|Success|Tax calculation completed and tax lines created successfully.|
|Integration error|Tax engine connectivity or communication failure occurred.|
|Recalculate tax|Invoice header or invoice line needs field changes, invoice tax status changes to recalculate tax. The invoice is sent for tax revalidation manually or through scheduler.|

For more information on using tax status, see [Tax Engine Integration](../concept/tax-engine-integration.md).

**Parent Topic:**[Tax lines](create-tax-lines-apo.md)

