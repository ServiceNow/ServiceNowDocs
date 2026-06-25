---
title: Outbound cost allocation staging table
description: Field descriptions for the outbound cost allocation \[sn\_spend\_intg\_outbound\_invoice\_cost\_allocation\] staging table used to configure ERP integrations that export cost allocation data to third-party ERP systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/outbound-cost-allocation-table.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice management, cost allocation, GL coding, ERP integration, staging table, outbound integration]
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Outbound cost allocation staging table

Field descriptions for the outbound cost allocation \[sn\_spend\_intg\_outbound\_invoice\_cost\_allocation\] staging table used to configure ERP integrations that export cost allocation data to third-party ERP systems.

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

**Parent Topic:**[Accounts Payable Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/acc-pay-reference.md)

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

[Accounts Payable Operations glossary]()

