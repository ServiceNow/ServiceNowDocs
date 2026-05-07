---
title: Transaction Manager: Using Runtime API calls
description: See a list of the APIs that are used in the runtime end user experience, together with their purposes and responses.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Using Runtime API calls

See a list of the APIs that are used in the runtime end user experience, together with their purposes and responses.

CPQ APIs are divided into two categories: runtime APIs and admin APIs. This article lists the runtime APIs for Transaction Manager.

The runtime APIs are the same APIs that are used in the runtime end user experience and include the following key actions.

-   Initialize a session
    -   Purpose: Initializes a session to establish a context for executing transaction events, managing state, and processing subsequent API calls. Can initialize for an existing transaction. If a transaction is not specified, a new transaction is created.
    -   Response: Returns a session ID, a transaction ID, and transaction information.
-   Delete a session
    -   Purpose: Deletes a session to securely end user activity, clear session-specific data, and free up system resources.
    -   Response: The session is deleted. No information is returned.
-   Create a transaction
    -   Purpose: Creates a transaction, providing the object to manage the transaction life cycle, configure and add products, and determine pricing.
    -   Response: Returns a transaction ID and transaction information.
-   Run events on a transaction \(system and custom\)
    -   Purpose: Triggers a specified event on a transaction to execute predefined logic or workflows, such as editing field values, initiating approvals, versioning transactions, and validating configurations.
    -   Response: Varies by event.
-   Add products to a transactions \(upsert\)
    -   Purpose: Adds a product or products to a transaction, enabling dynamic configuration and pricing updates based on the product’s attributes.
    -   Response: Returns updated transaction data with the additional product.
-   Get a list of transactions
    -   Purpose: Retrieves a list of transactions, enabling users to view, manage, or take action on existing transactions.
    -   Response: A list of transactions with transaction IDs and other metadata.
-   Get details of a transaction
    -   Purpose: Retrieves the header information of a transaction, providing key details such as stage, account, and the summary-level data needed for display or processing.
    -   Response: All header field data for the transaction.
-   Get a transaction's lines
    -   Purpose: Retrieves the line item details for a transaction, returning product-level data such as quantities, pricing, and custom attributes for each item in the quote.
    -   Response: All line-level field data for the transaction.
-   Get statistics for transactions

    -   Purpose: Retrieves metrics on transactions. Metrics include views by user, session time by user, and stage time.
    -   Response: Summary metrics for the last 30 days or for a specified date range.
    For further details about the Transaction Manager metrics API, see [Transaction Manager: Transaction metrics API](cpq-transaction-manager-metrics-api.md).


[Postman Collection](https://logikio.atlassian.net/wiki/spaces/CS/pages/2234351617/Txn+Mgr+-+Intro+to+Transaction+Manager+Runtime+API+Calls)

