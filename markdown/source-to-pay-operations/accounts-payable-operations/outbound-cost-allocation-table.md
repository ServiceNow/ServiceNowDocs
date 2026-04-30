---
title: Outbound cost allocation staging table
description: The outbound cost allocation \[sn\_spend\_intg\_outbound\_invoice\_cost\_allocation\] staging table stores important data about cost allocation information so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Accounts Payable Operations reference, Accounts Payable Operations, Finance and Supply Chain]
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

**Parent Topic:**[Accounts Payable Operations reference](acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties](acc-pay-properties.md)

[Create New Invoice Line form](create-invoice-line-form.md)

[Create invoice cost allocation form](create-invoice-cost-allocation-form.md)

[Distribution set form](distribution-set-form.md)

[Create New Invoice case form](create-new-ap-case-form.md)

[Create New Invoice task form](create-apm-task-form.md)

[Invoice processing case form](invoice-processing-case-form.md)

[Tax lines](create-tax-lines-apo.md)

[Invoice exception form](exception-form-fields.md)

[Request Help form](ur-request-help-form.md)

[Master data table for Accounts Payable Operations](master-data-table-apo.md)

[Invoice exception definition form](invoice-exception-definition-form.md)

[Approval Rule form](new-approval-rule-form.md)

[Approval Plan form](approval-plan-form.md)

[Accounts Payable Operations glossary](../concept/apo-glossary.md#)

