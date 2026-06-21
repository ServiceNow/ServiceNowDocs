---
title: Retrieving Space Occupancy Data
description: Retrieve the Occupancy and Environment Data table for loading workplace occupancy data and space occupancy data insights for a selected workplace location.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/workplace-connectors/space-occupancy-data.html
release: yokohama
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Connectors for occupancy data, Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Retrieving Space Occupancy Data

Retrieve the Occupancy and Environment Data table for loading workplace occupancy data and space occupancy data insights for a selected workplace location.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Occupancy and Environment Sensors** &gt; **Occupancy and Environment Data**.

2.  On the form, review the field details for space occupancy data.

    |Field|Descriptions|
    |-----|------------|
    |Location|Location details of the specific workspace.|
    |Space Occupancy value|Time series data. If the value is 0, it indicates space is unoccupied. If the value is greater than 0, it indicates space is occupied. Select this value to visualize the time-series data in different transforms. For more information, see .|

    The retrieved space occupancy data can be used to verify the following use cases:

    -   Showing the occupancy data in the Location Directory. For more information, see [Manage workplace activities and services with Location directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown).
    -   Automatic reservation check-in. For more information, see [Configure automatic check-in for reserved spaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/workplace-reservation-management/configure-rsv-check-in.md).

**Parent Topic:**[Setup Workplace Connectors for occupancy data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/workplace-connectors/setup-occupancy-connectors.md)

**Previous topic:**[Retrieving Action Configurations data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/workplace-connectors/actions-configurations-occupancy.md)

**Next topic:**[Setup Workplace Connectors for environmental data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/workplace-connectors/setup-environmental-data-connectors.md)

