---
title: Outbound cost allocation staging table
description: The outbound cost allocation \[sn\_spend\_intg\_outbound\_invoice\_cost\_allocation\] staging table stores important data about cost allocation information so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/outbound-cost-allocation-table.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Outbound cost allocation staging table

The outbound cost allocation \[sn\_spend\_intg\_outbound\_invoice\_cost\_allocation\] staging table stores important data about cost allocation information so that an ERP integrator can export this data to a third-party ERP system.

## Outbound cost allocation staging table

The following table lists fields for the outbound cost allocation \[sn\_spend\_intg\_outbound\_invoice\_cost\_allocation\] staging table.

|Field|Data type|Description|
|-----|---------|-----------|
|Number|String|An auto-generated number that uniquely identifies the invoice.|
|Allocation type|Choice|The cost allocation type that you would like to assign cost to.|
|Cost center|Reference|Cost center for which the invoice is generated.|
|Ledger account|Reference|A reference field for the account used to generate the  invoice.​|
|Allocate by|String|Determines whether the cost allocation is based on amount or percentage.|
|Allocation amount|String|Amount that is allocated.|
|Invoice line|Reference|Line items on the invoice.|
|Integration status|Choice|Status of the integration process.|

**Parent Topic:**[Accounts Payable Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties]()

[Create New Invoice Line form]()

[Create invoice cost allocation form]()

[Distribution set form]()

[Create New Invoice case form]()

[Create New Invoice task form]()

[Invoice processing case form]()

[Tax lines]()

[Invoice exception form]()

[Request Help form]()

[Data required for invoice processing]()

[Invoice exception definition form]()

[Approval Rule form]()

[Approval Plan form]()

