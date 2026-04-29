---
title: Service Model Foundation responsibilities
description: A responsibility, or responsibility definition, describes a role or a function that supports a customer. Use responsibility definitions to create relationships between an agent and a customer or between two consumers.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Service Model Foundation responsibilities

A responsibility, or responsibility definition, describes a role or a function that supports a customer. Use responsibility definitions to create relationships between an agent and a customer or between two consumers.

When you create a relationship, you select the users involved in the relationship and the responsibility that one user performs on behalf of another. The responsibility that is assigned to a relationship provides access to customer cases and information.

Service Model Foundation includes responsibility definitions that you can use to create relationships:

-   Between agents and accounts, households, or consumers.
-   Between two consumers.

The following responsibilities are provided with the Service Model Foundation plugins.

**Note:** Responsibilities are stored in the Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table.

For the list of responsibilities included in the base system, see [List of responsibilities provided with the base system](list-of-reponsibilities-provided-with-base-system.md). To create a responsibility, see [Create a responsibility definition](../task/t_CreateAResponsibilityDefinition.md).

## Customizing responsibility definitions

You can use the responsibility definitions provided with Service Model Foundation plugins. You can also modify these definitions or create your own definitions to meet your business requirements.

**Note:** If you modify the existing definitions or create definitions, you must update access control lists \(ACLs\) to reflect the changes.

If you have an existing account manager responsibility definition, you must evaluate the functionality of the account manager responsibility definition provided with the Service Model Foundation plugins.

**Note:** Creating and using responsibility definitions is a feature available in releases before Paris. Customers can create responsibility definitions using the Responsibility Definition \(sn\_customerservice\_responsibility\_def\) table and use those definitions to create account teams using the Account Team Member \(sn\_customerservice\_team\_member\) table. For more information, see [Create account teams](../concept/configure-csm-account-teams.md).

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
</table>**Note:** The unique behavior of a responsibility definition isn’t enforced when the responsibility is used for relationships between consumers or household members.

