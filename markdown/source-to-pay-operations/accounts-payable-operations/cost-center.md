---
title: Cost center
description: Cost centers are a commonly used reference between financial systems and IT. Cost center records represent business entities and have a related list of CI Cost Center Relationships that measure the cost center's consumption of business services.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Master data table for Accounts Payable Operations, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Cost center

Cost centers are a commonly used reference between financial systems and IT. Cost center records represent business entities and have a related list of CI Cost Center Relationships that measure the cost center's consumption of business services.

For more information on cost centers and how it is referenced within financial systems, see Cost Management.

## cmn\_cost center table

|Field|Data type|Description|
|-----|---------|-----------|
|Name|String|A unique name for the cost center.|
|Account Number|String|An account number associated with the cost center, if one exists.|
|Code|String|A code associated with the cost center, if one exists.|
|Location|Reference|A reference to the location of the cost center.|
|Valid from|Date/Time|The date that the cost center is valid from. The format is YYYY-MM-DD HH: MM: SS.|
|Valid to|Date/Time|The date that the cost center is valid to. The format is YYYY-MM-DD HH: MM: SS.|
|Manager|String|A reference to the user who manages the cost center.|
|Parent|String|A reference to the parent cost center in the hierarchical structure of cost centers.|

**Parent Topic:**[Master data table for Accounts Payable Operations](master-data-table-apo.md)

