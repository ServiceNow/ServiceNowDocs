---
title: Switch between fiscal calendars
description: Change the fiscal calendar type of the instance, for example from a standard fiscal calendar to a 4-4-5 calendar, and regenerate the fiscal periods.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/goal-framework/switch-between-fiscal-calendars.html
release: australia
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 2
audience: admin
breadcrumb: [Setting a goal calendar, Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Switch between fiscal calendars

Change the fiscal calendar type of the instance, for example from a standard fiscal calendar to a 4-4-5 calendar, and regenerate the fiscal periods.

## Before you begin

Role required: sn\_gf.goal\_admin

Plan for stale targets. Only targets with breakdowns can become stale. Plan to run the reset job after the switch.

## About this task

Switching the fiscal calendar type changes the periods that targets use. A target becomes stale when the check-in frequency periods of its breakdowns aren't supported by the goal calendar that is set in the system property. Targets without breakdowns don't become stale. The calendar mode stays as it is. For example, if the mode is `fiscal`, it remains `fiscal` after the switch.

## Procedure

1.  Set the fiscal calendar type.

    1.  Navigate to **All** &gt; **System Definition** &gt; **System Properties**.

    2.  Search for and open the **com.glide.fiscal\_calendar.fiscal\_calendar\_type** system property.

    3.  In the value field, choose one of the following values.

        -   `Regular`: the standard fiscal calendar.

        -   `445`: the 4-4-5 calendar.

        -   `13 Period`: the 13-period calendar.

2.  Set the fiscal unit for the new calendar type.

    1.  Navigate to **All** &gt; **System Definition** &gt; **System Properties**.

    2.  Search for and open the **com.glide.fiscal\_calendar.fiscal\_unit** system property.

    3.  For a 4-4-5 calendar, set the fiscal unit to 4-4-5 period.

3.  Check the fiscal year start day and start month, and change them if the fiscal year starts on a different date.

    These are stored in the **com.glide.fiscal\_calendar.fiscal\_year\_start\_day** and **com.glide.fiscal\_calendar.fiscal\_year\_start\_month** system properties.

4.  Regenerate the fiscal periods for the date range of your targets.

    Regenerating the periods replaces the existing fiscal periods with new ones. Targets that use the old periods become stale.

5.  Review the targets that became stale, and reset them.

    To clear them, see [Reset the check-in frequency of stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/reset-stale-target-check-in-frequency.md). Then ask the goal or target owners to select a check-in frequency again.


## Result

The instance uses the new fiscal calendar. Targets offer the check-in frequencies that the new calendar supports. Stale targets are reset, and their owners select a frequency again.

**Parent Topic:**[Setting a goal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/set-a-goal-calendar.md)

**Related topics**  


[Switch from the Gregorian calendar to a fiscal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/switch-from-gregorian-to-fiscal-calendar.md)

[Fiscal calendar support for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/fiscal-calendar-goal-framework.md)

