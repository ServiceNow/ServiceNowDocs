---
title: Tables installed with FSM for Schedule Optimization
description: The following tables are installed with the Field Service Management plugin, but are only used by Schedule Optimization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/tables-installed-with-fsm-for-schedule-optimization.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Schedule Optimization components, Reference, Field Service Management]
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
</table>**Parent Topic:**[Schedule Optimization components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/schedule-optimization-components.md)

**Related topics**  


[Optimizing technician schedules at set intervals throughout the day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/optimize-your-schedules-intraday.md)

[Configure intraday optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/configure-intraday-optimization.md)

