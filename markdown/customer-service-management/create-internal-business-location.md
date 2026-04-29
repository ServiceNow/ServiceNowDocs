---
title: Create an internal business location
description: Create an internal business location to enable users and consumers to create accounts, contacts, consumers, and households.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a business location, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create an internal business location

Create an internal business location to enable users and consumers to create accounts, contacts, consumers, and households.

## Before you begin

Role required: admin

## About this task

A business location has a manager. When you create an internal business location, you add a user to the **Manager** field on the Internal Business Location form. Users then added as internal business location managers are automatically assigned the sn\_customerservice.svc\_location\_manager\_contributor role.

However, to assign the sn\_customerservice.svc\_location\_manager role to the internal business location managers, the **sn\_bus\_loc.int\_bus\_loc.onboard\_location\_manager\_as\_contributor** system property must be set to **false**.

**Note:** Only internal users can be added as managers for internal business locations.

The manager of an internal business location can access all the cases for account, household, or consumer in the location hierarchy, including cases for child business locations. The manager can also:

-   Add staff members to business locations in the location hierarchy.
-   Create account team or consumer team relationships with staff members from the location hierarchy.
-   View customer information.
-   Update cases created in the location hierarchy.
-   Create cases for customers in the location hierarchy.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Service Organizations** &gt; **Internal Business Locations**.

2.  Select **New** on the Internal Business Locations list.

3.  Fill in the fields on the [Internal Business Location](../reference/data-model-business-location-form.md) form.

4.  Select **Submit**.

    The location is added to the Internal Business Locations list.

    After creating an internal business location, add staff members to it. You can then create relationships with accounts, households, and consumers, and track customers served by that location.


**Related topics**  


[Create an external business location](create-external-business-location.md)

