---
title: Bi-directional account relationships
description: A bi-directional account relationship is a relationship that exists between two accounts. You can create account relationships between two customer accounts or between a partner account and a customer account.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create customer relationships, Configure accounts and contacts, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Bi-directional account relationships

A bi-directional account relationship is a relationship that exists between two accounts. You can create account relationships between two customer accounts or between a partner account and a customer account.

A bi-directional account relationship is based on a defined account relationship type. Creating a bi-directional account relationship is a two-step process that involves:

-   Defining the types of relationships that exist between your partners and customers.
-   Using these relationship types to create relationship records between selected accounts.

You can view relationship records on the Account form for either account in the relationship. These records are stored in the **Account Relationships** related list.

For relationships between a partner account and a customer account, partner account contacts with the partner role or the partner administrator role can create and manage cases for their customer accounts.

## Account relationship types

An account relationship type defines a relationship that can exist between accounts. Users with the system administrator role can define the following account relationship types:

-   Account to account
-   Partner to account

When creating an account relationship type, you define the following information on the Account Relationship Type form:

-   The type of **source** account \(account or partner\).
-   The type of **target** account \(account or partner\).
-   The relationship between the source account and the target account.
-   The reverse relationship between the source account and the target account.

![Account Relationship form displaying an instance of the relationship between two accounts.](../image/CSMAccountRelationshipTypeForm.png "Account Relationship Type form")

**Note:** One default account relationship type is provided for partner accounts.

## Account relationship records

Once an account relationship type has been defined, users with the customer service manager role can use it to create relationship between specific accounts or partners. An account relationship record includes the following information:

-   A source account, selected in the **Account From** field.
-   A target account, selected in the **Account To** field.
-   The account relationship type that this relationship record is based on.
-   The relationship and the reverse relationship of the selected accounts.

View a relationship record from either account:

-   The relationship \(**Account From** &gt; **Account To**\) appears in the **Account Relationships** related list on the source account record.
-   The reverse relationship \(**Account To** &gt; **Account From**\) appears in the **Account Relationships** related list on the target account record.

Select the account relationship record from either account to see the Account Relationship form.

![Account Relationship Type form displaying various fields related to customer and partner accounts.](../image/CSMAccountRelationshipForm.png "Account Relationship form")

You can also view account relationship records that use a specific account relationship type. This information appears as a related list on the Account Relationship Type form. This list shows the source account \(**Account From** field\) and the target account \(**Account To** field\) for each account relationship record.

