---
title: Schedule the export of data visualizations or dashboards
description: Automate the export and mailing of data visualizations. Help colleagues build presentations, share information with external users, or track data over time.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Share, edit, or delete, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Schedule the export of data visualizations or dashboards

Automate the export and mailing of data visualizations. Help colleagues build presentations, share information with external users, or track data over time.

## Before you begin

Role required:

-   par\_scheduler, or any role that contains it, to create or edit the scheduled export of any dashboard or visualization that you can access.
-   sn\_par\_sche\_export.par\_scheduler\_admin to delete the scheduled export of a dashboard or data visualization.
-   viz\_admin to create, update, or delete the scheduled export of any data visualization on the instance
-   dashboard\_admin to create, update, or delete the scheduled export of any dashboard on the instance.

To view the list of scheduled exports, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Scheduled Export**. This list contains all scheduled exports including Core UI dashboards and reports and Platform Analytics experience dashboards and data visualizations. You can also access the Scheduled exports using the left navigation pane.

## About this task

You can export multiple dashboards and data visualizations together in one scheduled email. Supported export formats depend on what you are exporting and whether you are exporting it as part of a dashboard or as a standalone data visualization.

|Data visualization or dashboard element|Supported dashboard export formats|Supported data visualization export formats|
|---------------------------------------|----------------------------------|-------------------------------------------|
|Calendar reports, Indicator scorecards, Pivot tables, Geomap|None|None|
|Lists|PDF|PDF, Microsoft Excel \(.xls or .xlsx\), Embedded LIST, CSV|
|Other data visualizations|PowerPoint, PDF|PowerPoint, PDF, PNG, JPEG, Embedded PNG|
|Non-data visualization dashboard elements, like Headings|None|Not applicable|

**Note:** This topic is available in both the Dashboard and the Data Visualization documentation.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** and select **Data Visualizations** or **Dashboards**.

2.  Select an item that you want to export on a regular schedule.

    Check the list of supported export formats under **About this task**.

3.  From the More actions menu \(![More actions menu icon](../../../administer/integrationhub/images/more-actions-menu-icon.png)\), select **Schedule**.

    You cannot be in Edit mode.

    ![Schedule option in More actions menu](../image/paw-vd-schedule.png)

    All the options appear for exporting the dashboard or data visualization. If you do not want to export this object, select **Change**.

4.  Select the file type.

5.  If you are exporting a dashboard or data visualization to PDF, or a data visualization to a graphic file, select the page format and orientation.

    Scheduled exports of List data visualizations to PDF do not have options for page format or orientation. If you need a PDF with a particular format or orientation, consider putting the List on a dashboard and scheduling the export of that dashboard, instead.

6.  If you are exporting a dashboard to Power Point, do the following steps:

    1.  Select whether to export all tabs or only specific tabs.

    2.  If you select to export only specific tabs, select which tabs to export and whether to include the top layout contents.

        ![Export configuration for one tab and the top level visualizations.](../image/sched-exp-by-tab.png "Configuring the export of dashboard tabs")

        For example, if you do not turn on **Export all tabs**, you have to select the tabs to export. If you select a tab and turn on **Export all visualizations in the top layout**, you export that tab and any visualizations placed above the tabs.

        ![Tab and top level visualizations that are exported.](../image/sched-exp-top-and-tab.png "The visualizations that are exported")

7.  To add more dashboards or data visualizations to the export, do the following steps:

    1.  Expand the **Add** menu.

    2.  Select **Dashboard** or **Data visualization**.

    3.  Choose one or more dashboards or visualizations to export.

    4.  Configure the export criteria for each added dashboard or visualization as in Steps 4-6.

    You can add both dashboards and data visualizations to a single export.

8.  To send non-embedded exports as ZIP files, turn on **Send as ZIP files**.

9.  In the Email schedule section, specify when and how often to send the email.

<table id="table_schedule-export"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Turn on to enable delivery of scheduled export emails.

</td></tr><tr><td>

Reoccurrence

</td><td>

Select how often to send the export email.

</td></tr><tr><td>

Day, Time, other calendar fields

</td><td>

Specify when to send the email. Your options depend on how often you chose to send the email in **Reoccurrence**. Time fields are in HH:MM:SS format.

</td></tr><tr><td>

Omit if no records

</td><td>

Turn on to prevent the distribution of empty emails.

</td></tr><tr><td>

Use conditions

</td><td>

Turn on to specify a scripted condition for generating the report.

</td></tr><tr><td>

Condition

</td><td>

A conditional script that determines if a scheduled job should run. The last expression of the script should evaluate to a Boolean \(true/false\) value. This text box appears only if you select **Use conditions**. For more information about scripts on the ServiceNow AI Platform®, see Scripts.**Warning:** Conditional scripts for scheduled emails are executed in the sandbox. Therefore, function definitions are not allowed. Some API calls and keywords are also not allowed. For more information, see Script sandbox property.

</td></tr></tbody>
</table>10. In the Email details section, specify the recipients and the email subject.

    You can enter users and groups on your instance or any permitted internal or external email addresses. Security constraints may restrict who you can send the report to. You can also add a message. To send email to persons who are not on your instance, you need to have outbound email configured. See [Outbound Email Configuration](https://developer.servicenow.com/dev.do#!/learn/courses/xanadu/app_store_learnv2_automatingapps_xanadu_automating_application_logic/app_store_learnv2_automatingapps_xanadu_notifications/app_store_learnv2_automatingapps_xanadu_outbound_email_configuration).

11. Select **Save** to save the schedule.


**Parent Topic:**[Common data visualization tasks](../../reporting/concept/common-dv-tasks.md)

