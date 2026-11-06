---
title: Switch from the Gregorian calendar to a fiscal calendar
description: Change the calendar mode of the instance from Gregorian to fiscal, so that targets use the fiscal periods of your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/scenario-planning-in-spw/switch-from-gregorian-to-fiscal-calendar-spw.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 2
audience: admin
breadcrumb: [Setting a goal calendar, Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Switch from the Gregorian calendar to a fiscal calendar

Change the calendar mode of the instance from Gregorian to fiscal, so that targets use the fiscal periods of your organization.

## Before you begin

Role required: sn\_gf.goal\_admin

Fiscal periods must exist for the date range of the targets. If they don't, generate them first.

## About this task

The calendar mode decides which check-in frequencies the form displays and how breakdowns are generated. The mode is stored in the **sn\_gfa.calendar\_type** system property.

Only targets with breakdowns can become stale. A target becomes stale when its stored breakdowns no longer match the goal calendar that is set in the system property. For example, a target with a Daily check-in frequency becomes stale after the switch to fiscal, because the fiscal calendar doesn't display Daily. Targets without breakdowns don't become stale when the goal calendar changes. See [Managing stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/managing-stale-targets.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **System Properties**.

2.  Search for and open the **sn\_gfa.calendar\_type** system property.

3.  In the **Value** field, set the value to `fiscal`, and save.

    The value is `gregorian` or `fiscal`. If the property is empty, the mode is Gregorian.

4.  Review the targets that became stale.

    Stale targets are locked until their check-in frequency is cleared. Clearing the check-in frequency with the reset job deletes all breakdowns of each stale target, and the total actual value is retained on the target form. The owner then selects a check-in frequency again to rebuild the breakdowns. To clear them, see [Reset the check-in frequency of stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/reset-stale-targets-gfa.md).


## Result

The instance uses fiscal periods. Resetting the stale targets deletes their breakdowns, and their total actual values are retained. The form displays only the check-in frequencies that the fiscal calendar type supports. For the values, see [Check-in frequency values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/check-in-frequency-values-spw.md).

**Parent Topic:**[Setting a goal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/set-a-goal-calendar-spw.md)

**Related topics**  


[Switch between fiscal calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/switch-between-fiscal-calendars-spw.md)

