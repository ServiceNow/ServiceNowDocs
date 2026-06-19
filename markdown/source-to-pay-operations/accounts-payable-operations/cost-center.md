---
title: Cost center
description: Cost centers are a commonly used reference between financial systems and IT. Cost center records represent business entities and have a related list of CI Cost Center Relationships that measure the cost center's consumption of business services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/cost-center.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data required for invoice processing, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Cost center

Cost centers are a commonly used reference between financial systems and IT. Cost center records represent business entities and have a related list of CI Cost Center Relationships that measure the cost center's consumption of business services.

For more information on cost centers and how it is referenced within financial systems, see .

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

**Parent Topic:**[Data required for invoice processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.md)

