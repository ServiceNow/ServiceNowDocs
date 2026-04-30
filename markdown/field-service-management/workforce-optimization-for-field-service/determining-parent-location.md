---
title: Mapping a service location to a parent location
description: Map a service location to a parent location by setting parent determination rules.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service with Service Locations, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Mapping a service location to a parent location

Map a service location to a parent location by setting parent determination rules.

Parent determination uses a business rule that is stored in the **wm\_location\_parent\_lookup\_rule** table to map a service location to its parent location. All service locations are mapped to their corresponding parent location. The system checks the combination of fields and assigns the parent location to a work order or work order task.

Rules are executed in the following order to determine a parent location when a new service location is added:

1.  **Zip / Postal Code**: The corresponding parent location is assigned when a zip code and country values match.
2.  **Min Zip / Postal Code** and **Max Zip / Postal Code**: When a zip code and country values fall under the defined minimum and maximum zip code range, then the corresponding parent location is assigned.
3.  **City** and **State**: When city, state, and country values match, then the corresponding parent location is assigned.
4.  **State**: When state and country values match, then the corresponding parent location is assigned.

**Note:** The **Country** name is the default selection for all the criteria.

For more information, see [Create parent determination rules for service locations](../task/configure-parent-determination.md).

**Related topics**  


[Setting ad-hoc locations in work orders and work order tasks](service-locations-work-orders.md)

