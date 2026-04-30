---
title: Get a list of widgets per page
description: Get a summary of all widgets that appear on Service Portal pages. Use this data to better understand widget customizations and page usage.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Analyzing portal performance and usage, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Get a list of widgets per page

Get a summary of all widgets that appear on Service Portal pages. Use this data to better understand widget customizations and page usage.

## Before you begin

Role required: sp\_admin or admin

## About this task

The Portal Analyzer is a scheduled job that runs on-demand. After you select to run the Portal Analyzer job, the system produces a list of each widget and the page that it appears on.

The list also includes the following information:

-   Level of customization of each widget
-   Number of views on each page
-   Number of user visits on each page

Use the exported list to consider which pages and widgets to focus on while redesigning your portal. For example, you might consider removing a page that has fewer user visits or replacing a customized widget with a cloned widget.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the Portal Analyzer record.

3.  On the form header, select **Execute Now**.

    The system creates a list of all the widgets on each page in your instance.

4.  In the navigation filter, enter `sp_portal_analyzer.list`.

5.  Review the list and, if needed, export it as a CSV, Excel, XML, JSON, or PDF file to reference during a system upgrade.

    For more information on exporting list data, see [List export](https://www.servicenow.com/docs/access?context=export-list-data&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).


**Parent Topic:**[Analyzing portal performance and usage](using-portal-analytics.md)

**Related topics**  


[Scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

