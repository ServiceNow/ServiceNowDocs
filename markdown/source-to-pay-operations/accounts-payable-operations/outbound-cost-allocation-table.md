---
title: Outbound cost allocation staging table
description: The outbound cost allocation \[sn\_spend\_intg\_outbound\_invoice\_cost\_allocation\] staging table stores important data about cost allocation information so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2024-10-17"
reading_time_minutes: 1
breadcrumb: [Create New Invoice Line form, Accounts Payable Operations reference, Accounts Payable Operations, Finance and Supply Chain]
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

**Parent Topic:**[Create New Invoice Line form](create-invoice-line-form.md)

