---
title: Export target breakdowns
description: Optionally, export target breakdowns before you switch or set a goal calendar, so that you have a record of them after the change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/scenario-planning-in-spw/export-target-breakdowns.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-11-17"
reading_time_minutes: 1
breadcrumb: [Setting a goal calendar, Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Export target breakdowns

Optionally, export target breakdowns before you switch or set a goal calendar, so that you have a record of them after the change.

## Before you begin

Role required: sn\_gf.goal\_admin or sn\_gf.goal\_user

## About this task

This task is optional. Export the target breakdowns before you change the goal calendar, or before you run the reset job. The reset job deletes all existing breakdowns of the stale targets, while the total actuals stay on the main target form. The export keeps a record of the breakdowns that you can use to check any discrepancy in the stale targets after the change.

For the reset job, see [Reset the check-in frequency of stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/reset-stale-targets-gfa.md).

## Procedure

1.  Navigate to **All**, enter `sn_gfa_target_breakdown.list`, and press Enter.

    The list of target breakdowns appears.

2.  To include the target for each breakdown, select the **Update Personalized List** \(\[Omitted image "cp-personalize-option.png"\] Alt text:\) icon, and then add the **Target** field to the selected columns.

    \[Omitted image "export-target-breakdowns1.png"\] Alt text: The Personalize list icon and the Target field in the selected columns.

3.  Right-click any field on the header, and then select **Export** &gt; **Excel \(.xlsx\)**.

    A popup window appears with the export progress.

    \[Omitted image "export-target-breakdowns2.png"\] Alt text: The export progress popup window.

4.  Select **Download** to save the exported Excel workbook.

    \[Omitted image "export-target-breakdowns3.png"\] Alt text: The Download option in the export popup window.


## Result

You have an Excel workbook with the target breakdowns from before the change. Keep it until you have checked the stale targets after the change.

**Parent Topic:**[Setting a goal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/set-a-goal-calendar-spw.md)

**Related topics**  


[Switch from the Gregorian calendar to a fiscal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/switch-from-gregorian-to-fiscal-calendar-spw.md)

[Switch between fiscal calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/switch-between-fiscal-calendars-spw.md)

