---
title: Service Model Foundation responsibilities
description: A responsibility, or responsibility definition, describes a role or a function that supports a customer. Use responsibility definitions to create relationships between an agent and a customer or between two consumers.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Service Model Foundation overview, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Service Model Foundation responsibilities

A responsibility, or responsibility definition, describes a role or a function that supports a customer. Use responsibility definitions to create relationships between an agent and a customer or between two consumers.

When you create a relationship, you select the users involved in the relationship and the responsibility that one user performs on behalf of another. The responsibility that is assigned to a relationship provides access to customer cases and information.

Service Model Foundation includes responsibility definitions that you can use to create relationships:

-   Between agents and accounts, households, or consumers.
-   Between two consumers.

The following responsibilities are provided with the Service Model Foundation plugins.

**Note:** Responsibilities are stored in the Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table.

<table id="table_ygc_wsk_jlb"><thead><tr><th>

Responsibility

</th><th>

Used in relationship

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Manager

</td><td>

Account Team Member

</td><td>

Use the Account Manager responsibility to create a relationship between an agent and an account. With this relationship, the agent can: -   Create and manage cases for their accounts.
-   View account information, including the related entities for an account.
-   Create and manage contacts and additional addresses for their accounts.

</td></tr><tr><td>

Relationship Manager

</td><td>

-   Consumer Team Member
-   Household Team Member

</td><td>

Use the Relationship Manager responsibility to create a relationship between:-   An agent and a consumer.
-   An agent and a household.

 With this relationship, the agent can do the following:

-   For a consumer:
    -   Create and manage cases for the consumer.
    -   View household information, including the related entities for that consumer.
-   For a household:
    -   Create and manage cases for the household.
    -   View household information, including the related entities for that household.
    -   Create and manage household members.

</td></tr><tr><td>

Authorized Representative

</td><td>

-   Consumer to Consumer Relationship
-   Household Member Relationship

</td><td>

Use the Authorized Representative responsibility to create a relationship between two consumers, regardless of household, or between two consumers within the same household.With this relationship, a consumer can:

-   Create and manage cases for another consumer.
-   View the information of another consumer.
-   View the install base information of another consumer and create cases for:
    -   Sold products
    -   Install base items

</td></tr></tbody>
</table>## Customizing responsibility definitions

You can use the responsibility definitions provided with Service Model Foundation plugins. You can also modify these definitions or create your own definitions to meet your business requirements.

**Note:** If you modify the existing definitions or create new definitions, you may also need to update ACLs to reflect the changes.

If you have an existing account manager responsibility definition, you may need to evaluate the functionality of the account manager responsibility definition provided with the Service Model Foundation plugins.

**Note:** Creating and using responsibility definitions is a feature available in releases prior to Paris. Customers can create responsibility definitions using the Responsibility Definition \(sn\_customerservice\_responsibility\_def\) table and use those definitions to create account teams using the Account Team Member \(sn\_customerservice\_team\_member\) table. For more information, see [Create account teams](../concept/configure-csm-account-teams.md).

## Create a responsibility definition

Users with the system administrator role can create responsibility definitions.

1.  Navigate to **Customer Service** &gt; **Administration** &gt; **Responsibility Definitions**.
2.  Select **New** and fill in the fields on the Responsibility Definition form.
3.  In the **Type** field, select **User** if this responsibility is to be used in the following relationships:
    -   Account Team Member
    -   Consumer Team Member
    -   Household Team Member
4.  If this responsibility is to be used in the following consumer relationships, set the **Type** field to **None**.
    -   Consumer to Consumer
    -   Household Member

For more information, see [Create a responsibility definition](../task/t_CreateAResponsibilityDefinition.md).

## Create a unique responsibility definition

A responsibility definition can be unique, meaning that the responsibility can only be assigned to one user. To make a responsibility definition unique:

1.  Navigate to **Customer Service** &gt; **Administration** &gt; **Responsibility Definitions**.
2.  Select a responsibility definition.
3.  Enable the **Unique** check box on the Responsibility Definition form.
4.  Select **Update**.

When creating or updating records in the following tables, the system checks for and enforces unique responsibilities.

-   Household Team Member \[sn\_customer\_rel\_household\_to\_user\]
-   Consumer Team Member \[sn\_customer\_rel\_consumer\_to\_user\]
-   Account Team Member \[sn\_customerservice\_team\_member\]

For example, the following table describes the table type, an associated responsibility and the applied unique behavior.

<table id="table_r3g_dyr_jlb"><thead><tr><th>

Table

</th><th>

Responsibility Example

</th><th>

Unique behavior

</th></tr></thead><tbody><tr><td>

Account Team Member

</td><td>

Account Manager

</td><td>

An account can have only one account manager but a user with the Account Manager responsibility can manage multiple accounts.

</td></tr><tr><td>

Consumer Team Member

</td><td>

Relationship Manager

</td><td>

A consumer can have only one Relationship Manager but a user with the Relationship Manager responsibility can manage multiple consumers.

</td></tr><tr><td>

Household Team Member

</td><td>

Relationship Manager

</td><td>

A household can have only one Relationship Manager but a user with the Relationship Manager responsibility can manage multiple households.

</td></tr></tbody>
</table>**Note:** The unique behavior of a responsibility definition is not enforced when the responsibility is used for relationships between consumers or household members.

