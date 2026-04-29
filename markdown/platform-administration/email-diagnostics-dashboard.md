---
title: Email diagnostics dashboard
description: The email diagnostics dashboards provide visibility in to email delivery metrics that can help in improving the email health by identifying errors and areas that need deeper investigation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email diagnostics dashboard

The email diagnostics dashboards provide visibility in to email delivery metrics that can help in improving the email health by identifying errors and areas that need deeper investigation.

To access Email diagnostics dashboard, navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Email notifications dashboard** &gt; **Diagnostics**.

Email diagnostics are available in a new tab within the Email Notifications dashboard for admins to track the following areas:

-   Bounce management
-   Email delivery metrics
-   SMTPSender jobs health
-   Error metrics and connection status

Data is displayed for the last six hours and can be refreshed at any time.

Email diagnostics overview 

## Analytics

Analytics provides comprehensive insights into the status and performance of your email metrics and enables you to monitor for all the email-related operations within your instance.

|UI component|Description|
|------------|-----------|
|Email status|Email status is the total count of emails in each status category within the email queue for the displayed time frame.|
|Bounce management|Bounce management shows the total number of hard and soft bounces received due to delivery failures within the displayed time frame.|
|Throughput rate|The average number of emails sent per minute during the displayed time frame.|
|Avg Latency per email|The average time taken to move emails from send-ready state to sent state within the displayed time frame.|
|Avg Job processing time|The average time taken by an SMTP sender job to complete the email processing within the displayed time frame.|
|Avg email sending time|The average time taken for an email to be relayed to the SMTP server within the displayed time frame.|

**Operational overview**

The operational overview gives the overview of email sending and reader operations for the displayed time and can be refreshed to fetch the latest updated status.

![operational overview of email diagnostics dashboard](../image/email-operational-overview.png "Operational overview")

**Queue overview**

Queue overview gives insights into all email records including the records pending for processing and their status.

![Queue overview for email diagnostics dashboard](../image/email-queue-overview.png "Queue overview")

|UI component|Description|
|------------|-----------|
|Emails in send-ready status|The number of emails that are ready to be picked up for processing.|
|Emails in retry status|Then number of emails that encountered delivery failures and are scheduled for reprocessing.|
|Emails cleared from the queue|The number of emails processed successfully during the displayed timeframe.|
|Avg Latency|The average time taken to process each email successfully and move it out of the queue.|
|Email creation trend|The trend of email records created in sys\_email table at various intervals.|
|Queue latency trend|The average latency trend at various intervals for all jobs within the displayed timeframe.|

**Job overview**

A Job Overview is a consolidated view that displays the status, performance, and metrics, giving administrators and users a quick insight into their operational state. Only processed jobs insights are displayed and jobs that are currently in execution are excluded.

![Job overview for email diagnostics dashboard](../image/email-job-overview.png "Job overview")

|UI component|Description|
|------------|-----------|
|Emails sent|The number of emails sent successfully within the displayed timeframe.|
|Jobs failed|Total number of jobs that failed during execution within the displayed timeframe.|
|Currently running job|Jobs currently in execution during the displayed timeframe \(real-time status\).|
|Job completed|Jobs that completed execution within the displayed timeframe.|
|Job processing avg time|Average time taken to process emails per job within the displayed timeframe.|
|Job processing max time|Maximum time taken by a job to process emails within the displayed timeframe.|
|Email processed trend|Displays the trend of emails processed by all sender jobs within the displayed timeframe.|
|Job latency trend|Displays the trend of average latency at various intervals for all jobs within the displayed timeframe.|

## Error log overview

Provides a quick, visual summary of all the errors occurrences, types, and trends to enable quick identification of issues.

|UI component|Description|
|------------|-----------|
|No. of errors|Displays total number of errors during the displayed timeframe.|
|Blocked email addresses|Count of email addresses that are blocked due to bounces during the displayed timeframe.|
|Hard bounce|Count of hard bounces within the displayed timeframe.|
|Soft bounce|Count of soft bounces within the displayed timeframe.|
|Top errors|Displays the top 5 errors with their counts within the displayed timeframe.|
|Bounce trend|Displays the hard and soft bounces received over the period displayed in the timeframe.|

**Error Log**

An error log captures and provides information about issues, failures, or unexpected events that occur within the instance.

## Connection status

![Connection status of configured email accounts](../image/email-connection-status.png "Connect status")

Connection status displays the real time status of all email accounts configured in an instance.

**Parent Topic:**[Email and SMS notifications](c_EmailNotifications.md)

**Related topics**  


[Create notification categories](../task/create-notification-categories.md)

[Create an email notification](../task/t_CreateANotification.md)

[Email notifications dashboard](email-notifications-dashboard.md)

[Email templates](c_EmailTemplates.md)

[Email layouts](email-layouts.md)

[Email retention](email-retention.md)

[Watermarks on notification emails](c_WorkingWithWatermarks.md)

[Parse an email thread](../task/parse-email.md)

[Email digests](email-digests.md)

[Domain separation and Notifications](domain-separation-notifications.md)

[Email FAQs and troubleshooting notification emails](troubleshooting-notification-emails.md)

