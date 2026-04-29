---
title: Review SAM artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Impact Value Management Data Collection Content Pack for SAM, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Review SAM artifacts

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

**Note:** The frequencies of all applicable indicators and indicator sources have been changed from quarterly to monthly. If this is not the first time using this content pack, you should run a baseline historical job \(data collection job\) to capture applicable historical data. The historical data will be visualized in a future enhancement of the dashboard.

|Artifact type|Name|
|-------------|----|
|Formula|% new hires with all SW provisioned by day 1|
|Automated|Impact VM - \# of New Hire catalog Item Requests Completed by 1st day|
|Automated|Impact VM - Total Number of New Hires|
|Formula|Avg. time to close a SW request \(hrs\)|
|Automated|Impact VM - Total \# of completed sw requests|
|Automated|Impact VM - Total 'business duration' of completed sw requests|
|Formula|Impact VM - % of SaaS licenses unused / underutilized \(per publisher\)|
|Formula|Impact VM - unused / underutilized software licenses|
|Automated|Impact VM - Total \# of used software licenses|
|Automated|Impact VM - Total \# of software licenses|
|Formula|Impact VM - % of on-prem SW license unused / underutilized \(per publisher\)|
|Formula|Impact VM - % of SW that is centrally managed|
|Manual|Impact VM - Total \# of software|
|Automated|Impact VM - \# of managed software|
|Formula|Impact VM - \# of employees : \# of SAM FTEs|
|Automated|Impact VM - Total \# of employees|
|Automated|Impact VM - \# of SAM FTEs|
|Manual|Impact VM - Avg. time to respond to an audit \(hrs\)|
|Manual|Impact VM - Legacy SAM systems monthly run-rate|
|Formula|Impact VM - SW audit financial settlements as a % of SW spend|
|Automated|Impact VM - Current Subscription Spend|
|Automated|Impact VM - True-up Cost|
|Manual|Impact VM - \# of material security breaches due to vulnerable SW|
|Automated|Impact VM - \# of unplanned outages from SW issues|
|Data Collection Job|Impact VM - Monthly Data Collection|
|Widget|\# of employees : \# of SAM FTEs - monthly|
|Widget|\# of material security breaches due to vulnerable SW - monthly|
|Widget|\# of unplanned outages from SW issues - monthly|
|Widget|% new hires with all SW provisioned by day 1 - monthly|
|Widget|% of on-prem SW license unused / underutilized \(per publisher\) - monthly|
|Widget|% of SaaS licenses unused / underutilized \(per publisher\) - monthly|
|Widget|% of SW that is centrally managed - monthly|
|Widget|Avg. time to close a SW request \(hrs\) - monthly|
|Widget|Avg. time to respond to an audit \(hrs\) - monthly|
|Widget|Legacy SAM systems monthly run-rate|
|Widget|SW audit financial settlements as a % of SW spend - monthly|
|Dashboard|Impact VM - SAM|

