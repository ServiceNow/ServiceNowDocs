---
title: Tables installed with FSM for Schedule Optimization
description: The following tables are installed with the Field Service Management plugin, but are only used by Schedule Optimization.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Schedule Optimization components, Field Service Management reference, Field Service Management]
---

# Tables installed with FSM for Schedule Optimization

The following tables are installed with the Field Service Management plugin, but are only used by Schedule Optimization.

<table id="table_hmx_41p_1yb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

\[Intraday Events\] wm\_intraday\_events

</td><td>

Captures agent/task events from the following pre-defined triggers:-   PTO submitted
-   Agent running late
-   Task canceled
-   New high priority task created

</td></tr><tr><td>

\[Intraday Jobs\] wm\_intraday\_jobs

</td><td>

-   Groups all the events for an individual qualifier and relates them to an optimization job
-   Maintains the state of the optimization job and task updates

</td></tr><tr><td>

\[Intraday Job Qualifier\] wm\_intraday\_job\_m2m\_qualifier

</td><td>

Relates a group or territory to an intraday job

</td></tr></tbody>
</table>**Parent Topic:**[Schedule Optimization components](schedule-optimization-components.md)

