---
title: Workplace Profile Location Assignment form
description: The location assignment form helps you assign a location or a neighborhood to a workplace profile.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Workplace Profile Location Assignment form

The location assignment form helps you assign a location or a neighborhood to a workplace profile.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace profile

</td><td>

Workplace profile record that the location must be assigned to. A workplace profile can have multiple location assignments.For more information about workplace profiles, see [Map designated workspaces to user profiles](../task/map-employees-to-existing-workplace-locations-wsd.md).

</td></tr><tr><td>

Profile type

</td><td>

Type of assignment you want to set for the workplace profile. Neighborhood assignments are applicable if **Neighborhood** is selected as the group by or view by option in a scenario or building overview. Location assignments are applicable for all other options.

</td></tr><tr><td>

Neighborhood

</td><td>

Neighborhood record that you want to assign to the profile. This field appears only if the **Profile type** is set to Neighborhood assignment.

</td></tr><tr><td>

Workplace location

</td><td>

Workplace location record that you want to assign to the profile.**Note:** The Workplace location field is required for neighborhood assignment. Select the required building, floor, or space that you want to assign to the profile.

</td></tr><tr><td>

Schedule plan

</td><td>

Schedule plan that you want to use to assign workplace locations to the profile. For more information about schedule plans, see [Schedule Planning](../../workplace-central/concept/schedule-planning.md).

</td></tr><tr><td>

Active

</td><td>

Option to activate the record.

</td></tr><tr><td>

Is primary

</td><td>

Option to specify if the assigned workplace location is the primary location for the profile. A workplace profile can only be assigned one primary location.For more information about setting a primary location, see [Set the primary location of a workplace profile](../task/set-prim-location-of-worplace-profile.md).

</td></tr><tr><td>

Reason for anomaly

</td><td>

Anomaly that occurred due to a mismatch in the allocation or assignment type. For more information about anomalies, see [Workplace location assignment anomaly types](location-assignment-anomaly-types.md). This field is automatically calculated based on the workplace location and profile records.

</td></tr><tr><td>

Enable employee location privacy

</td><td>

Option to specify whether employees can hide their location assignments from other users.

</td></tr><tr><td>

Source

</td><td>

Source from which the location assignment record was created. This field is automatically generated and is only visible in the Workplace Profile Location Assignments related list.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Core references](../concept/wsd-references.md)

**Related topics**  


[Components installed with Workplace Core](components-installed-with-workplace-service-delivery.md)

[Properties installed with Workplace Core](properties-installed-with-workplace-service-delivery.md)

[Workplace location assignment anomaly types](location-assignment-anomaly-types.md)

[Reserve a space form](reserve-space-form.md)

