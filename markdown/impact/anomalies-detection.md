---
title: Anomalies detection
description: Instance Observer proactively detects the anomalies for cyclical or non-cyclical metrics under the performance chart for the Impact Total package on production instances. Anomalies represent metrics outliers based on historical patterns. Every anomaly may not represent an issue, but, notifies you and you decide the criticality and configure alerts, accordingly.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Performance, Impact Instance Observer, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Anomalies detection

Instance Observer proactively detects the anomalies for cyclical or non-cyclical metrics under the performance chart for the Impact Total package on production instances. Anomalies represent metrics outliers based on historical patterns. Every anomaly may not represent an issue, but, notifies you and you decide the criticality and configure alerts, accordingly.

Cyclical metrics occur as a complete set of events that repeat themselves regularly in the same order or in a regularly repeated period. Non-cyclical metrics are metrics that repeat themselves irregularly or in random, less predictable repeated periods. An anomaly, also known as an outlier, is a data point that is unusual, rare, or doesn't conform to the expected patterns or distribution of the data.

There are five cyclical metrics being tracked:

-   **Transaction count**: The instance-wide sum of all UI transactions of an internal type known as UI\_TYPE.
-   **Server Response Time**: The average or mean execution time for UI\_TYPE transactions.
-   **SQL Response Time**: The reported mean of database response time measured at the application layer that starts when a query is sent to the database and finishes when the response has been received.
-   **Semaphore Mean**: The average number of end-user transactions being processed concurrently over a one-minute period.
-   **Node Memory Max**: The in use memory max in MB per node at a given data point in history. This value generally ranges between 1000 MB to 2048 MB.

![Anomalies tab chart](../image/io-anomalies-tab-chart.png)

-   The x-axis represents time, and the y-axis represents the actual metrics as per date range selected. For example, the line chart displays the transaction count values over time. Anomalies are denoted by red color coding on the chart and represent the occurrence of an anomaly in the data. The placement of the red mark depends on the criteria or algorithm used to detect anomalies.
-   The range represents the upper and lower boundary limits with a normal distribution of the metrics based on their historical dataset pattern.
-   The mean line represents the four week average value of the metrics to compare the deviation at a given point in time.

## Job anomaly detection

Job anomaly charts track the number of scheduled jobs running concurrently for each hour of the day with the overlaying metric of the average of transaction counts for each hour. Any bar in the chart that has one or multiple anomalous jobs is highlighted as red. Select the detail link of the bar chart to view the job level details.

Job Details will represent the hourly scheduled jobs along with respective average transactions of that instance.

![Scheduled jobs anomalies chart](../image/io-job-anomalies-1.png)

Drill down from the hourly scheduled job count into an individual recurrence job for any hour of day and further into the execution pattern of the same job from the last seven days. This can help to perform end to end root cause for jobs that usually take a consistent amount of time to complete that suddenly experience a significant increase or decrease in execution time, indicating a possible performance issue.

![Job details after drilling down into a specific date.](../image/io-job-anomaly-detection-chart.png)

-   **Schedule job criteria**

    For the job to be considered a scheduled job, it should satisfy at least one of the following criteria:

    -   The job runs at least once for each day of the week.
    -   The job has run at least once for every week in the past four weeks.
-   **Average transaction count calculation**

    For every hour in a given day, the sum of the transaction count of the past four weeks for the same day and same hour is averaged. For example, by fetching the sum of transaction counts from the past four Mondays for the fourth hour and averages the values for the final calculation.

-   **Job anomaly identification**

    For the past four weeks, for every hour in which the job ran, the average duration time is calculated with the standard deviation value, which is the mean value, plus 5 multiplied by the standard deviation value.

    This value serves as an upper range for the job for that hour, if the job is running at the fourth hour and in the last four weeks the average duration of a job at that time is ten minutes and the standard deviation is two minutes, the upper range will be 10 + \(5\*2\) = 20 minutes.

    If the current running job takes more than 20 minutes to execute, then the job is identified as an anomaly.


## Anomaly response

All anomalies don’t represent an issue, but, the outliers detected based on historical patterns. Configure alerts accordingly after analyzing the criticality of the anomaly detected. See [Configure anomaly alerts](configure-anomaly-alerts.md) for more information on alerts.

