---
title: Fiscal calendar support for targets
description: With fiscal calendar support, the check-in frequency of a target follows the fiscal periods of your organization instead of the Gregorian calendar.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/goal-framework/fiscal-calendar-goal-framework.html
release: australia
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 2
breadcrumb: [Explore, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Fiscal calendar support for targets

With fiscal calendar support, the check-in frequency of a target follows the fiscal periods of your organization instead of the Gregorian calendar.

Targets can break down their values by Gregorian periods or by the periods of a fiscal calendar. The calendar mode is set for the whole instance. When the mode is fiscal, the form displays the check-in frequencies that the calendar type supports, and the breakdowns that a target generates follow the fiscal periods.

## How the calendar mode is set

The calendar mode is stored in the **sn\_gfa.calendar\_type** system property. The value is `gregorian` or `fiscal`. If the property is not set, the mode is Gregorian.

The **sn\_gfa.calendar\_type** system property is separate from the older **sn\_gf.goal\_calendar\_type** system property. Changing the calendar mode can make targets with breakdowns stale when their stored breakdowns no longer match the calendar, even when their check-in frequency is supported by both calendars. A stale target can be recovered by running the reset job or by duplicating the target. The copy doesn't include the remarks, work notes, or history of the stale target. For more information, see [Stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/stale-targets.md).

## Check-in frequencies in fiscal mode

In fiscal mode, the form displays only the check-in frequencies that the fiscal calendar type supports. Each frequency maps to a fiscal period type:

-   Yearly maps to the fiscal year.
-   Quarterly maps to a fiscal quarter. In a 4-4-5 calendar, it maps to the 4-4-5 quarter.
-   Monthly maps to a fiscal month.
-   Period maps to a quad week in a 13-period calendar, or to a 4-4-5 period in a 4-4-5 calendar.

The calendar type decides which frequencies are displayed:

-   A standard fiscal calendar displays yearly, quarterly, and monthly.
-   A 13-period calendar displays yearly and period.
-   A 4-4-5 calendar displays yearly, quarterly, and period.

Weekly is displayed for any fiscal calendar that generates weeks. In fiscal mode, a new target defaults to the most detailed check-in frequency that the fiscal calendar provides, excluding weekly. For a standard fiscal calendar, the default is monthly. For a 13-period or 4-4-5 calendar, the default is period. In Gregorian mode, a new target has no default frequency.

## When saving and breakdown generation are blocked

All check-in frequencies that the calendar type supports are always displayed. The fiscal calendar must fully cover the start and end dates of the target at every level of the selected frequency. If the calendar has a gap or an overlap in the target's date range, or if a parent period is missing, the target can't be saved with that frequency, and its breakdowns aren't generated.

When a save is blocked, the user sees a message that explains the cause. Depending on the cause, the message asks the user to choose a different frequency, to adjust the target dates, or to contact the administrator.

**Related topics**  


[Managing stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/managing-stale-targets-gf.md)

[Setting a goal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/set-a-goal-calendar.md)

