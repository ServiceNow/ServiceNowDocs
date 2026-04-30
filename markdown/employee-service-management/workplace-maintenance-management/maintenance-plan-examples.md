---
title: Maintenance plan schedule examples
description: Maintenance plans are created for models \(assets\) or locations. The schedule trigger type defined for a maintenance plan can be meter or duration-based schedule. Associate multiple templates to maintenance schedules as required. The scheduled job fetches plan records that have a template associated to it and creates maintenance cases for a maintenance plan.
locale: en-US
release: zurich
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Maintenance plan schedule examples

Maintenance plans are created for models \(assets\) or locations. The schedule trigger type defined for a maintenance plan can be meter or duration-based schedule. Associate multiple templates to maintenance schedules as required. The scheduled job fetches plan records that have a template associated to it and creates maintenance cases for a maintenance plan.

For example, use cases for creating maintenance plans can be based on the following:

-   Schedule printer ink cartridge replacement
-   Schedule coffee beans refill

## Maintenance schedule for printer ink cartridge replacement

Schedule a printer ink cartridge replacement after printing a specified number of pages for a location. For example, 10,000 pages. Define a general plan with a meter-based maintenance schedule. Associate a schedule template, for example, Schedule template A.

1.  Create a model-based maintenance plan for HP Printer Cartridge Replacement and publish the plan.

    For more information, see [Create and publish maintenance plans](../task/create-publish-maintenance-plans.md).

2.  Create a meter-based schedule:
    -   Name: Schedule name.
    -   Trigger: Select **Meter**.
    -   Trigger Type: Select the following trigger types for a meter-based schedule:
        -   Table: Pre-filled values based on your plan type \(model or location\).
        -   Field: For example, select the location type.
        -   Every: Integer-based value. For example: 3

The maintenance plan schedules the HP printer to replace ink cartridges after printing 10, 000 pages.

## Schedule coffee beans refilling for coffee machines

Schedule coffee beans refilling for coffee machines daily. Associate a schedule template, for example, Schedule template B. The schedule should have an entry in the Workplace Maintenance Service configuration table.

1.  Create a model-based maintenance plan for Coffee machines and publish the plan.
2.  Create a duration-based schedule:
    -   Name: Schedule name.
    -   Active: Select this option to activate the schedule for a maintenance plan.
    -   Trigger: Select **Duration**.
    -   Trigger Type: Interval. Specify the duration in days and hours since this is a daily schedule.

The coffee beans are refilled daily based on the scheduling condition and template associated to this maintenance plan.

For more information, see [Workplace planned maintenance scheduled job](sch-job-planned-nightly.md).

**Parent Topic:**[Workplace Maintenance Management references](workplace-maintenance-mgmt-references.md)

**Previous topic:**[Workplace Maintenance Management references](workplace-maintenance-mgmt-references.md)

**Next topic:**[Components installed with Workplace Maintenance Management](../reference/components-installed-with-maintenance-mgmt.md)

