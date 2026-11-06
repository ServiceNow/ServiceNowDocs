---
title: Switch from the Gregorian calendar to a fiscal calendar
description: Change the calendar mode of the instance from Gregorian to fiscal, so that targets use the fiscal periods of your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/goal-framework/switch-from-gregorian-to-fiscal-calendar.html
release: australia
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 2
audience: admin
breadcrumb: [Setting a goal calendar, Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Switch from the Gregorian calendar to a fiscal calendar

Change the calendar mode of the instance from Gregorian to fiscal, so that targets use the fiscal periods of your organization.

## Before you begin

Role required: sn\_gf.goal\_admin

Fiscal periods must exist for the date range of the targets. If they don't, generate them first.

## About this task

The calendar mode decides which check-in frequencies targets offer and how their breakdowns are generated. The mode is stored in the **sn\_gfa.calendar\_type** system property.

Only targets with breakdowns can become stale. A target becomes stale when the check-in frequency periods of its breakdowns aren't supported by the goal calendar that is set in the system property. For example, a target with a Daily check-in frequency becomes stale after the switch to fiscal, because the fiscal calendar doesn't offer Daily. Targets without breakdowns don't become stale when the goal calendar changes. See [Managing stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/managing-stale-targets-gf.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **System Properties**.

2.  Search for and open the **sn\_gfa.calendar\_type** system property.

3.  In the **Value** field, set the value to `fiscal`, and save.

    The value is `gregorian` or `fiscal`. If the property is empty, the mode is Gregorian.

4.  Review the targets that became stale.

    Stale targets are locked until their check-in frequency is cleared. Clearing the check-in frequency with the reset job deletes all breakdowns of each stale target, and the total actual value is retained on the target form. The owner then selects a check-in frequency again to rebuild the breakdowns. To clear them, see [Reset the check-in frequency of stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/reset-stale-target-check-in-frequency.md).


## Result

The instance uses fiscal periods. Targets offer only the check-in frequencies that the fiscal calendar supports. For the details, see [Fiscal calendar support for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/fiscal-calendar-goal-framework.md).

**Parent Topic:**[Setting a goal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/set-a-goal-calendar.md)

**Related topics**  


[Switch between fiscal calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/switch-between-fiscal-calendars.md)

