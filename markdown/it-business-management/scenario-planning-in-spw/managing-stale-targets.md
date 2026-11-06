---
title: Managing stale targets
description: Understand which targets become stale after a goal calendar change, and how to recover them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/scenario-planning-in-spw/managing-stale-targets.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 1
audience: [admin, user]
breadcrumb: [Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Managing stale targets

Understand which targets become stale after a goal calendar change, and how to recover them.

Only targets with breakdowns can become stale. A target becomes stale when its stored breakdowns no longer match the goal calendar set in the system property. This can happen when the check-in frequency isn't supported by the calendar, or when the breakdowns don't match the calendar's periods, for example after the calendar mode or the fiscal calendar type changes, or after the fiscal periods are regenerated or deleted. A target can become stale even when its check-in frequency is supported by both calendars. Targets without breakdowns, including those set to None, don't become stale when the goal calendar changes.

A stale target's values and structure are locked until it is recovered. To recover it, an administrator runs the scheduled job **Goal calendar alignment - Reset check-in frequency for stale targets**, which clears the check-in frequency of the stale targets. The target owner then selects a check-in frequency again. As an alternative to the reset job, a goal owner or target owner can duplicate the stale target and set a check-in frequency on the copy. The copy doesn't include the remarks, work notes, or history of the stale target.

For the definition, the locked actions, and the cases that aren't stale, see [Stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/stale-targets.md).

To run the reset job, see [Reset the check-in frequency of stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/reset-stale-targets-gfa.md).

-   **[Stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/stale-targets.md)**  
A target with breakdowns becomes stale when its stored breakdowns no longer match the goal calendar. A stale target can't be changed until its check-in frequency is cleared.
-   **[Reset the check-in frequency of stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/reset-stale-targets-gfa.md)**  
Clear the check-in frequency of stale targets in a date range after a goal calendar change, so that the owners can select a frequency again.

**Parent Topic:**[Configuring goals in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/configuring-goal-framework-apw.md)

