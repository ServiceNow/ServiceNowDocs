---
title: Invoice exception definition form
description: Field descriptions for the Invoice exception definition form used to create and configure invoice exception definitions in Accounts Payable Invoice Processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-exception-definition-form.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [APO, Accounts Payable Operations, invoice automation, AP automation, invoice exception]
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice exception definition form

Field descriptions for the Invoice exception definition form used to create and configure invoice exception definitions in Accounts Payable Invoice Processing.

<table id="table_acw_lsh_ywb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the invoice exception definition.

</td></tr><tr><td>

Application

</td><td>

Application scope to create the invoice exception definition in. For example, Accounts Payable Invoice Processing.

</td></tr><tr><td>

Active

</td><td>

Option to activate the invoice exception definition for use.

</td></tr><tr><td>

Order

</td><td>

The order in which you want the invoice exception to be identified. Specify a numeric value in multiples of 100.

</td></tr><tr><td>

Line level exception

</td><td>

Option to mark the invoice exception definition as a line-level exception.

</td></tr><tr><td>

View

</td><td>

View that is used to display the fields in an exception record.

</td></tr><tr><td>

Allow bypass

</td><td>

Option to allow bypass of the invoice exception definition.

</td></tr><tr><td>

Dependent

</td><td>

The Invoice exception definition on which the new invoice exception definition depends on.For example, if an exception definition record A is dependent on an exception definition record B, then when an invoice has an exception of type exception definition B in open state, then the exception engine does not check the invoice for exception definition A. Instead, the exception engine identifies only the exception definition B.

The dependent invoice exception definition record must have a lower order value than the new invoice exception definition record that you are creating.

</td></tr><tr><td>

Applicable to

</td><td>

Type of invoice that the invoice exception definition is applicable to. For example, PO Invoice.

</td></tr><tr><td>

Subflow

</td><td>

Subflow that is run to determine if the exception exists for a given invoice.

</td></tr></tbody>
</table>**Parent Topic:**[Accounts Payable Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties]()

[Create New Invoice Line form]()

[Create invoice cost allocation form]()

[Outbound cost allocation staging table]()

[Distribution set form]()

[Create New Invoice case form]()

[Create New Invoice task form]()

[Invoice processing case form]()

[Tax lines]()

[Invoice exception form]()

[Request Help form]()

[Data required for invoice processing]()

[Approval Rule form]()

[Approval Plan form]()

[Accounts Payable Operations glossary]()

