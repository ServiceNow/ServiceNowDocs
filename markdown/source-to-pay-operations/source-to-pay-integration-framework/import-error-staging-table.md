---
title: Import error staging table
description: The Import error \[sn\_spend\_intg\_import\_error\] staging table temporarily stores important data on errors before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/source-to-pay-integration-framework/import-error-staging-table.html
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables for Accounts Payable Operations, Inbound staging tables Source-to-Pay Operations, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Import error staging table

The Import error \[sn\_spend\_intg\_import\_error\] staging table temporarily stores important data on errors before this data is sent to the primary table.

|Field|Data type|Description|
|-----|---------|-----------|
|Error message|String|A message that describes the error encountered.|
|Outbound status|Reference|Indicates the status of outgoing transactions.|

**Parent Topic:**[Inbound staging tables for Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/source-to-pay-integration-framework/inbound-staging-tables-for-apo.md)

**Related topics**  


[Invoice import inbound staging table]()

[Invoice line import inbound staging table]()

[Invoice payment detail import inbound table]()

[Organization tax details inbound staging table]()

[Invoice tax line staging table]()

