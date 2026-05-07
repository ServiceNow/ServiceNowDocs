---
title: Transaction Manager use case: Display LIG line number on line detail
description: How to display the line item group line number in the line detail.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transaction Manager: Use cases, Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager use case: Display LIG line number on line detail

How to display the line item group line number in the line detail.

This document outlines the implementation approach for displaying the line item group \(LIG\) line number in the line detail layout. This enhancement lets users easily reference and correlate the line detail with the appropriate line in the LIG.

To display the line number in the line detail view, follow the steps below. This requires using a line detail layout \(for example, `default_layout_linedetail`\).

1.  Create a custom read-only line-level field to store the row number.

    -   Variable name: `txn.line.custom.rowNumber`
    -   Default value: `{{txn#rowNumber}}`
    ![Row number](../images/cpq-txn-mgr-use-case-display-line-number-1.png)

2.  Add the new field to your line detail layout to make it visible when viewing line items.

    Ensure that the field has the setting `"enableMarkdown": true`. Additionally, to display the row number on the LIG line, add the `"showLineNumbers": true` property to the `lineGrid` layout object in the non-line detail layout \(or layouts\).

3.  Save and deploy the updated blueprint with the modified layouts.
4.  In the Transaction UI, create a new transaction or open an existing one.

    The line number appears in the line detail view, as in the following example:

    ![Line detail screen](../images/cpq-txn-mgr-use-case-display-line-number-2.png)


**Parent Topic:**[Transaction Manager: Use cases](transaction-manager-use-cases.md)

