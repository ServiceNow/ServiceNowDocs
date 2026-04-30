---
title: Portal Analyzer
description: Get a summary of all widgets that appear on Service Portal pages. Use this data to better understand widget customizations and page usage.Run a scheduled job to get a summary of all widgets that appear on pages.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using portal analytics, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Portal Analyzer

Get a summary of all widgets that appear on Service Portal pages. Use this data to better understand widget customizations and page usage.

The Portal Analyzer is a scheduled job that runs on-demand. After you select to run the Portal Analyzer job, the system produces a list of each widget and the page that it appears on.

The list also includes the following information:

-   Level of customization of each widget
-   Number of views on each page
-   Number of user visits on each page

You can export the list as a CSV, Excel, XML, JSON, or PDF file. Use the exported list to consider which pages and widgets to focus on while redesigning your portal. For example, you might consider removing a page that has less user visits or replacing a customized widget with a cloned widget.

The Portal Analyzer is active by default on your instance.

**Parent Topic:**[Using portal analytics](using-portal-analytics.md)

**Related topics**  


[Scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

## Run the Portal Analyzer

Run a scheduled job to get a summary of all widgets that appear on pages.

### Before you begin

Role required: admin or sp\_admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open the Portal Analyzer record.

3.  On the form header, select **Execute Now**.


### Result

The system creates a list of all the widgets on each page in your instance. You can view this list by entering `sp_portal_analyzer.list` in the application navigator.

### What to do next

Export the list as a CSV, Excel, XML, JSON, or PDF file to reference during a system upgrade. For more information on exporting list data, see [List export](https://www.servicenow.com/docs/access?context=export-list-data&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

