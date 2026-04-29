---
title: Actual and business elapsed times
description: Task SLA records contain two sets of timing information: Actual elapsed and Business elapsed.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Level Agreement \(SLA\) processing, Exploring Service Level Management, Service Level Management, IT Service Management]
---

# Actual and business elapsed times

Task SLA records contain two sets of timing information: **Actual elapsed** and **Business elapsed**.

The difference between these two sets of timing is vital when you create and report on SLA definitions.

-   **Actual elapsed** values are calculated on a 24x7 basis.
-   **Business elapsed** values are calculated based on the schedule specified in the task SLA. The schedule is taken from the SLA definition by default.

    **Note:** If no schedule is specified, then the **Business elapsed time** is the same as the **Actual elapsed time**. This can be disabled by changing the **com.snc.sla.always\_populate\_business\_fields** property to false in the SLA Engine. When this property is set to false, the **Business** fields will be 0 or empty.


By default, the related list for the task SLA record displays the actual elapsed time only. You can configure the list to also display the business elapsed time.

## Elapsed times and schedules

Consider a scenario where an SLA has a defined schedule of 9 am to 5 pm on weekdays. With this schedule, the difference between actual and business elapsed times can be significant.

For example, if a task SLA starts at 2 pm on a weekday, its business elapsed time at 9 am on the next weekday is 3 hours while its actual elapsed time is 19 hours.

![Actual elapsed time and business elapsed time within actual](../image/SLM_ElapsedTimes.png "Business elapsed time vs actual elapsed time")

In addition, if a schedule defines an 8 hour working day, then 24 hours or one day in business elapsed time equates to 3 days in actual elapsed time.

![24 by 7 actual elapsed time example](../image/ActualAndBusinessTimeExample2.png "Exampl of business and actual elapsed times - 24 X 7")

## Example

For example, an incident is opened on Friday, December 12 at 9 pm, outside of the SLA schedule of 8 am to 5 pm on weekdays.

If the current time is the following Monday at 9:30 am, then:

-   **Business elapsed time** is 1 hour and 30 minutes because the SLA business timer stopped at 5 pm on Friday and restarted at 8 am on Monday.
-   **Actual elapsed time** is 60 hours and 30 minutes, representing the real time between the incident being opened and the current time.

Elapsed percentages are also similarly calculated. The actual elapsed percentage is over 750% while the business elapsed percentage is 19% on an 8 hour SLA.

**Parent Topic:**[Service Level Agreement \(SLA\) processing](../concept/c_SLAProcessing.md)

