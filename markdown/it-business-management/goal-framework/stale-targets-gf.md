---
title: Stale targets
description: A target with breakdowns becomes stale when its stored breakdowns no longer match the goal calendar. A stale target can't be changed until its check-in frequency is cleared.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/goal-framework/stale-targets-gf.html
release: australia
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 2
breadcrumb: [Managing stale targets, Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Stale targets

A target with breakdowns becomes stale when its stored breakdowns no longer match the goal calendar. A stale target can't be changed until its check-in frequency is cleared.

A goal target has breakdowns that split its value by period, for example by month, quarter, or fiscal period.

## When a target becomes stale

The following calendar changes can leave a target stale. These changes apply only when the target has breakdowns and its stored breakdowns no longer match the goal calendar set in the system property:

-   The goal calendar switches between Gregorian and fiscal.
-   The fiscal calendar type changes.
-   Fiscal periods are regenerated or deleted.

A target can also be stale when its check-in frequency is not supported by the calendar. For example, a target with a period frequency becomes stale after the calendar switches to Gregorian. A target whose frequency is supported by both calendars can also become stale when its breakdowns don't match the regenerated periods.

## What a stale target blocks

A stale target can't be changed. Its value and its structure are locked until the target is reset. The target form shows a message that explains the lock and asks the user to contact the administrator.

Targets that are stale are shown with locked rows and empty breakdown cells in the goals list.

## Targets that never become stale

A target with the check-in frequency set to **None** is never stale after a calendar change, because it has no breakdowns. A target with the legacy fortnightly frequency is never stale either. Milestones are not stale.

## How to clear a stale target

A stale target can be recovered in one of two ways: by running the reset job, or by duplicating the target. An administrator runs the scheduled job **Goal calendar alignment - Reset check-in frequency for stale targets**, which clears the check-in frequency of the stale targets. The owner then selects a frequency again, which rebuilds the breakdowns to match the calendar. Alternatively, a goal owner or target owner can duplicate the stale target and set a check-in frequency on the copy. The copy doesn't include the remarks, work notes, or history of the stale target. For reset steps, see [Reset the check-in frequency of stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/reset-stale-target-check-in-frequency.md).

**Parent Topic:**[Managing stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/managing-stale-targets-gf.md)

