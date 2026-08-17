---
title: Service Model Foundation relationships
description: Create relationships between an agent and a customer or between two consumers that provide additional access to customer data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-data-model-relationships.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Service Model Foundation relationships

Create relationships between an agent and a customer or between two consumers that provide additional access to customer data.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## Relationships between internal users and customers

Internal users can have relationships with accounts, consumers, and households. These relationships provide internal users with additional access to customer cases and information. An internal user with a relationship to a customer can create and manage cases on behalf of that customer.

Relationships are created using responsibilities. Use the following responsibilities to create relationships between internal users and customers:

-   Account Manager: Use this responsibility to create a relationship between a staff member and an account.
-   Relationship Manager: Use this responsibility to create a relationship between a staff member and a household or a consumer.

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

When a relationship definition is deleted, all the relationships that use the definition are also deleted.

When a consumer is deleted, all the relationships to which the consumer belonged are also deleted.

When a household is deleted, all the relationships created for the household are also deleted.

When a consumer stops being a current member of a household, all the relationships created for the consumer within the household are also deleted.

