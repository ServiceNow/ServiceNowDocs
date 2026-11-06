---
title: Set the on-click behavior of a Core UI report
description: You can configure a URL to open when you select a section of a report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/reporting/set-report-on-click.html
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Advanced Core UI reporting topics, Core UI Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Set the on-click behavior of a Core UI report

You can configure a URL to open when you select a section of a report.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## About this task

**Note:** This topic refers to Core UI reports, not Platform Analytics data visualizations.

Redirect the user to a URL rather than to the configured drilldown or the list that underlies the selected section of a report.

See [Define a report drilldown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/reporting/c_DrillingDownWithinReports.md) for the report types that don't support the drilldown feature.

## Procedure

1.  Open the report you want to configure.

2.  Select the **Show report structure** icon \(\[Omitted image "Form\_ShowReportStructureIcon.png"\] Alt text: Show report structure\).

3.  Select the link icon \(\[Omitted image "link-icon.png"\] Alt text:\).

    \[Omitted image "set-redirect-url.png"\] Alt text: Set redirect URL link button

4.  In the **Set redirect URL** dialog box, enter relative link within the instance, for example, `/$knowledge.do?sys_id=123`.

    When the user points to the report, the tooltip includes the text **Click to open**.

5.  Enter a label for the URL.

    When the user points to the report, the tooltip includes the text **Click to open** and the text of the label, for example, Click to open Knowledge Base.

6.  Select **Save**.


## Result

When you select the report, the redirect URL replaces any drilldown functionality.

**Parent Topic:**[Advanced Core UI reporting topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/reporting/c_AdvancedReporting.md)

