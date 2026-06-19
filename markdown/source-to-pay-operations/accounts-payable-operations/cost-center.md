---
title: Cost center
description: Field descriptions for the Cost Center \[cmn\_cost\_center\] table used to create and manage cost center records that link financial systems to IT services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/cost-center.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice automation, AP automation, finance automation]
breadcrumb: [Data required for invoice processing, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Cost center

Field descriptions for the Cost Center \[cmn\_cost\_center\] table used to create and manage cost center records that link financial systems to IT services.

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

**Parent Topic:**[Data required for invoice processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.md)

