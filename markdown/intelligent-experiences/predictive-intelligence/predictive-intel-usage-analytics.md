---
title: Predictive Intelligence Usage Analytics dashboard
description: The Predictive Intelligence Usage Analytics dashboard is a central location to understand the effectiveness and overall value of all your Predictive Intelligence solutions. View metrics for model training successes and failures. Monitor prediction statistics including breakdowns by individual model.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Testing and monitoring predictions, Predictive Intelligence, Enable AI experiences]
---

# Predictive Intelligence Usage Analytics dashboard

The Predictive Intelligence Usage Analytics dashboard is a central location to understand the effectiveness and overall value of all your Predictive Intelligence solutions. View metrics for model training successes and failures. Monitor prediction statistics including breakdowns by individual model.

![An overview of the PI Usage Dashboard, with the tab for the Classification tab open. The Date Range selector is highlighted. Several widgets are visible, such as Total Active Solutions.](../images/predictive-intel-usage-analytics-overview-a.png)

For your models in the Classification, Similarity, and Clustering capabilities, the Predictive Intelligence Usage Analytics dashboard gives you visibility into training and predictions. You can specify the time periods to report on, as well as select specific solutions for a deep dive.

With the ml\_report\_user or ml\_admin role, view the Predictive Intelligence Usage Analytics dashboard by navigating to **Predictive Intelligence** &gt; **Dashboards** &gt; **Monitoring**.

The dashboard has separate tabs for each capability. The Classification tab opens by default, or you can select Similarity or Clustering. Each tab contains a set of reports in the form of widgets.

You can drill down into the underlying records by selecting a report's chart or graph, which opens a query-filtered list. Many reports in the Training Statistics section of PI Usage Dashboard are drawn from the ml\_solution table. Reports in the Prediction Statistics section are drawn from the ml\_predictor\_results table.

## Date Range

The **Date Range** selector opens a calendar picker where you can select the time frame for the reports. Your selected date range applies to all widgets on the current tab.

The calendar picker offers a variety of preset dates under its **Standard** subhead. Choose from **Last 3 months**, **Today**, **YTD** \(year to date, from January 1 of the current calendar year\), and so forth.

You can also choose **Custom range** to select your own dates. Enter dates directly into the **Start date** and **End date** fields, or select a date range using the calendar. Then select **Apply** to update the reports in all widgets on the page.

![The Date Range selector is open, showing a variety of Standard date ranges. Also available is a calendar and fields for specifying a Custom range.](../images/predictive-intel-usage-analytics-date-selector-a.png)

## Available metrics for Classification and Similarity

The following tables describe the widgets available on both the Classification and Similarity tabs, unless otherwise noted. The Clustering capability has different widgets, so refer to the **Available metrics for Clustering** section on this page.

<table id="table_a4x_kzx_l3c"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total Solutions

</td><td>

Total number of Classification \(or Similarity\) solutions created.

</td></tr><tr><td>

Total Active Solutions

</td><td>

Total number of Classification \(or Similarity\) solutions that are active.

</td></tr><tr><td>

Total Successful Model Trainings

</td><td>

The number of Classification \(or Similarity\) jobs that have been successfully completed in the instance.

</td></tr><tr><td>

Total Failed Model Trainings

</td><td>

The number of Classification \(or Similarity\) jobs that have failed in the instance.

</td></tr><tr><td>

Trained Solutions - By Month

</td><td>

Total trained Classification \(or Similarity\) solutions aggregated monthly.

</td></tr><tr><td>

Active Solutions - By Month

</td><td>

Total active Classification \(or Similarity\) solutions aggregated monthly.

</td></tr><tr><td>

Classification \(or Similarity\) Training Status

</td><td>

The distribution of Classification \(or Similarity\) model training states.

</td></tr><tr><td>

Active Status Distribution

</td><td>

The distribution of active versus inactive records. The "true" portion indicates active items, while "false" represents inactive ones.

</td></tr><tr><td>

Training Frequency Distribution

</td><td>

The training frequency distribution across all Classification \(or Similarity\) solutions.The available options range from **Run once** up to **Every 180 days**.

</td></tr><tr><td>

Update Frequency Distribution \(Similarity only\)

</td><td>

The update frequency distribution across all similarity solutions.The available options range from **Run once** up to **Every 180 days**.

</td></tr></tbody>
</table>|Widget|Description|
|------|-----------|
|Total Successful Predictions - By Month|Count of total Classification \(or Similarity\) predictions calculated per month.|
|Total Successful Predictions|Total number of successful predictions made on all Classification \(or Similarity\) solutions.|
|Total Failed predictions|Total number of failed predictions made on all Classification \(or Similarity\) solutions.|

![The Classification solution selector is open, displaying names of three Classification solution available for selection.](../images/predictive-intel-usage-analytics-solution-selector-a.png)

For the following widgets, use the selector labeled **Classification solution** or **Similarity solution** to choose an individual model.

|Widget|Description|
|------|-----------|
|Successful Predictions per Solution|The number of successful predictions for the selected Classification \(or Similarity\) solution.|
|Failed Predictions per Solution|The number of failed predictions for the selected Classification \(or Similarity\) solution.|

## Available metrics for Clustering

The following table describes metrics available on the Clustering tab of the Predictive Intelligence Usage Analytics dashboard.

|Widget|Description|
|------|-----------|
|Total Solutions|The total number of clustering solutions created in the instance.|
|Total Active Solutions|The number of active clustering solutions in the instance.|
|Total Successful Model Trainings|The number of clustering jobs that have been successfully completed in the instance.|
|Total Failed Model Trainings|The number of clustering jobs that have failed in the instance.|
|Trained Solutions - By Month|The number of clustering trainings triggered per month.|
|Active Solutions - By Month|The number of active clustering solutions trained per month.|
|Clustering Training Status|A pie chart showing the training status distribution across all clustering solutions in the instance.|
|Active Status Distribution|A pie chart showing the distribution of active and inactive clustering solutions.|
|Training Frequency Distribution|The percentage of training frequencies set across the clustering solutions.|
|Update Frequency Distribution|The percentage of update frequencies set across the clustering solutions.|

For the following widgets, use the selector labeled **Clustering solution** on the Clustering tab to pick an individual model.

|Widget|Description|
|------|-----------|
|Cluster details|The details of each cluster created in the specified solution.|
|Number of clusters|The number of clusters created in the specified clustering solution.|
|Total Records Clustered|The total number of records clustered in the specified clustering solution.|
|Number of updates completed \(in last 7 days\)|The number of update jobs completed for a specified clustering solution.|
|Details of Last Update \(in last 7 days\)|When the clustering solution was last updated, number of new clusters created, records assigned to existing clusters, and new clusters in the last update.|

**Parent Topic:**[Testing and monitoring predictions](testing-reviewing-ml-solutions.md)

