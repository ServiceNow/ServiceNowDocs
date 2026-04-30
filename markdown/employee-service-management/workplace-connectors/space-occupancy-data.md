---
title: Retrieving Space Occupancy Data
description: Retrieve the Space Occupancy Data table for loading workplace occupancy data and space occupancy data insights for a selected workplace location.
locale: en-US
release: xanadu
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Connectors for occupancy data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Retrieving Space Occupancy Data

Retrieve the Space Occupancy Data table for loading workplace occupancy data and space occupancy data insights for a selected workplace location.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Occupancy and Environment Sensors** &gt; **Occupancy and Environment Data**.

2.  On the form, review the field details for space occupancy data

    |Field|Descriptions|
    |-----|------------|
    |Location|Location details of the specific workspace.|
    |Space Occupancy value|Time series data. If the value is 0, it indicates space is unoccupied. If the value is greater than 0, it indicates space is occupied. Select this value to visualize the time-series data in different transforms. For more information, see [MetricBase transforms](https://www.servicenow.com/docs/access?context=metricbase-transforms&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).|

    The retrieved space occupancy data can be used to verify the following use cases:

    -   Showing the occupancy data in the Location Directory. For more information, see [Manage workplace activities and services with Location directory](../../workplace-service-delivery/concept/location-directory.md).
    -   Automatic reservation check-in. For more information, see [Configure automatic check-in for reserved spaces](../../wsd-reservation-management/concept/configure-rsv-check-in.md).

**Parent Topic:**[Setup Workplace Connectors for occupancy data](../concept/setup-occupancy-connectors.md)

**Previous topic:**[Retrieving Action Configurations data](actions-configurations-occupancy.md)

**Next topic:**[Setup Workplace Connectors for environmental data](../concept/setup-environmental-data-connectors.md)

