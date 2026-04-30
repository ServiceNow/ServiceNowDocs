---
title: Report statistics
description: The Report Stats list enables you to view how often each of your Core UI reports is run and how long it takes for the reports to run.The Reports Usage dashboard provides an overview of how reports are used in a ServiceNow instance or domain.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Report statistics

The **Report Stats** list enables you to view how often each of your Core UI reports is run and how long it takes for the reports to run.

To view report statistics, navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Report Statistics**. The admin or report\_admin role is required. By default, the Report Statistics list displays all reports that have been run. To view reports that haven't been run, select the context menu icon \(![Context menu icon](../image/ContextMenuIcon.png)\) and choose **Add Unused Reports**.

**Note:** Adding unused reports to this list takes some time, especially if your instance has many reports.

Overview and suggestions on how to manage reports within the ServiceNow environment.

The **Report Stats** list has the following columns:

|Column|Description|
|------|-----------|
|Report|The name of the report. Select the hyperlink to view the report properties.|
|Last run|The date and time the report was last run.|
|Runs|The number of times the report has ever been run.|
|Runs on page|The number of times the report has been run on a dashboard.|
|Recent run time|The average execution time of the report in milliseconds based on the 25 most recent runs. Edit the **glide.report.recent\_executions\_number** property to change the number of runs used to calculate this value.|
|Run time|The average execution time in milliseconds of all runs of the report.|
|Recent number executions|The number of time the report was recently loaded from the server. The maximum number of recent executions is determined by the property **glide.report.recent\_executions\_number**.|

-   To view the reports that take the most time to run, sort **Recent run time** from z-a.
-   To view used reports, filter out the value 0 from the **Runs** column.
-   To view the most used reports, sort the **Runs** column from z-a.

**Parent Topic:**[Administering reports](c_AdminsteringReports.md)

## Reports Usage dashboard

The Reports Usage dashboard provides an overview of how reports are used in a ServiceNow instance or domain.

To view report statistics, navigate to **Performance Analytics** &gt; **Admin Console** and select **Report Usage** on the Usage tile.

**Note:** The report\_admin role cannot view this console. The admin or pa\_admin role is required.

The Reports Usage dashboard shows the following widgets:

|Widget|Type|Description|
|------|----|-----------|
|Number of Reports|Single Score with percentage change month on month.|The number of reports in the instance. Click the score to view a dashboard with chart and lists of breakdowns, records, and scores.|
|% Reports not viewed in the last 6 months|Single Score with percentage change month on month.|The percentage of reports in the domain or instance that have not been viewed in the last six months. Click the score to view a detailed dashboard with a chart on which you can adjust the period, the calculation used, and additional information on the report.|
|Top 10 Report Tables|List|A list of the top 10 tables used in reports. Point to the name of a table to read its description. Click the name of the table or the number of reports to show a dashboard with an enlarged chart, a list of the records in the table, the scores, and additional information on the report.|
|Reports by Visualization type|Bar chart \(with option to change the visualization to one of several other report types\)|The number of times the report has been run on dashboard. Click a report segment to show a dashboard with an enlarged chart, a list of the records in the table, the scores, and additional information on the report.|

