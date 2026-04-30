---
title: Performance Analytic indicators to measure application performance
description: Use performance analytic \(PA\) indicators to know the count of incidents, problems, and changes logged against a business application and use this insight to improve the performance of your applications.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Preconfigured indicators and their source applications - Legacy, Framework setup for application assessment - Legacy, Application assessment - Legacy, Explore- Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Performance Analytic indicators to measure application performance

Use performance analytic \(PA\) indicators to know the count of incidents, problems, and changes logged against a business application and use this insight to improve the performance of your applications.

Enterprise Architecture uses indicators that are sourced from Performance Analytics \(PA\). These indicators give a count of incidents, problems, changes, and the number of change requests that were closed on a given day. Follow the given order to run the PA jobs at the scheduled time, and get the scores of the indicators to evaluate the performance of your business applications.

## Order in which to run PA jobs and generate scores

You should run the scheduled jobs in the following order:

1.  \[PA Incident\] Daily Data Collection.
2.  \[PA Change\] Daily Data Collection.
3.  \[PA Problem\] Daily Data Collection.
4.  \[Enterprise Architecture Scheduled job\] Load Application Indicators and compute Application Scores.

If there are historic data, then run them in the following order:

**Note:**

You require Performance Analytics Premium for Enterprise Architecture \(com.snc.pa.premium.apm\) plugin to retrieve historic data that are older than six months.

1.  \[PA Incident\] Historic Data Collection.
2.  \[PA Change\] Historic Data Collection.
3.  \[PA Problem\] Historic Data Collection.
4.  Regenerate Enterprise Architecture scores for required time period. This action deletes the existing scores including daily scores and generates new scores instead of just updating the existing scores.

## Frequency at which indicator scores are generated

Scores are generated as per the scheduled run of the job that executes the script. If the indicator frequency is:

-   **Monthly**

    scores are generated only on the last day of a month.

-   **Quarter**

    scores are generated only on the last day of a quarter.

-   **Yearly**

    scores are generated only on the last day of a year.


**Note:** Fiscal periods should be generated in the same time zone in which the scores are generated.

## Collection of PA indicator score data

The period unit \(days, weeks, or month\) at which the PA indicator scores are collected and preserved depends on the frequency of the data source indicator. However, the frequency at which the application indicator collects the PA indicator data source scores varies.

In Enterprise Architecture, the frequency of the application indicator must be greater than or equal to the frequency of the data source indicator.

The following table describes the frequency at which Enterprise Architecture collects data from the data source indicators after the job runs:

|Enterprise Architecture frequency|Data source indicator frequency|
|---------------------------------|-------------------------------|
|Monthly|Monthly|
|Quarterly|Monthly and Quarterly|
|Yearly|Monthly, Quarterly, and Yearly|

If you are an Enterprise Architecture customer, who has upgraded to the Zurich release, then the **Daily** frequency of Performance Analytics data source indicator is not available. RemoveDailyFreqAndUpdatePAIndicator fix script automatically removes the **Daily** frequency of PA indicators and updates the frequency to **Monthly**.

## Limitations to display application breakdowns in PA scoresheet

If there is a large number of business applications installed, then all the breakdowns are not displayed in the **Performance Analytics** &gt; **Scoresheet**, as there is a limitation set in the system properties: **com.snc.pa.scoresheet.max\_elements** and **com.snc.pa.scorecards.max\_breakdown\_elements**. To reconfigure the property limitation:

1.  Navigate to **Performance Analytics** &gt; **System** &gt; **Properties**.
2.  Enter the maximum number in the **Maximum number of elements of a breakdown in Scoresheet** field. The number must be greater than or equal to the number of business applications installed in your system.
3.  Enter the maximum number in the **Maximum number of breakdown elements in scorecard lists** field.
4.  Click **Save**.

**Parent Topic:**[Preconfigured indicators and their source applications - Legacy](../reference/preconfigured-indicators-and-sources.md)

