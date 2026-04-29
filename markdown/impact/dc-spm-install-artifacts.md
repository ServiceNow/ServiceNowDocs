---
title: Review SPM artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install the Data Collection Pack, Impact Value Management Data Collection Content Pack for SPM, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Review SPM artifacts

The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.

The content pack comes with the following artifact types.

|Artifact type|Description|
|-------------|-----------|
|Indicator Source|Captures the basic data sets and commits them to the working memory of the platform to provide the foundation for the calculations. This is also called a data cube.|
|Automated Indicator|Basic calculation definition on the indicator source data set, potentially with additional filter conditions that you apply before making the calculation.|
|Manual Indicator|Metric for which there is no data set within the platform. Requires you to manually add a data point.|
|Formula Indicator|A more comprehensive calculation, such as % and ratio calculations that require multiple automated indicator data points for the calculation.|
|Data Collection Jobs|Schedule on which the automated data collection will run.|
|Widgets|Configuration for the UI visualization of an indicator.|
|Dashboard|Display of a collection of widgets on a pane. This dashboard contains two tabs. One tab contains widgets showing quarterly values, and the other contains widgets showing monthly values.|

## Artifacts by type

The app contains the following artifacts for each of the above-specified artifact types.

|Artifact type|Name|
|-------------|----|
|Data Collection Job|Impact VM – SPM - Monthly Data Collection|
|Data Collection Job|Impact VM – SPM - Historical Data Collection|
|Dashboard|Impact VM - SPM|
|Widget|% of projects completed that are identified as aligned to strategy|
|Widget|Avg. cycle time for approved demand \(days\)|
|Widget|Avg. project duration \(weeks\)|
|Widget|Project Budget actuals vs. forecast|
|Widget|Avg. budget under management per PM|
|Widget|Avg. total effort required per demand|
|Widget|% of project team spent on administrative tasks|
|Widget|Total benefits of demands to decommission/migrate legacy system|
|Widget|% attainment of forecasted benefits this month|
|Formula|Impact VM - % of projects completed that are identified as aligned to strategy|
|Automated|Impact VM - \# of projects completed this month|
|Automated|Impact VM - \# of projects completed this month with primary goal assigned|
|Formula|Impact VM - Avg. cycle time for approved demand \(days\)|
|Automated|Impact VM - Total Age of Demand to Project This Month \(Days\)|
|Automated|Impact VM - Total demands to projects this month|
|Formula|Impact VM - Avg. project duration \(weeks\)|
|Automated|Impact VM - Total number of the completed projects this month|
|Automated|Impact VM - Sum of project Actual Duration|
|Formula|Impact VM - Project Budget actuals vs. forecast|
|Automated|Impact VM - Total actual cost for the projects ended this month|
|Automated|Impact VM - Total budgeted cost for the projects ended this month|
|Formula|Impact VM - Avg. budget under management per PM|
|Automated|Impact VM - Number of Project managers|
|Formula|Impact VM - Avg. total effort required per demand|
|Automated|Impact VM - \# of demands completed this month|
|Automated|Impact VM - Total allocated hours for all demands completed|
|Manual|Impact VM - % of project team spent on administrative tasks|
|Manual|Impact VM - Total benefits of demands to decommission/migrate legacy system|
|Formula|Impact VM - % attainment of forecasted benefits this month|
|Automated|Impact VM - Total actual benefits attained for the completed projects this month|
|Automated|Impact VM - Total forecasted benefits attained for the completed projects this month|

