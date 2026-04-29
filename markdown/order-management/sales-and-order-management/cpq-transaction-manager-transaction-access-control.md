---
title: Transaction Manager: Transaction Access Control
description: Using the Transaction Access control feature, you can precisely control which users can view or modify a transaction.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager: Transaction Access Control

Using the Transaction Access control feature, you can precisely control which users can view or modify a transaction.

The Transaction Access Control feature improves security and compliance by providing precise control over who can view and edit each transaction. In headless use cases, it can limit a list of transactions to those the current user has access to.

This feature is controlled by a tenant setting and is disabled by default. When the feature is disabled, all users can access all transactions.

## Access levels

Admin:

-   Can view and edit all transactions
-   Can grant full access to others
-   Can revoke full access, but not owner status
-   Cannot be removed

Owner:

-   Assigned to the creator of a transaction
-   Can view and edit the owned transaction
-   Can grant or revoke full access
-   Cannot be removed \(if last owner\)

Full access:

-   Can view and edit specified transactions
-   Can grant or revoke full access of others

## Usage

Access control can be accessed through the runtime UI.

![Transaction access](../images/cpq-txn-mgr-access-control.png)

Any user with access can grant or remove access for others. However, admins and owners cannot have their access removed. When users without access try to open restricted transactions, they receive an error.

When Transaction Access Control is enabled on an instance that has transactions, transaction creators automatically become owners. Users who have edited a transaction receive full access.

## API support

Access can be granted or revoked through API calls. API can also be used to retrieve a list of transactions to which a user has access, and return a history of users who were granted or revoked access. For a Postman colleciton of Transaction Manager access control API calls, contact support.

