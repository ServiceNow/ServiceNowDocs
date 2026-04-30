---
title: DevOps System Health dashboard
description: The System Health dashboard lets the DevOps administrator view the overall health of integrations, connectivity status, as well as view trends of inbound event processing data.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# DevOps System Health dashboard

The System Health dashboard lets the DevOps administrator view the overall health of integrations, connectivity status, as well as view trends of inbound event processing data.

Role required: sn\_devops.admin

**Note:** The DevOps System Health dashboard is available only in DevOps data model 1.33 and later versions.

Use the System Health dashboard to track the health, event status, and connectivity status of your DevOps environment. Interactive charts enable you to view and analyze the system health and inbound event processing details.

**Note:**

-   Scores aren’t real-time. For example, if the chart displays that two events are in the waiting state, the events could have already moved to the completed state.
-   Because the scores are fetched from formula indicators, you can’t drill down to the records in the KPI page.

![DevOps System Health Dashboard](../image/devops-system-health-dashboard.png "DevOps System Health Dashboard")

## Events

From the DevOps Change Workspace, navigate to **Administration** &gt; **System health** &gt; **System health dashboard**.

<table id="table_sv5_h3z_gsb"><thead><tr><th>

Report

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event count

</td><td>

Count trend

</td><td>

Daily trending total count of DevOps events. The report displays the percentage and count, which is the last 7 running sum.

 Total count includes events from \[sn\_devops\_inbound\_event\], \[sn\_devops\_event\], and the \[sn\_devops\_processed\_event\] tables.

</td></tr><tr><td>

Events by state

</td><td>

Pie chart

</td><td>

Total count DevOps events distributed by current state.

</td></tr><tr><td>

Events by tool

</td><td>

Pie chart

</td><td>

Total count of DevOps events, distributed by tool.

</td></tr><tr><td>

Retry count

</td><td>

Count trend

</td><td>

Daily trend of the count of total retried DevOps.The report displays the percentage and count variance in the last 24 hours.

</td></tr><tr><td>

Processed count

</td><td>

Count trend

</td><td>

Daily trend of the total count of processed DevOps events.The report displays the percentage and count variance in the last 24 hours.

</td></tr><tr><td>

Error count

</td><td>

Count trend

</td><td>

Daily trend of the total count of DevOps events in error state. The report displays the percentage and count variance in the last 24 hours.

</td></tr><tr><td>

Waiting count

</td><td>

Count trend

</td><td>

Daily trend of the total count of DevOps events in waiting state. The report displays the percentage and count variance in the last 24 hours.

</td></tr><tr><td>

Event trend

</td><td>

Line trend

</td><td>

Total trending count of DevOps events. The report displays the percentage and count variance in the last 24 hours.

</td></tr><tr><td>

Processing duration

</td><td>

Line trend

</td><td>

Processing duration of events \(in seconds\) measured daily.

</td></tr></tbody>
</table>## Tool connectivity

The Tool connectivity status report displays the connectivity status with details of all the integrated tools. The tool connectivity table displays the connection status for each connected tool. A background job tries to connect to the tools every hour and maintains the connection history. You can view the historical details under a new related list on the tools page.

To see the report, from the DevOps Change Workspace, navigate to **Administration** &gt; **System health** &gt; **Tool connectivity**.

![Tool connectivity list.](../image/system-health-tool-conn.png)

## System health email notifications

A base system DevOps Report group is added by default. An email notification summarizing the weekly System Health report is sent to the users in this DevOps Report user group that is specified in the **Who will receive** related list of the **System Notifications &gt; Email Notifications** form, as configured in the base system DevOps Health Report notification. For more information, see [Email notifications](https://www.servicenow.com/docs/access?context=c_EmailNotifications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Note:**

-   Add users with DevOps Admin \(sn\_devops.admin\) role to the DevOps Report user group.
-   You need to remove a user from the group to unsubscribe the user from receiving notifications.

The base-system email notification contains and displays a comparative digest of key system health performance indicators as compared to their performance in the previous weekly report. The comparative data is sourced from relevant tables and calculated based on required indicators using the date range specified in weekly report. The comparative data and indicators always display with respect to the same tables and indicators vis-a-vis, the data collected against the relevant reports and indicator data for the previous week.

To configure the frequency in which the base system email notification is sent out. Navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Trigger DevOps Health Check Email Notification** and select the **Configure Job Notification** related link, and make the schedule changes.

If you want to modify the users who receive the email notification, modify the user group specified in the **Groups** field of the **Who will receive** section. Navigate to **System Notification** &gt; **Email** &gt; **Notification** &gt; **DevOps Health Script**. For more information, see [Add a user to a group](https://www.servicenow.com/docs/access?context=t_AddAUserToAGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Use the **Preview Notification** option to check your notification.

For example, you can see which users will or will not receive the notification, along with what instance details and period for which the notification is sent.

![Preview for System health notification email](../image/system-health-email-notification-preview.png)

**Parent Topic:**[DevOps Change Velocity reference](../reference/devops-change-velocity-reference.md)

