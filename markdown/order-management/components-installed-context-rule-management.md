---
title: Components installed with Context Rule Management
description: Several types of components are installed with activation of the Context Rule Management \(sn\_csm\_ctxrul\_mgt\) plugin, including tables and user roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/components-installed-context-rule-management.html
release: australia
topic_type: reference
last_updated: "2026-11-05"
reading_time_minutes: 1
breadcrumb: [Pricing Management reference, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Components installed with Context Rule Management

Several types of components are installed with activation of the Context Rule Management \(sn\_csm\_ctxrul\_mgt\) plugin, including tables and user roles.

## Roles installed

<table id="table_ctx_roles_inst"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Context rule administrator

 \[sn\_csm\_ctxrul\_mgt.context\_rule\_administrator\]

</td><td>

Grants create, update, and delete access to matrix validations, validation definitions, rule matrices, and context variables.

</td><td>

-   sn\_csm\_ctxrul\_mgt.rule\_matrix\_writer
-   sn\_csm\_ctxrul\_mgt.context\_variable\_viewer

</td></tr><tr><td>

Rule matrix writer

 \[sn\_csm\_ctxrul\_mgt.rule\_matrix\_writer\]

</td><td>

Grants read and create access to rule matrices.

</td><td>

sn\_csm\_ctxrul\_mgt.rule\_matrix\_viewer

</td></tr><tr><td>

Rule matrix viewer

 \[sn\_csm\_ctxrul\_mgt.rule\_matrix\_viewer\]

</td><td>

Grants read access to matrix inputs, matrix outputs, matrix types, and rule matrices.

</td><td>

None

</td></tr><tr><td>

Context variable viewer

 \[sn\_csm\_ctxrul\_mgt.context\_variable\_viewer\]

</td><td>

Grants read access to context types and context variables.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_ctx_tables_inst"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Context Type

 \[sn\_csm\_ctxrul\_mgt\_context\_type\]

</td><td>

Stores a named context, such as transaction header, transaction lines, or across lines.

</td></tr><tr><td>

Context Variable

 \[sn\_csm\_ctxrul\_mgt\_context\_variable\]

</td><td>

Stores the variables that belong to a context type, including whether the variable is an input or an output and whether it is mapped to a field or resolved by script.

</td></tr><tr><td>

Matrix type

 \[sn\_csm\_ctxrul\_mgt\_matrix\_type\]

</td><td>

Stores the definition of a family of rule matrices, including its inputs, outputs, validations, and supported context types.

</td></tr><tr><td>

Matrix input

 \[sn\_csm\_ctxrul\_mgt\_matrix\_input\]

</td><td>

Stores an input column definition on a matrix type, which references an input context variable.

</td></tr><tr><td>

Matrix output

 \[sn\_csm\_ctxrul\_mgt\_matrix\_output\]

</td><td>

Stores an output column definition on a matrix type, which references an output context variable.

</td></tr><tr><td>

Matrix Validation

 \[sn\_csm\_ctxrul\_mgt\_matrix\_validation\]

</td><td>

Stores the link between a matrix type and a validation definition, and whether that validation is required.

</td></tr><tr><td>

Validation Definition

 \[sn\_csm\_ctxrul\_mgt\_validation\_definition\]

</td><td>

Stores a named row-level validation script that runs against decision table rows while an administrator authors them.

</td></tr><tr><td>

Rule Matrix

 \[sn\_csm\_ctxrul\_mgt\_rule\_matrix\]

</td><td>

Stores an administrator-authored rule matrix, which is backed by a decision table record and is versioned.

</td></tr><tr><td>

Rule Entity Filter

 \[sn\_csm\_ctxrul\_mgt\_rule\_entity\_filter\]

</td><td>

Stores a filter that scopes a rule matrix to a set of product offerings, categories, or catalogs, either as a static list or as a condition.

</td></tr></tbody>
</table>**Parent Topic:**[Pricing Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/price-management-reference.md)

