---
title: Check-in frequency values
description: The check-in frequency of a target sets how often its actual value must be updated. This reference lists each value and when it is displayed on the target form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/scenario-planning-in-spw/check-in-frequency-values-spw.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2026-10-28"
reading_time_minutes: 1
audience: [admin, user]
breadcrumb: [Reference, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Check-in frequency values

The check-in frequency of a target sets how often its actual value must be updated. This reference lists each value and when it is displayed on the target form.

## Values

|Label|Stored value|Gregorian mode|Fiscal mode|
|-----|------------|--------------|-----------|
|Daily|daily|Displayed|Not displayed|
|Weekly|weekly|Displayed|Displayed only when the fiscal calendar generates weeks|
|Period|period|Not displayed|Displayed. A quad week in a 13-period calendar, or a 4-4-5 period in a 4-4-5 calendar|
|Monthly|monthly|Displayed|Displayed for a standard fiscal calendar|
|Quarterly|quarterly|Displayed|Displayed for a standard fiscal calendar and a 4-4-5 calendar|
|Yearly|yearly|Displayed|Displayed|

## When the Period value is available

The Period value is displayed on the target form only when a release of Goal Framework Advanced that supports fiscal periods is installed. Without that release, the Period option is removed from the form. A target that already has the Period value keeps it, so the value doesn't show as blank.

When the calendar mode is Gregorian, a target that has breakdowns and the Period value becomes stale. Change its check-in frequency to a value that the calendar displays, or run the reset job. See [Stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/stale-targets.md).

## Legacy values

Targets that were given the fortnightly value before it was removed from the field can still have it. The value isn't displayed on the form. Targets that have it are never stale.

**Parent Topic:**[Strategic Planning Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/alignment-planner-workspace-reference.md)

