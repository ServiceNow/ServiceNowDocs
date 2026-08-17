---
title: Actual and business elapsed times
description: Task SLA records contain two sets of timing information: Actual elapsed and Business elapsed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/service-level-management/r\_ElapsedTimeCounting.html
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2026-07-22"
reading_time_minutes: 2
breadcrumb: [Service Level Agreement \(SLA\) processing, Explore, Service Level Management, IT Service Management]
---

# Actual and business elapsed times

Task SLA records contain two sets of timing information: Actual elapsed and Business elapsed.

The difference between these two sets of timing is vital when you create and report on SLA definitions.

-   **Actual elapsed** values are calculated on a 24x7 basis.
-   **Business elapsed** values are calculated based on the schedule specified in the task SLA. The schedule is taken from the SLA definition by default.

    **Note:** If no schedule is specified, then the **Business elapsed time** is the same as the **Actual elapsed time**. This can be disabled by changing the **com.snc.sla.always\_populate\_business\_fields** property to false in the SLA Engine. When this property is set to false, the **Business** fields will be 0 or empty.


By default, the related list for the task SLA record displays the actual elapsed time only. You can configure the list to also display the business elapsed time.

## Elapsed times and schedules

Consider a scenario where an SLA has a defined schedule of 9 am to 5 pm on weekdays. With this schedule, the difference between actual and business elapsed times can be significant.

If a task SLA starts at 2 p.m. on a weekday, by 9 a.m. the next weekday it shows 3 business hours and 19 actual hours.

\[Omitted image "SLM\_ElapsedTimes.png"\] Alt text: Actual elapsed time and business elapsed time within actual

If a schedule defines an 8-hour working day, 24 hours of business elapsed time equals 3 days of actual elapsed time.

## Example

For example, an incident is opened on Friday, December 12 at 9 pm, outside of the SLA schedule of 8 am to 5 pm on weekdays.

If the current time is the following Monday at 9:30 am, then:

-   **Business elapsed time** is 1 hour and 30 minutes because the SLA business timer stopped at 5 pm on Friday and restarted at 8 am on Monday.
-   **Actual elapsed time** is 60 hours and 30 minutes, representing the real-time between the incident being opened and the current time.

Elapsed percentages are also similarly calculated. The actual elapsed percentage is over 750% while the business elapsed percentage is 19% on an 8 hour SLA.

## How the SLA workflow uses business elapsed percentage

The SLA workflow uses the SLA Percentage Timer activity to trigger notifications at defined thresholds — for example, at 50% and 75% of the SLA duration. These thresholds are calculated using Business elapsed time.

When a timer fires, the SLA workflow evaluates how much business elapsed time has been consumed against the total SLA duration \(as defined in the SLA definition's schedule\). The timer does not advance while the SLA schedule is inactive — for example, overnight or on weekends.

For example, on an 8-hour SLA with a 9 a.m. to 5 p.m. weekday schedule:

-   **50% threshold**

    The 50% timer fires after 4 hours of business elapsed time — regardless of how many wall-clock hours have passed.

-   **Example timing**

    If the SLA starts at 4 p.m. on Monday, the 50% timer fires at 10 a.m. on Tuesday, after the overnight gap is excluded.


This confirms that notifications and escalations reflect actual working time, not calendar time.

**Parent Topic:**[Service Level Agreement \(SLA\) processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-level-management/c_SLAProcessing.md)

**Related topics**  


[SLA Percentage Timer workflow activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/r_SLAPercentageTimer.md)

[Flows for SLA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-level-management/flows-for-sla.md)

