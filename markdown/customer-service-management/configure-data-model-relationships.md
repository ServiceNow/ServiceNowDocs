---
title: Create relationships
description: Use relationships to provide internal and external users with additional access to customer data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Create relationships

Use relationships to provide internal and external users with additional access to customer data.

## Before you begin

Role required: admin

## About this task

With the Service Model Foundation feature, you can create relationships between the following users:

-   Between an internal user and an account, household, or consumer.
-   Between two consumers.

Relationships are based on responsibility definitions. These definitions describe a role or a function that supports a customer. When you create a relationship, you select the users involved in the relationship and the responsibility that one user performs on behalf of another.

The Service Model Foundation plugins provide:

-   Relationships that you can create between users.
-   Responsibility definitions that you can assign to a user in a relationship.

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

Use the Account Manager responsibility to create a relationship between an internal user and an account. With this relationship, the internal user can: -   Create and manage cases for their accounts.
-   View account information, including the related entities for an account.
-   Create and manage contacts and additional addresses for their accounts.

</td></tr><tr><td>

Relationship Manager

</td><td>

-   Consumer Team Member
-   Household Team Member

</td><td>

Use the Relationship Manager responsibility to create a relationship between:-   An internal user and a consumer.
-   An internal user and a household.

 With this relationship, the internal user can do the following:

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
</table>## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer Relationships**.

2.  Select the desired relationship.

<table id="choicetable_emj_jjz_2mb"><tbody><tr><td id="d98532e259">

**Account Team Members**

</td><td>

Create a relationship between an internal user and an account.

</td></tr><tr><td id="d98532e268">

**Consumer Team Members**

</td><td>

Create a relationship between an internal user and a consumer.

</td></tr><tr><td id="d98532e277">

**Household Team Members**

</td><td>

Create a relationship between an internal user and a household.

</td></tr><tr><td id="d98532e286">

**Consumer Relationships**

</td><td>

Create a relationship between two consumers, regardless of household.

</td></tr><tr><td id="d98532e295">

**Household Relationships**

</td><td>

Create a relationship between two consumers within a household.

</td></tr></tbody>
</table>3.  From the selected relationship list, select **New**.

4.  Fill in the following fields for the selected relationship.

<table id="table_bvg_mkz_2mb"><thead><tr><th>

Form

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Account Team Member

</td><td>

-   **Account**: Select the account to which the internal user is assigned.
-   **Responsibility**: Select the **Account Manager** responsibility.
-   **User**: Select the internal user to fulfill the responsibility.
-   **Type**: Select the type from the list of related party configurations.
-   **Order**: Select the order that specifies the sequence in which records are displayed, organized according to business preferences.


</td></tr><tr><td>

Consumer Team Member

</td><td>

-   **Consumer**: Select the consumer to which the internal user is assigned.
-   **Responsibility**: Select the **Relationship Manager** responsibility.
-   **User**: Select the internal user to fulfill the responsibility.
-   **Order**: Select the order that specifies the sequence in which records are displayed, organized according to business preferences.


</td></tr><tr><td>

Household Team Member

</td><td>

-   **Household**: Select the household to which the internal user is assigned.
-   **Responsibility**: Select the **Relationship Manager** responsibility.
-   **User**: Select the internal user to fulfill the responsibility.
-   **Order**: Select the order that specifies the sequence in which records are displayed, organized according to business preferences.


</td></tr><tr><td>

Consumer to Consumer Relationship

</td><td>

-   **Consumer is**: Select the consumer to fulfill the responsibility on behalf of another consumer.
-   **Responsibility**: Select the **Authorized Representative** responsibility.
-   **of Consumer**: Select the consumer who is being represented by the consumer in the **Consumer is** field.


</td></tr><tr><td>

Household Member Relationship

</td><td>

-   **Household**; select the desired household.
-   **Consumer is**: Select the consumer in the household to fulfill the responsibility on behalf of another consumer within the same household.
-   **Responsibility**: Select the **Authorized Representative** responsibility.
-   **of Consumer**: Select the consumer who is being represented by the consumer in the **Consumer is** field.
-   **Type**: Select the type from the list of related party configurations.
-   **Order**: Select the order that specifies the sequence in which records are displayed, organized according to business preferences.


</td></tr></tbody>
</table>5.  Select **Submit**.

    The relationship is added to the relationship list.

    Account, Consumer, and Household Team Member relationships are also added to the corresponding related lists on the Business Location form.

    -   Account Staff Relationships
    -   Consumer Staff Relationships
    -   Household Staff Relationships
    Consumer to Consumer and Household Member relationships are added to the following related lists:

    -   Household form &gt; Member Relationships
    -   Consumer form &gt; Consumer Relationships

**Related topics**  


[Service Model Foundation responsibilities](../reference/csm-data-model-responsibilities.md)

[Create a responsibility definition](t_CreateAResponsibilityDefinition.md)

