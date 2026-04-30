---
title: Manage Instance Observer alerts
description: Act on Instance Observer \(IO\) threshold alerts directly from the notification.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Alerts in Instance Observer, Overview of Instance Observer, Platform Health, Using Impact, Impact]
---

# Manage Instance Observer alerts

Act on Instance Observer \(IO\) threshold alerts directly from the notification.

## Before you begin

Role required: admin

## Procedure

1.  Open an alert threshold notification.

    The email notifications originate from ServiceNow and the subject is `New Alert`.

    ![Shows a sample email with a threshold alert.](../image/io-alert-notification-email.png)

2.  Select the alert banner to be directed to the threshold chart in Instance Observer.

    ![Shows a threshold chart in Instance Observer with an explanation of the threshold alert when hovering over an alert indicator.](../image/io-threshold-chart.png)

3.  Hover over an alert icon for general information about the anomaly.

4.  Select **Generate Root Cause** to open the Root cause correlation \(RCC\) history table.

5.  Select an entry to view the Summary of the root cause and metrics charts of where a potential issue may exist.

    -   ![Shows the RCC summary report.](../image/io-RCC-report.png "Summary of the root cause correlation chart")

    -   ![Shows the metrics charts.](../image/io-metrics-charts.png "Metrics charts")

    -   The available menu options vary based on the type of root cause correlation.
6.  Sort the table by Created Date/Time to view the most recent entries chronologically.

7.  Drill into the impacted node to the affected job.

    ![Shows the jobs for impacted nodes for the alert threshold notification.](../image/io-impacted-job.png)

8.  Select the job to open the job details with granular transaction and log information.

    ![Shows the selected job details expanded with transaction and log information.](../image/io-job-details.png)

9.  For further investigation, select **Create a Case** and submit the captured summary information.


