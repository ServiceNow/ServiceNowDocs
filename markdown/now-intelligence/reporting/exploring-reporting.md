---
title: Exploring reporting
description: Reporting functionality is available by default for all tables, except for system tables.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Exploring reporting

Reporting functionality is available by default for all tables, except for system tables.

## Reporting overview

**Note:** On net new Australia instances and instances migrated to Platform Analytics experience, Reporting functionality is replaced with Data Visualizations. For more information, see [Data visualizations in Platform Analytics](../../performance-analytics/concept/analytics-center-data-visualizations.md).

Core UI Reporting functionality is in maintenance mode and is no longer being augmented or changed. Only security fixes to this feature will be addressed.

The report\_admin role is required to create or edit reports, which may still be necessary in Service Portal, for example.

ServiceNow® enables you to create and distribute reports that show the current state of instance data, such as the number of open incidents of each priority.

## Reporting workflow

ServiceNow reports are visualizations of your data that you can share with users on dashboards and service portals, export to PDF, and email. Learn how to create, run, edit, view, and share reports.

## Reporting benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Run a report to view current data in an existing report.|[View a report](../../reporting/task/t_RunAReport.md#)|itil, report\_user, report\_group, report\_global, report\_admin, or admin|
|Create a report to visualize and analyze current instance data or temporary data that you have imported.|[Create a report](../../reporting/task/t_CreateYourOwnReport.md#)| |
|View a list of reports and create reports from the Reports list.|[View the Reports list](../../reporting/reference/r_ViewTheReportsList.md#)|admin|
|Users who cannot create their own global reports can modify a global report, and then save a personal version of the report.|[Copy a report](../../reporting/task/copy-report.md)|itil, report\_user, report\_group, report\_global, report\_admin, or admin|
|Delete reports that are no longer used.|[Delete a report](../../reporting/task/delete-report.md#)|creator, an administrator, or have a managing role of a report to delete|
|Keyboard shortcuts enable you to perform certain functions in the Report Designer without using your mouse.|[Report Designer keyboard shortcuts](../../reporting/reference/keyboard-shortcuts.md)| |

