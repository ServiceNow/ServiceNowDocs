---
title: Configuring Time Zones
description: There are multiple ways to set up time zones with Dispatcher Workspace. This gives dispatchers the flexibility to see Field Service technicians' times in a way that works best for them.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configuring Time Zones

There are multiple ways to set up time zones with Dispatcher Workspace. This gives dispatchers the flexibility to see Field Service technicians' times in a way that works best for them.

You don’t have to configure either of these options and can use Dispatcher Workspace with a single time zone. You can also use multiple time zones, and equalized time zones together at the same time, or separately.

## Multiple time zone configuration

If you choose to enable multiple time zones, then you must configure the time zones that dispatchers can choose from. For more information on how to add the time zones as options, see [Configure multiple time zones for dispatchers](../task/add-remore-time-zones.md).

## Resource time indicators

Resource time indicators render technicians' schedules based on their time zone on the calendar in Dispatcher Workspace. The technician's location determines their time zone. It shows all technicians lined up evenly on the calendar, but with a broken time indicator that corresponds with the technician’s location. To configure resource time indicators you must:

1.  Ensure that all locations have the correct time zone added. For more information on adding time zones to locations, see Set up locations.

    **Note:** If you don’t see a time zone drop-down on the location record, then add it to the form. For more information on adding form fields, see Configuring the form layout.

2.  Ensure that all Field Service Technicians have the correct time zone configured on their user record. The line break on the calendar in Dispatcher Workspace is determined based on the time zone configured on the technician’s user record. For more information on adding Time zones to user records, see: The User record.
3.  Enable the work.management.enable.timezone.agnostic property. For more information see [Enable resource time indicators](../task/enable-equalized-time.md).

