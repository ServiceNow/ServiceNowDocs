---
title: Account address access for contacts
description: Enable contacts and similar roles to access addresses linked to their accounts. This access enables them to view and select account-related addresses and the corresponding location records tied to those accounts.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Account Address table, Enhanced address data model for accounts, Configure accounts and contacts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Account address access for contacts

Enable contacts and similar roles to access addresses linked to their accounts. This access enables them to view and select account-related addresses and the corresponding location records tied to those accounts.

## Account Address overview

Account Addresses \[account\_address\_relationship\] table acts as a bridge between accounts and locations, enabling you to associate multiple locations with a single account. They also enable the reuse of the same address record across multiple accounts using shared references.

## Accessible Accounts overview

Accessible accounts are customer accounts that a contact can access based on their role and access configuration. Contacts can access their accounts through:

-   Direct association with accounts
-   Association to the accounts through customer relationships
-   Assigned roles or access control list \(ACL\) permissions

This feature extends account address and location access to external roles such as:

-   Contact \[sn\_customerservice.customer\]
-   Contact Admin \[sn\_customerservice.customer\_admin\]
-   Customer Case Manager \[sn\_customerservice.​customer\_case\_manager​\]
-   Customer Account Admin \[customer\_account\_admin\]
-   Partner \[sn\_customerservice.partner\]
-   Partner Admin \[sn\_customerservice.​partner\_admin\]
-   Contact Manager \(internal\) \[sn\_customerservice.contact\_manager\]
-   Roles that inherit the Contact \[sn\_customerservice.customer\] role

Each of these external roles already has access to their associated accounts. However, they didn't previously have access to the associated account addresses and locations. With this enhancement, they can access the related account addresses and location records for those accounts.

## Contact access to account-related addresses

Contacts can access account addresses and corresponding location records through different types of account relationships. These relationships determine which accounts and addresses they can view or interact with.

-   My Account: It’s a direct, one-to-one relationship between the contact and it's assigned account. For example, a service provider is added as a contact under the parent account. Through the parent-child hierarchy, they can view and manage cases, addresses, and locations across child accounts in different regions.
-   Other Accessible Accounts: They’re additional accounts that contacts can access indirectly, through one of the following relationships:
    -   Account Hierarchy: Access is inherited through parent-child account relationships. If a contact is associated with the parent account, they might automatically access the child accounts. For example, a global IT manager associated with the parent account can view and manage cases, addresses, and location records from regional teams under child accounts.
    -   Account Relationship: Access is granted through formal associations between two customer accounts that aren’t part of a hierarchy, and can be unidirectional or bidirectional. For example, a partner account managing support for products from another organization. Through this relationship, contacts from the partner account can access the addresses of the associated customer account.
    -   Contact Relationship: Access is granted when a contact is linked to another customer account they don’t belong to directly. This relationship is commonly used where a contact works across multiple accounts, such as an external service provider. For example, a consultant working with three client organizations can access the associated addresses and locations of all three accounts.

