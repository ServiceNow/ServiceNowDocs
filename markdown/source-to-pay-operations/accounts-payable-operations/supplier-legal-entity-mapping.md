---
title: Supplier Legal Entity Mapping
description: The linking of supplier registered legal entity to the customer's corresponding legal entity within APO is referred as Supplier legal entity mapping. Mapping ensures that invoices, purchase orders, and payments are correctly routed, validated, and processed across systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/supplier-legal-entity-mapping.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data required for invoice processing, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Supplier Legal Entity Mapping

The linking of supplier registered legal entity to the customer's corresponding legal entity within APO is referred as Supplier legal entity mapping. Mapping ensures that invoices, purchase orders, and payments are correctly routed, validated, and processed across systems.

## Supplier Legal Entity Mapping table

|Field|Data type|Description|
|-----|---------|-----------|
|Supplier|Reference|Name of the supplier.|
|Legal entity|Reference|Legal entity of the customer.|
|Payment term|Reference|The name or code of the payment term. Example: Net 60.|
|General ledger account|Reference|The account to which capital or operational expenses will be posted.|

**Parent Topic:**[Data required for invoice processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.md)

