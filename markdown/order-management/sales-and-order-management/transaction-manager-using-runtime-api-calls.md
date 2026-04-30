---
title: Transaction Manager: Using Runtime API calls
description: See a list of the APIs that are used in the runtime end user experience, together with their purposes and responses.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 2
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Using Runtime API calls

See a list of the APIs that are used in the runtime end user experience, together with their purposes and responses.

ServiceNow CPQ APIs are divided into two categories: Runtime APIs and admin APIs. This article lists the runtime APIs for Transaction Manager.

The Runtime APIs are the same APIs that are used in the runtime end user experience and include the following key actions.

-   Initialize a session
    -   Purpose: Initializes a session to establish a context for executing transaction events, managing state, and processing subsequent API calls. Can initialize for an existing transaction, or if not specified, a new transaction will be created.
    -   Response: Returns a Session ID, Transaction ID, and transaction information.
-   Delete a session
    -   Purpose: Deletes a session to securely end user activity, clear session-specific data, and free up system resources.
    -   Response: Session is deleted. No information is returned.
-   Create a transaction
    -   Purpose: Creates a transaction, providing the object to manage the transaction lifecycle, configure and add products, and determine pricing.
    -   Response: Returns a Transaction ID and transaction information.
-   Run events on a transaction \(system and custom\)
    -   Purpose: Triggers a specified event on a transaction to execute predefined logic or workflows, such as editing field values, initiating approvals, versioning transactions, or validating configurations.
    -   Response: Varies by specified event.
-   Add products to a transactions \(upsert\)
    -   Purpose: Adds a product or products to a transaction, allowing dynamic configuration and pricing updates based on the product’s attributes.
    -   Response: Returns updated transaction data with additional product.
-   Get a list of transactions
    -   Purpose: Retrieves the list of transactions, enabling users to view, manage, or take action on an existing transaction.
    -   Response: List of transactions with Transaction ID and other metadata.
-   Get details of a transaction
    -   Purpose: Retrieves the header information of a transaction, providing key details such as stage, account, and summary-level data needed for display or processing.
    -   Response: All header field data for the transaction.
-   Get a transaction's lines
    -   Purpose: Retrieves the line item details for a transaction, returning product-level data such as quantities, pricing, and custom attributes for each item in the quote.
    -   Response: All line-level field data for the transaction.
-   Get statistics for transactions
    -   Purpose: Retrieves views and sessions by user as well as average time spent per stage for a given date range. Date range specifies a `toDate` and `days` which gets statistics from `(toDate - days) -> toDate`.
    -   Response: Summary metrics for date range.

[Postman Collection](https://logikio.atlassian.net/wiki/spaces/CS/pages/2234351617/Txn+Mgr+-+Intro+to+Transaction+Manager+Runtime+API+Calls)

