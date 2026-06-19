---
title: Transaction Manager use case: Display LIG line number on line detail
description: How to display the Line Item Group line number in the Line Detail.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/sales-and-order-management/transaction-manager-use-case-display-lig-line-number-on-line-detail.html
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 1
breadcrumb: [Transaction Manager: Use cases, Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager use case: Display LIG line number on line detail

How to display the Line Item Group line number in the Line Detail.

This document outlines the implementation approach for displaying the Line Item Group \(LIG\) Line Number in the Line Detail layout. This enhancement lets users easily reference and correlate the line detail with the appropriate line in the LIG.

To display the line number in the Line Detail view, follow the steps below. This requires using a Line Detail Layout \(for example, `default_layout_linedetail`\).

1.  Create a custom read-only line-level field to store the row number.

    -   Variable Name: `txn.line.custom.rowNumber`
    -   Default Value: `{{txn#rowNumber}}`
    \[Omitted image "cpq-txn-mgr-use-case-display-line-number-1.png"\] Alt text: Row number

2.  Add the new field to your Line Detail layout to make it visible when viewing line items.

    Ensure that the field has the setting `"enableMarkdown": true`. Additionally, to display the row number on the LIG line, add the `"showLineNumbers": true` property to the lineGrid layout object in the non-line detail layout \(or layouts\).

3.  Save and deploy the updated blueprint with the modified layouts.
4.  In the Transaction UI, create a new transaction or open an existing one.

    The line number appears in the Line Detail view, as in the following example:

    \[Omitted image "cpq-txn-mgr-use-case-display-line-number-2.png"\] Alt text: Line detail screen


**Parent Topic:**[Transaction Manager: Use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/transaction-manager-use-cases.md)

