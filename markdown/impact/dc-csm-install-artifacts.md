---
title: Review Customer Service Management artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/dc-csm-install-artifacts.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Impact Value Management Data Collection Content Pack for Customer Service Management, Enable data collection for Value Management, Guided Setup, Configuring Impact, Impact]
---

# Review Customer Service Management artifacts

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

The app contains the following artifacts for each of the before-specified artifact types.

**Note:** The frequencies of all applicable indicators and indicator sources have been changed to monthly from quarterly. If this is not the first time using this content pack, you should run a baseline historical job \(data collection job\) to capture applicable historical data. The historical data will be visualized in a future enhancement of the dashboard.

|Artifact type|Name|Outcome Model|
|-------------|----|-------------|
|Indicator Source|Impact VM - CSM - Case closed This month|Enhanced|
|Indicator Source|Impact VM - CSM - Case closed with account This month|Enhanced|
|Automated|Impact VM - CSM - Number of T1 customer cases closed|Enhanced|
|Automated|Impact VM - CSM - Number of T1 CS Agent FTEs|Enhanced|
|Automated|Impact VM - CSM - Number of customer cases|Enhanced|
|Automated|Impact VM - CSM - Number of customers|Enhanced|
|Automated|Impact VM - CSM - Number of T2 customer cases closed|Enhanced|
|Automated|Impact VM - CSM - Number of customer cases|Enhanced|
|Automated|Impact VM - \# of T2+ customer support cases closed|Standard|
|Automated|Impact VM - \# of T2+ customer support agents \*|Standard|
|Automated|Impact VM - \# of T1 customer support cases closed|Standard|
|Automated|Impact VM - \# of T1 customer support agent \*|Standard|
|Automated|Impact VM - \# of cases not resolved within SLAs|Standard|
|Automated|Impact VM - \# of customer cases|Standard|
|Automated|Impact VM - \# of closed customer cases|Standard|
|Automated|Impact VM - \# of customer cases that resulted in an upsell|Standard|
|Automated|Impact VM - \# of survey responses|Standard|
|Automated|Impact VM - \# of survey responses with a low overall service rating.|Standard|
|Automated|Impact VM - Avg. cumulative processing effort required per request case \(hrs\)|Standard|
|Formula|Impact VM - CSM - T1 cases closed per agent|Enhanced|
|Formula|Impact VM - CSM - Number of cases per customer|Enhanced|
|Formula|Impact VM - CSM - Cases escalated beyond Tier 1|Enhanced|
|Formula|Impact VM - % of customer cases that result in an upsell|Standard|
|Formula|Impact VM - % of surveyed customers that report an unfavorable support experience|Standard|
|Formula|Impact VM - % of cases not resolved within SLAs|Standard|
|Formula|Impact VM - \# of T1 customer support cases closed : \# of T1 customer support agent|Standard|
|Formula|Impact VM - \# of T2+ customer support cases closed: \# of T2+ customer support agents|Standard|
|Data Collection Job|Impact VM - CSM - Monthly Data Collection| |
|Data Collection Job|Impact VM - CSM - Historical Data Collection| |
|Widget|Impact VM - CSM - T1 cases closed per agent|Enhanced|
|Widget|Impact VM - CSM - Number of cases per customer|Enhanced|
|Widget|Impact VM - CSM - Cases escalated beyond Tier 1|Enhanced|
|Widget|% of cases not resolved within SLAs|Standard|
|Widget|\# of interactions handled by an agent that don't have related case|Standard|
|Widget|\# of revenue generating customer requests|Standard|
|Widget|\# of T1 customer support cases closed|Standard|
|Widget|\# of T1 customer support cases closed : \# of T1 customer support agents|Standard|
|Widget|\# of T2+ customer support cases closed|Standard|
|Widget|\# of T2+ customer support cases closed: \# of T2+ customer support agents|Standard|
|Widget|% of customer cases that result in an upsell|Standard|
|Widget|% of surveyed customers that report an unfavorable support experience|Standard|
|Widget|Avg. cumulative processing effort required per request case \(hrs\)|Standard|
|Dashboard|Impact VM - CSM Service Management| |
|Group Type|Tier 1| |
|Group Type|Tier 2+| |

**Parent Topic:**[Impact Value Management Data Collection Content Pack for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/data-collection-csm.md)

