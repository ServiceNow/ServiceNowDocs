---
title: Organization tax details
description: Accounts Payable specialist uses the organization tax table to view the supplier's tax registration details.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Master data table for Accounts Payable Operations, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Organization tax details

Accounts Payable specialist uses the organization tax table to view the supplier's tax registration details.

## Organization tax table

The organization table `sn_fin_org_tax_detail` stores supplier or organization tax details.

|Field|Data type|Description|
|-----|---------|-----------|
|Organization|Reference|The supplier or organization name.|
|Country of registration|Reference|Name of the country where the supplier or organization details are registered.|
|State/Province|String|Name of the state or province where the supplier or organization details are registered.|
|Tax ID|String/Numeric|Unique reference ID issued against an organization or supplier|
|Active|Boolean|The status of the tax registration of the organization or supplier.|

**Parent Topic:**[Master data table for Accounts Payable Operations](master-data-table-apo.md)

