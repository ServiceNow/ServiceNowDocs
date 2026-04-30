---
title: Allow Event planners to handle reservations with more flexibility
description: Reservation planners can bypass or overrule certain settings in the Reservable module while moving a reservation to another location in the Event planner Scheduled View.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with schedule view, Working with Event planner, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Allow Event planners to handle reservations with more flexibility

Reservation planners can bypass or overrule certain settings in the Reservable module while moving a reservation to another location in the Event planner Scheduled View.

Space planners with the \(sn\_wsd\_rsv.reservation\_planner\) role can move a reservation when a location or space is part of a Reservable module. Space and reservation planners \(sn\_wsd\_rsv.reservation\_planner\) with the dedicated role \(sn\_wsd\_rsv.bypass\_module\_validation\) can ignore or bypass certain settings in the Reservable module configuration. They can move and update a reservation from one Reservable module to another without the need to recreate a reservation. Space planners can bypass the Reservable module configuration limitations to optimize reservations quickly and easily.

For example, reservation planners or space planners can bypass the following settings in the Reservable module:

-   Max days in the future
-   Max number of occurrence
-   Min and Max duration
-   Available in
-   All day

Space planners can do the following while moving a reservation in the Event planner:

-   Move to different Reservable modules when a space is available in multiple Reservable modules.

    **Note:** Space planners can’t move a reservation from one space to another when there’s no Reservable module associated with it.

-   Move shift-based reservations. Space planners can move a shift-based reservation to a location having the same-shift-based reservation module.

    **Note:** Space planners can’t move a shift-based reservation to a different shift-based module. When a space is part of two different shift-based Reservable modules, only one of the shift-based Reservable module is available for selection while moving a reservation. Space planners can move a shift-based Reservable module to a non-shift based Reservable module. For example, **Desks within a Shift Reservable** module to **Desks** Reservable module.


**Parent Topic:**[Working with schedule view](../task/working-with-schedule-view.md)

