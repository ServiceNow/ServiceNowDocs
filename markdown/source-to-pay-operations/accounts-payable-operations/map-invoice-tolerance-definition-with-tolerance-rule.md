---
title: Map invoice tolerance type with invoice exception definition
description: Map invoice tolerance type definitions with invoice exception definitions to apply custom tolerance thresholds to specific exception scenarios.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/map-invoice-tolerance-definition-with-tolerance-rule.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice exception, invoice tolerance]
breadcrumb: [Tolerance Rules and Variances for invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Map invoice tolerance type with invoice exception definition

Map invoice tolerance type definitions with invoice exception definitions to apply custom tolerance thresholds to specific exception scenarios.

## Before you begin

Role required: sn\_ap\_apm.admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Administration** &gt; **Invoice exception definition**.

    \[Omitted image "apo-invoice-exp-nav.png"\] Alt text: Navigate to Invoice exception definitionFor more information on configuring **invoice exception definition**, see [Invoice exception definition form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-exception-definition-form.md).

2.  Populate the tolerance type on the invoice exception definition form.

    For more information on the tolerance type, see [Define an invoice tolerance type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/define-a-new-tolerance-type-definition.md).

3.  You must update the **Subflow** logic to include associated tolerance type logic as per the business requirement.

4.  Select **Submit**.


**Parent Topic:**[Tolerance Rules and Variances for invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/tolerance-rules-and-variance.md)

