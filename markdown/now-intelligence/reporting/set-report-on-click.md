---
title: Set the on-click behavior of a Core UI report
description: You can configure a URL to open when you select a section of a report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/reporting/set-report-on-click.html
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Set the on-click behavior of a Core UI report

You can configure a URL to open when you select a section of a report.

## Before you begin

Role required:

-   When creating reports: Any
-   When editing reports created by others: report\_admin, report\_global, or report\_group

## About this task

Redirect the user to a URL rather than to the configured drilldown or the list that underlies the selected section of a report.

See [Define a report drilldown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/c_DrillingDownWithinReports.md) for the report types that don't support the drilldown feature.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Select the report that you want to configure.

3.  Select the **Show report structure** icon \(\[Omitted image "Form\_ShowReportStructureIcon.png"\] Alt text: Show report structure\).

4.  Select the link icon \(\[Omitted image "link-icon.png"\] Alt text:\).

5.  In the **Set redirect URL** dialog box, enter relative link within the instance, for example, `/$knowledge.do?sys_id=123`.

    When the user points to the report, the tooltip includes the text **Click to open**.

6.  Enter a label for the URL.

    When the user points to the report, the tooltip includes the text **Click to open** and the text of the label, for example, Click to open Knowledge Base.

7.  Select **Save**.

    \[Omitted image "report-config-redirect.gif"\] Alt text: Animation illustrating the steps to configure a report redirect to a URL


## Result

When you select the report, the redirect URL replaces any drilldown functionality.

**Parent Topic:**[Advanced Core UI reporting topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/reporting/c_AdvancedReporting.md)

