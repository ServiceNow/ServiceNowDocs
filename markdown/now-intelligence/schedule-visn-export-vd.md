---
title: Schedule data visualization export
description: Automate the export and mailing of data visualizations. Help colleagues build presentations, share information with external users, or track data over time.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-05-20"
reading_time_minutes: 2
breadcrumb: [Export a visualization, Platform Analytics]
---

# Schedule data visualization export

Automate the export and mailing of data visualizations. Help colleagues build presentations, share information with external users, or track data over time.

## Before you begin

Role required: par\_scheduler, to schedule the export of any visualization that you created or that was shared with you. If you have the report\_scheduler, admin, or viz\_admin role, you can schedule the export of any data visualization.

To view the list of scheduled exports, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Scheduled Export**. This list contains all scheduled exports including Core UI dashboards and reports and Platform Analytics experience dashboards and data visualizations.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select the visualization that you want to export.

    **Note:** You cannot export calendar reports or indicator scorecards.

3.  From the More actions menu \(![Context menu icon](../../dashboards/image/icon-vert-3dot-p.png)\), select **Schedule**.

    ![Schedule option in More actions menu](../image/paw-vd-schedule.png)

4.  In the File to export section, specify the following information:

<table id="table_fsx_mlr_rwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File type

</td><td>

Export data visualizations in PDF, PNG, or JPEG format. Select **Embedded PNG** to embed a PNG in the email body instead of sending it as an attached file or ZIP. You can edit the email around the image.List - Simple visualizations can be exported as PDF or Excel files.

</td></tr><tr><td>

Page format

</td><td>

Select Letter, A4, or A3 to correspond to the paper dimensions of the printed visualization. If you are exporting a pivot table, you can select Dynamic to resize the visualization to the page being viewed.You cannot set page format for List - Simple visualizations.

</td></tr><tr><td>

Orientation

</td><td>

Choose Portrait or Landscape. You cannot select the orientation for Pivot tables with Dynamic format or for List - Simple visualizations.

</td></tr></tbody>
</table>5.  To include more visualizations in this scheduled email, select **+ Add file**.

6.  In the Email schedule section, specify when and how often to send the email.

<table id="table_schedule-export"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Turn on to enable delivery of scheduled reports.

</td></tr><tr><td>

Reoccurrence

</td><td>

Select how often to send the visualization.

</td></tr><tr><td>

Day, Time, other calendar fields

</td><td>

Specify when to send the email. Your options depend on how often you chose to send the email in **Reoccurrence**. Time fields are in HH:MM:SS format.

</td></tr><tr><td>

Omit if no records

</td><td>

Turn on to prevent the distribution of empty reports.

</td></tr><tr><td>

Use conditions

</td><td>

Turn on to specify a scripted condition for generating the report.

</td></tr><tr><td>

Condition

</td><td>

Conditional script that determines if a scheduled job should run. The last expression of the script should evaluate to a Boolean \(true/false\) value. This text box appears only if you select **Use conditions**. For more information about scripts on the ServiceNow platform, see [Scripts](https://www.servicenow.com/docs/access?context=c_Script&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).**Warning:** Conditional scripts for scheduled report emails are executed in the sandbox. Therefore, function definitions are not allowed. Some API calls and keywords are also not allowed. For more information, see [Script sandbox property](https://www.servicenow.com/docs/access?context=r_ScriptSandboxing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

</td></tr></tbody>
</table>7.  In the Email details section, specify the recipients and the email subject.

    You can enter users and groups on your instance or any permitted email addresses. Security constraints may restrict who you can send the report to. You can also add a message. To send emails to persons not on your instance, see [Outbound Email Configuration](https://developer.servicenow.com/dev.do#!/learn/courses/xanadu/app_store_learnv2_automatingapps_xanadu_automating_application_logic/app_store_learnv2_automatingapps_xanadu_notifications/app_store_learnv2_automatingapps_xanadu_outbound_email_configuration).

8.  To send non-embedded exports as ZIP files, turn on **Send as ZIP files**.

9.  Select **Save** to save the schedule or **Save and close** to return to the Visualization Designer.


**Parent Topic:**[Export a visualization from the Visualization Designer](export-visualization-vd.md)

