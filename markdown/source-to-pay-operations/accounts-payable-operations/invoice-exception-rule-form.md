---
title: Invoice Exception Rule Form
description: Invoice exception rules in Accounts Payable Operations define which invoices trigger exceptions and how they are handled. Use this reference to understand each form field and its configuration options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-exception-rule-form.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Invoice exception form, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice Exception Rule Form

Invoice exception rules in Accounts Payable Operations define which invoices trigger exceptions and how they are handled. Use this reference to understand each form field and its configuration options.

Invoice exception rules define the conditions under which invoices are flagged as exceptions in Accounts Payable Operations. Each rule specifies the exception type, triggering conditions, handling behavior, and processing order. The form fields control rule activation, resolution workflow, and exception prioritization.

## Form field definitions

The following table describes each field in the invoice exception rule for.

|Field name|Description|
|----------|-----------|
|Active|Controls whether the rule is enabled. When selected, the rule is active and exceptions are triggered. When cleared, the rule is inactive and invoices aren't flagged by this rule.|
|Allow bypass|When selected, authorized users can bypass this exception and proceed with invoice processing without triggering the exception.|
|Rejection mode|Controls how exceptions from this rule are resolved. Options: "Manual" or "None".|
|Base object|This field determines which records are evaluated against the rule conditions. sn\_shop\_invoice is the table name shown in the condition builder. Header level exception will be set to \[sn\_shop\_invoice\] table and for line level it will be set to \[sn\_shop\_invoice\_line\] table.|
|Condition|Defines the logical criteria that trigger the exception.|
|Condition field selector|A drop-down showing available invoice fields. Select a field to include in the condition criteria.|
|Condition operator|Logical operators for field comparison.|
|Condition value|The comparison value for the condition.|
|Condition logic \(AND / OR\)|Logical operators joining multiple conditions.|
|New Criteria button|Adds an additional condition row to the rule, allowing complex multi-field matching criteria.|
|Order|A numeric value that controls the sequence in which rules are evaluated.|

**Parent Topic:**[Invoice exception form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/exception-form-fields.md)

