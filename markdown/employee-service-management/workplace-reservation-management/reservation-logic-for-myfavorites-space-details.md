---
title: Reservable module derivation logic for Space details
description: While selecting a reservable module from the Space details page, system identifies the reservable module based on the derivation logic.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Reservable module derivation logic for Space details

While selecting a reservable module from the Space details page, system identifies the reservable module based on the derivation logic.

When you select a space from the Space details page, application selects a suitable reservable module to make a reservation. The system attempts to select a reservable module with no **Min durations** and **Max durations**. In the absence of such a module, a reservable module with **Min durations** and **Max durations** set is chosen. In either case, if there are multiple modules satisfying the space criteria, the following logic is applied:

## Reservable Modules without Min and Max duration values

-   Workplace Reservation Management first selects a reservable module that has no **Min duration** and **Max duration** values set. If there are multiple modules with no **Min Duration** and **Max Duration** values, then application assigns the reservable module based on the following:
-   -   System checks for Reservable Modules where the **Override approval policy** is **Never require approval**, in case it does not find such a module, priority is given to a module with approval policy **No Override** followed by **Always require approval**.
-   If there are multiple modules having the same approval policy, system assigns the reservable modules where **Recurring** reservation is allowed.
-   If **Recurring** is allowed for multiple modules, system tries to assign the reservable modules where **Allows all day** reservation is allowed.
-   If **Recurring** is allowed and **All day** is set, the system selects a reservable module where **All day** is not mandatory.

## Reservable Modules with Min and Max duration values

The same selection criteria for reservation modules is applied in this case as with no **Min duration** and **Max duration** values. Only difference is that the system checks for whether the **Start time** and **End time** duration matches with the **Min duration** and **Max duration** values. If there are multiple modules having similar field values, system assigns the reservable module on the following logic:

-   If there are multiple modules having the same approval policy, system assigns the reservable modules where **Recurring** reservation is allowed.
-   If **Recurring** is allowed for multiple modules, system checks for and assigns the reservable modules where **Allows all day** reservation is allowed.
-   If **Recurring** is allowed and **All day** is also set, then, system selects a reservable module where **All day** is not mandatory.

For more information, see [Configure a reservable module](../task/config-reservable-module.md).

**Parent Topic:**[Workplace Reservation Management references](rsv-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Reservation Management](../reference/components-installed-with-wsd-reservation-mgmt.md)

[Properties installed with Workplace Reservation Management](../reference/properties-installed-with-wsd-reservation-mgmt.md)

[Workplace Reservation Management - Field descriptions](workplace-reservation-management-field-descriptions.md)

[Proximity calculation when browsing near a person](../reference/proximity-calculation-for-browse-near-person.md)

[Mobile push notifications for workplace reservations](../reference/reservation-push-notifications.md)

[Location privacy settings and impact](../reference/location-privacy-settings-and-impact.md)

[Additional details record producer - Mapping Variable types and limitations](../reference/custom-fields-record-producer-mapping-variable-type-conditions.md)

