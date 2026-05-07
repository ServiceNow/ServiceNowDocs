---
title: Set the on-click behavior of a Core UI report
description: You can configure a URL to open when you select a section of a report.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Set the on-click behavior of a Core UI report

You can configure a URL to open when you select a section of a report.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## About this task

You can redirect users to a URL rather than to the configured drilldown or the list that underlies the selected section of a report.

See [Define a report drilldown](../concept/c_DrillingDownWithinReports.md#) for the report types that don't support the drilldown feature.

## Procedure

1.  Navigate to **All** &gt; **Reports**.

2.  Select the report that you want to configure.

3.  Select **View Report**.

4.  Select the **Show report structure** icon \(![Show report structure](../image/Form_ShowReportStructureIcon.png)\).

5.  Select the link icon \(![](../image/link-icon.png)\).

6.  In the **Set redirect URL** dialog box, enter a relative link within the instance, for example, `/$knowledge.do?sys_id=123`.

    When the user hovers over the report, the tooltip includes the text **Click to open**.

7.  Enter a label for the URL.

    When the user hovers over the report, the tooltip includes the text **Click to open** and the text of the label, for example, Click to open Knowledge Base.

8.  Select **Save**.

    ![Animation illustrating the steps to configure a report redirect to a URL](../image/report-config-redirect.gif)


## Result

When you select the report, the redirect URL replaces any drilldown functionality.

**Parent Topic:**[Advanced Core UI reporting topics](../concept/c_AdvancedReporting.md)

