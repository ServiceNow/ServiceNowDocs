---
title: Create a responsibility definition
description: Define a role or responsibility that can support your organization and users in the Customer Service Management \(CSM\) application. By creating the responsibility definitions, you can create the relationships between your different entities like accounts, contacts, and more.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure customer access management, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Create a responsibility definition

Define a role or responsibility that can support your organization and users in the Customer Service Management \(CSM\) application. By creating the responsibility definitions, you can create the relationships between your different entities like accounts, contacts, and more.

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

Name of the responsibility.

</td></tr><tr><td>

Applicable to

</td><td>

Persona type that the responsibility applies to, such as the customer service managers or agents.

</td></tr><tr><td>

Type

</td><td>

Type of users to whom the responsibility can be assigned to:-   User: Select **User** if this responsibility should be assigned to an employee. When assigning this type, the list of available users comes from the Users \[sys\_users\] table.
-   Contact: Select **Contact** if this responsibility should be assigned to a customer contact. When assigning this role, the list of available users comes from the Contacts \[customer\_contact\] table.
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


**Related topics**  


[Service Model Foundation responsibilities](../reference/csm-data-model-responsibilities.md)

