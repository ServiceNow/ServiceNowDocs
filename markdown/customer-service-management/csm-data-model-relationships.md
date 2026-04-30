---
title: Service Model Foundation relationships
description: Create relationships between an agent and a customer or between two consumers that provide additional access to customer data.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Service Model Foundation overview, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Service Model Foundation relationships

Create relationships between an agent and a customer or between two consumers that provide additional access to customer data.

With the Service Model Foundation feature, you can create relationships between the following users:

-   Between an internal user and an account, household, or consumer.
-   Between two consumers.

Relationships are based on responsibilities, or responsibility definitions. When you create a relationship, you select the users involved in the relationship and the responsibility that one user performs on behalf of another. The responsibility that is assigned to a relationship provides access to customer cases and information.

The following relationships are provided with the Service Model Foundation plugins.

<table id="table_ygc_wsk_jlb"><thead><tr><th>

Relationship

</th><th>

Responsibility used in the relationship

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Team Member\[sn\_customerservice\_team\_member\]

</td><td>

Account Manager

</td><td>

Create a relationship between an internal user and an account.**Note:** The internal user in this relationship must also be assigned the relationship agent role \(sn\_customerservice.relationship\_agent\).

</td></tr><tr><td>

Consumer Team Member\[sn\_customer\_rel\_consumer\_to\_user\]

</td><td>

Relationship Manager

</td><td>

Create a relationship between an internal user and a consumer.**Note:** The internal user in this relationship must also be assigned the relationship agent role \(sn\_customerservice.relationship\_agent\).

</td></tr><tr><td>

Household Team Member\[sn\_customer\_rel\_household\_to\_user\]

</td><td>

Relationship Manager

</td><td>

Create a relationship between an internal user and a household.**Note:** The internal user in this relationship must also be assigned the relationship agent role \(sn\_customerservice.relationship\_agent\).

</td></tr><tr><td>

Consumer to Consumer\[sn\_customer\_rel\_consumer\_to\_consumer\]

</td><td>

Authorized Representative

</td><td>

Create a relationship between two consumers, regardless of household.

</td></tr><tr><td>

Household Member Relationships\[sn\_customer\_rel\_household\_member\_relationship\]

</td><td>

Authorized Representative

</td><td>

Create a relationship between two consumers within a household.

</td></tr></tbody>
</table>## Relationships between internal users and customers

Internal users can have relationships with accounts, consumers, and households. These relationships provide internal users with additional access to customer cases and information. An internal user with a relationship to a customer can create and manage cases on behalf of that customer.

Relationships are created using responsibilities. Use the following responsibilities to create relationships between internal users and customers:

-   Account Manager: use this responsibility to create a relationship between a staff member and an account.
-   Relationship Manager: use this responsibility to create a relationship between a staff member and a household or a consumer.

Relationships that you create are added to the following related lists:

-   Account Staff Relationships on the Business Location form
-   Consumer Staff Relationships on the Business Location form
-   Household Staff Relationships on the Business Location form
-   Account Team on the Consumer form
-   Consumer Team on the Consumer form
-   Household Team on the Household form

## Relationships between consumers

Consumers can have relationships with other consumers. These relationships enable consumers to view and manage cases and information on behalf of other consumers.

Relationships are created using responsibilities. Use the Authorized Representative responsibility to create relationships between consumers. With this responsibility, you can:

-   Create a relationship between two consumers, regardless of household.
-   Create a relationship between two consumers within a household.

Relationships that you create are added to the following related lists:

-   Member Relationships on the Household form
-   Consumer Relationships on the Consumer form

## Deleting relationships

When a relationship definition is deleted, all of the relationships that use the definition are also deleted.

When a consumer is deleted, all of the relationships to which the consumer belonged are also deleted.

When a household is deleted, all of the relationships created for the household are also deleted.

When a consumer stops being a current member of a household, all of the relationships created for the consumer within the household are also deleted. .

