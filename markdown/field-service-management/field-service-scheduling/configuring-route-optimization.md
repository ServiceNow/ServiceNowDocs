---
title: Configuring Route Optimization
description: Route optimization is essential for improving resource allocation in field service management. It strategically reorders tasks to reduce travel time for field agents, enhancing both productivity and customer service.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configuring Route Optimization

Route optimization is essential for improving resource allocation in field service management. It strategically reorders tasks to reduce travel time for field agents, enhancing both productivity and customer service.

## Configuration overview

The steps to set up Route Optimization are:

1.  Navigate to **All** &gt; **sys\_properties.list** &gt; **sn\_fsm\_disp\_wrkspc.enable\_optimize\_route** and set the value to true. This enables Route Optimization and displays **Optimize Route** option in the Dispatcher Workspace.
2.  To use route optimization features in the Dispatcher Workspace, do the following:
    -   Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** and ensure all configurations are made within the 'Field Service Management Configurable Dispatcher Workspace' application scope.
    -   Ensure the `sn_fsm_disp_wrkspc.enable_optimize_route` property is enabled.
    -   To optimize task bundles, enable the `Route Optimization for Bundles` \(work.management.travel.calculation.bundle\_route\_optimization\) property.

## Understanding Route Optimization Modes

You must select the work.management.optimization.conflict\_handling system property to avoid conflicts due to overflow tasks when optimizing the route. For more information, see [Properties installed with Field Service Management](../../planning-and-policy/reference/r_PropInstallWFieldServMgmnt.md).

Route optimization operates in three distinct modes, each designed to address specific scenarios:

1.  Optimize Within Shift: Reorders tasks within a single agent's shift to minimize travel time while respecting task time windows, scheduled breaks, and locked tasks.
2.  Extend Into Overtime: Adjusts tasks if an agent is running late, allowing overtime to ensure task completion.
3.  Cancel If Over Overtime: Attempts to optimize the route but cancels the operation if it would result in exceeding allowed overtime.

## Configuring additional options

Enhance route optimization with the following configuration options:

1.  Task constraints: Ensures all tasks remain within their start/end time windows \(if isFixedWindow = true\) and avoids moving locked tasks.
2.  Breaks &amp; Events: Schedule optimizations around planned breaks or personal events.
3.  Travel time estimates: Choose between using a Maps API for accurate travel time or straight-line estimates for faster calculations. Set up the Maps API key if opting for it.

## Customizing system properties

Customize route optimization to meet specific needs by configuring the following properties:

1.  Task-to-Task Time Buffer: Add a buffer of extra minutes between tasks to account for unexpected delays.
2.  Travel Time Calculation: Select between Maps API or straight-line estimates based on your accuracy needs.
3.  Default Work Hours: Define start and end times for agents without a fixed schedule.
4.  Travel Time Adjustments: Adjust travel times by adding percentages to account for uncertainties, such as rush hour.
5.  Rush Hour Timings: Specify morning and evening rush hour spans.
6.  Toll Road Option: Decide whether toll roads should be included in the route planning.

## Managing thresholds for task volume

The route optimization behavior adjusts based on the number of tasks:

-   Under 15 tasks: Complete route optimization is performed, considering all tasks and travel.
-   Over 200 tasks: Auto-routing fails, and an error message is displayed.
-   Partial Routing: If not all tasks can be accommodated, a smaller subset is optimized, and the remaining tasks revert to pending dispatch.

## Schedule job

The `Optimize Task Routing` job runs daily at 3:00 AM system time. Adjust this schedule based on your time zone or operational needs.

## Non-customizable client scripts

Client scripts for route optimization are pre-optimized and run within 4-6 seconds. These scripts should not be customized to ensure optimal performance.

