---
title: Create a matching attributes geography
description: Creating a geography with matching attributes involves defining geographies based on specific criteria such as city, state, country, or ZIP code.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating geographies, Configuring Field Service Territory Planning, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Create a matching attributes geography

Creating a geography with matching attributes involves defining geographies based on specific criteria such as city, state, country, or ZIP code.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager

## About this task

Matching attributes provide a precise and criteria-based method for outlining geographies for scheduling without the need for visual appearance. It's a way to categorize and group geographies based on shared attributes, streamlining the process of managing work orders or tasks within those defined criteria.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Geography**.

2.  In the **Territory Geographies** page, select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the geography.|
    |Geography type|Select **Matching Attributes**.|

4.  Select **Submit**.

5.  Open the geography record to add the matching attributes.

6.  In the **Matching Attributes** related list, select **New**.

    1.  In the **Type** field, select a condition to confine the geography boundary.

        For example, Zip/Postal Code is equal to.

    2.  In the **Zip/Postal Code** field, enter a zip or postal code.

    3.  In the **City** field, enter a city name.

    4.  In the **State** field, enter a state name.

    5.  In the **Country** field, enter a country name.

7.  Select **Update**.

    The geography with matching attributes is created.


## Result

This geography when associated with a territory displays the territory information in the **Territories** list. It does not have visual appearance on the map when its territory is selected in the Territory Planning console.

## What to do next

Link the geography to a territory. For more information, see [Create a Field Service territory](create-territories-territory-planning-console.md).

