---
title: Manage Instance Observer alerts
description: Act on Instance Observer \(IO\) threshold alerts directly from the notification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/manage-io-alerts.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Alerts in Instance Observer, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Manage Instance Observer alerts

Act on Instance Observer \(IO\) threshold alerts directly from the notification.

## Before you begin

Role required: admin

## Procedure

1.  Open an alert threshold notification.

    The email notifications originate from ServiceNow and the subject is `New Alert`.

    \[Omitted image "io-alert-notification-email.png"\] Alt text: Shows a sample email with a threshold alert.

2.  Select the alert banner to be directed to the threshold chart in Instance Observer.

    \[Omitted image "io-threshold-chart.png"\] Alt text: Shows a threshold chart in Instance Observer with an explanation of the threshold alert when hovering over an alert indicator.

3.  Hover over an alert icon for general information about the anomaly.

4.  Select **Generate Root Cause** to open the Root cause correlation \(RCC\) history table.

5.  Select an entry to view the Summary of the root cause and metrics charts of where a potential issue may exist.

    -   \[Omitted image "io-RCC-report.png"\] Alt text: Shows the RCC summary report.

    -   \[Omitted image "io-metrics-charts.png"\] Alt text: Shows the metrics charts.

    -   The available menu options vary based on the type of root cause correlation.
6.  Sort the table by Created Date/Time to view the most recent entries chronologically.

7.  Drill into the impacted node to the affected job.

    \[Omitted image "io-impacted-job.png"\] Alt text: Shows the jobs for impacted nodes for the alert threshold notification.

8.  Select the job to open the job details with granular transaction and log information.

    \[Omitted image "io-job-details.png"\] Alt text: Shows the selected job details expanded with transaction and log information.

9.  For further investigation, select **Create a Case** and submit the captured summary information.


**Parent Topic:**[Alerts in Instance Observer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/io-alerts-intro.md)

