---
title: Service Model Foundation business locations
description: Use the business location entity to create an organizational structure that includes internal and external business locations such as stores, branches, franchises, and dealerships.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Service Model Foundation business locations

Use the business location entity to create an organizational structure that includes internal and external business locations such as stores, branches, franchises, and dealerships.

A business location is an extension of a service organization. The business location entity enables you to model the internal and external organizational structure involved in supporting customers. It also enables you to give agents the right level of visibility into customer data.

With the business location entity you can:

-   Create internal and external business locations using a hierarchy, with parent and child locations.
-   Associate users within a business location, which makes them staff members of that location.
-   Provide staff members at a business location with access to the customer cases and information for that location.
-   Create teams of staff members to support accounts, consumers, and households.
-   Provide the staff members on those teams with access that enables them to manage cases for their accounts, consumers, and households.

## Creating a business location

Maintain an organizational structure by creating internal and external business locations. To create a business location, see [Create a business location](../concept/create-business-location.md).

## Accessing business locations

Managers have access to their business location and to the business locations that are designated as child locations in the hierarchy.

-   When a user is added to the **Manager** field, the sn\_customerservice.svc\_location\_manager role is automatically added to that user.
-   You can add a user as the manager for multiple business locations.

Staff members with the location agent role or location consumer agent role can perform the following actions:

-   Create cases for customers in their business locations.
-   Access cases where the location in the **Service Organization** field on the Case form matches their business locations.

