---
title: Configuring households
description: The household entity represents a group of consumers that usually share a common address and use services as a group.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer data, Set up your environment, Configure, Customer Service Management]
---

# Configuring households

The household entity represents a group of consumers that usually share a common address and use services as a group.

A household is made up of consumers who have been added as members of that household.

**Note:** A household has an address and consumers have their own addresses. These addresses don’t need to be the same to add a consumer as a member to a household.

With the household entity, you can:

-   Create households and add consumers as household members.
-   Create cases for households and household members.
-   Create relationships between household members. These relationships authorize one household member to manage cases on behalf of another member.
-   Create relationships between staff members and households or household members that enable the staff members to manage cases for those households and members.
-   Track information for the households, including sold products, contracts, and entitlements.

## Head of household

A household can have one member designated as the head of the household. A consumer who is added as the head of household is automatically added as a member of the household.

The head of household has access to all the cases and information for the household and the other household members. The head of household can also see:

-   The sold products for the household.
-   The sold products and install base items for household members.

## Household information

Households can have multiple members. These members can be either consumers or consumer users. Consumers can also belong to multiple households.

Membership in a household is defined by the **Start Date** and **End Date** on the Household Member form. A household member is considered to be a current member if:

-   The **Start Date** field is empty or is filled in with today's date.
-   The **Start Date** field is filled in with a past date and the **End Date** field is empty or is filled in with today's date or a future date.

Only one record with current membership dates is enabled for each consumer in a household. A consumer can leave and rejoin a household multiple times. This information is recorded using the start and end dates.

As members are added or removed from a household, the member history is retained. You can find this information in the following related lists on the Household form.

-   **Current Members**: The consumers currently in the household.
-   **All Members**: The current and past members of a household. This list provides a history of the household. Members can appear multiple times in this list.

On the Household form, you can also find information about household cases and products in the following related lists:

-   **Cases**: The cases that have been created for all the members within a household
-   **Sold Products**: The products owned by the household. These products can be owned or shared by multiple household members.

## Household member relationships

The following types of relationships can be created for households and household members. These relationships are included in the following related lists on the Household form:

-   **Member Relationships**: Relationships that have been established between household members. These relationships are created using the Authorized Representative responsibility. Household members that have an Authorized Representative relationship with another household member can act on behalf of that member and can manage cases and information for that member.
-   **Household Team**: Relationships that have been established between an agent and a household. These relationships are created using the Relationship Manager responsibility. Agents with a Relationship Manager role for a household can access all cases linked to that household.

## Consumer relationships

The following types of relationships can be created for consumers.

-   **Consumer Relationships**: Relationships that have been established between two consumers, regardless of household. These relationships are created using the Authorized Representative responsibility. Consumers that have an Authorized Representative relationship with another consumer can manage cases for that consumer.
-   **Consumer Team**: Relationships that have been established between an agent and a consumer. These relationships are created using the Relationship Manager responsibility. Agents with a Relationship Manager role for a consumer can access all cases linked to that consumer.

