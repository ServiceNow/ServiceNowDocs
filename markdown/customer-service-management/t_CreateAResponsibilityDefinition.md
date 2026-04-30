---
title: Create a responsibility definition
description: A responsibility, or responsibility definition, specifies the role or function a user has within an entity, determining access through relationships. When creating a relationship, users are assigned specific responsibilities that grant access to the entity and its related entities.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring customer access management, User management, Set up your environment, Configure, Customer Service Management]
---

# Create a responsibility definition

A responsibility, or responsibility definition, specifies the role or function a user has within an entity, determining access through relationships. When creating a relationship, users are assigned specific responsibilities that grant access to the entity and its related entities.

## Before you begin

Role required: admin

## About this task

If you’re using the Service Model Foundation feature, you can also create the responsibility definitions to use in customer and consumer relationships. For more information about configuring Service Model Foundation, see [Configure Service Model Foundation](configure-industry-data-model.md).

The Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table supports domain separation. For more information on domain separation, see [Domain separation and Customer Service Management](../concept/domain-separation-customer-service.md).

**Note:** Starting with the Vancouver release, the Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table is reparented to the Application file \[sys\_metadata\] table.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Responsibility Definitions**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_gza_pjv_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the responsibility, fr example, account manager.

</td></tr><tr><td>

Type

</td><td>

Type of users to whom the responsibility can be assigned to:-   User: Select **User** if this responsibility should be assigned to an employee. When assigning this type, the list of available users comes from the users \[sys\_users\] table.
-   Contact: Select **Contact** if this responsibility should be assigned to a customer contact. When assigning this role, the list of available users comes from the contact \[customer\_contact\] table.
-   Consumer: Select **Consumer** if this responsibility should be assigned to a customer contact. When assigning this role, the list of available users comes from the consumer \[csm\_customer\] table.
-   Account: Select **Account** if this responsibility should be assigned to a customer contact. When assigning this role, the list of available users comes from the account \[customer\_account\] table.
-   None: Select **None** if this responsibility definition is to be used when creating relationships between consumers.
 **Note:** Only the responsibility definitions with **Type** set to **User** can be used in the following Service Model Foundation relationships:

-   Account Team Member
-   Consumer Team Member
-   Household Team Member


</td></tr><tr><td>

Unique

</td><td>

Option that you can select to disable the duplicate entries for the responsibility definition.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

[Configure access through the responsibility access configuration](declarative-resposibility-framework.md)

**Related topics**  


[Service Model Foundation responsibilities](../reference/csm-data-model-responsibilities.md)

