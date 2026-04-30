---
title: Workplace location assignment anomaly types
description: Anomalies occur when there’s a mismatch in the allocation or assignment of a workplace profile and workplace location.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Workplace location assignment anomaly types

Anomalies occur when there’s a mismatch in the allocation or assignment of a workplace profile and workplace location.

<table id="table_sky_1ff_rpb"><thead><tr><th>

Reason for anomaly

</th><th>

Description

</th></tr></thead><tbody><tr><td>

No anomaly

</td><td>

There’s no anomaly.

</td></tr><tr><td>

Assignment type mismatch

</td><td>

The **Assignment type** of both the user profile and the **Workplace location** to which the user is assigned doesn’t match.

</td></tr><tr><td>

Allocation mismatch

</td><td>

The allocation of both the user profile and the **Workplace location** to which the user is assigned doesn’t match. The allocation mismatch considers the allocation set in the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property.Time-bound allocations follow only the start date and end date of the allocation, which are set in the system time zone. For more information, see [Allocate a cost center, department, or workplace entity](../../workplace-space-management/task/add-cost-center-department-floor.md).

</td></tr><tr><td>

Assignment type and allocation mismatch

</td><td>

The **Assignment type** and the allocation of both the user profile and the **Workplace location** to which the user is assigned doesn’t match.

</td></tr><tr><td>

Restricted neighborhood assignment mismatch

</td><td>

This anomaly arises due to any one of the following mismatches:-   When a user profile is assigned to a space that is assigned to a restricted neighborhood but the user profile isn’t assigned to that restricted neighborhood.
-   When a user profile is assigned to a space that is not assigned to the restricted neighborhood but the user profile is assigned to that neighborhood.

</td></tr><tr><td>

Space not part of neighborhood

</td><td>

The assigned **Workplace location** of the user is not part of the specified **Neighborhood**.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Core references](../concept/wsd-references.md)

**Related topics**  


[Components installed with Workplace Core](components-installed-with-workplace-service-delivery.md)

[Properties installed with Workplace Core](properties-installed-with-workplace-service-delivery.md)

[Workplace Profile Location Assignment form](wsd-location-assignment-form.md)

[Reserve a space form](reserve-space-form.md)

