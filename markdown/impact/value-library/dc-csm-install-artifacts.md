---
title: Review CSM artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
release: yokohama
product: Value Library
classification: value-library
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Impact Value Management Data Collection Content Pack for CSM, Data Collection Toolkit, Value Management, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Review CSM artifacts

The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.

## Performance/Platform analytics

The content pack comes with the following artifact types. For configuring the process, Group Type is the group classification for the User Administration - Groups.

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

**Note:** The frequencies of all applicable indicators and indicator sources have been changed to monthly from quarterly. If this is not the first time using this content pack, you should run a baseline historical job \(data collection job\) to capture applicable historical data. The historical data will be visualized in a future enhancement of the dashboard.

|Artifact type|Name|
|-------------|----|
|Automated|Impact VM - \# of cases not resolved within SLAs|
|Automated|Impact VM - \# of customer cases|
|Formula|Impact VM - % of cases not resolved within SLAs|
|Automated|Impact VM - \# of closed customer cases|
|Automated|Impact VM - \# of customer cases that resulted in an upsell|
|Formula|Impact VM - % of customer cases that result in an upsell|
|Automated|Impact VM - \# of survey responses|
|Automated|Impact VM - \# of survey responses with a low overall service rating|
|Formula|Impact VM - % of surveyed customers that report an unfavorable support experience|
|Automated|Impact VM - Avg. cumulative processing effort required per request case \(hrs\)|
|Automated|Impact VM - \# of T1 customer support cases closed|
|Automated|Impact VM - \# of T1 customer support agent|
|Formula|Impact VM - \# of T1 customer support cases closed : \# of T1 customer support agent|
|Automated|Impact VM - \# of T2+ customer support cases closed|
|Automated|Impact VM - \# of T2+ customer support agents|
|Formula|Impact VM - \# of T2+ customer support cases closed: \# of T2+ customer support agents|
|Data Collection Job|Impact VM - Monthly Data Collection|
|Widget|% of cases not resolved within SLAs|
|Widget|\# of interactions handled by an agent that don't have related case|
|Widget|\# of revenue generating customer requests|
|Widget|\# of T1 customer support cases closed|
|Widget|\# of T1 customer support cases closed : \# of T1 customer support agents|
|Widget|\# of T2+ customer support cases closed|
|Widget|\# of T2+ customer support cases closed: \# of T2+ customer support agents|
|Widget|% of customer cases that result in an upsell|
|Widget|% of surveyed customers that report an unfavorable support experience|
|Widget|Avg. cumulative processing effort required per request case \(hrs\)|
|Dashboard|Impact VM - CSM|
|Group Type|Tier 1|
|Group Type|Tier 2+|

