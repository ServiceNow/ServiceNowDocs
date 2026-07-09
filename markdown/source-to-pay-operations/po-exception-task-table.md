---
title: Purchase Order Exception Task table
description: Purchase order exception tasks are individual tasks assigned to users as part of resolving a purchase order exception.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/po-exception-task-table.html
release: australia
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Master data tables for Purchase Order Management, Reference, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Order Exception Task table

Purchase order exception tasks are individual tasks assigned to users as part of resolving a purchase order exception.

## sn\_poem\_exception\_task table

The Purchase Order Exception Task \(sn\_poem\_exception\_task\) table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Supplier|Reference|Supplier associated with the purchase order exception.|
|Supplier location|Reference|Specific location or site of the supplier relevant to this task.|
|Purchase order line|Reference|Line item on the purchase order associated with this task.|
|Sub type|String|Category of the exception task.|
|Related case|Reference|Exception case associated with this task.|
|Purchase order|Reference|Purchase order related to this exception task.|
|Primary contact|Reference|Main point of contact for resolving this exception on the buyer side.|

**Parent Topic:**[Master data tables for Purchase Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/master-data-tables-for-pom.md)

**Related topics**  


[View a purchase order exception task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/view-po-exception-task.md)

[Create and assign a purchase order exception task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/assign-a-poe-task-to-a-collaborator.md)

[Work on a purchase order exception task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/work-on-a-purchase-order-exception.md)

