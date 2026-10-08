---
title: Review HR Service Delivery artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance Analytics application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/dc-hr-install-artifacts.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Impact Value Management Data Collection Content Pack for HR Service Delivery, Enable data collection for Value Management, Guided Setup, Configuring Impact, Impact]
---

# Review HR Service Delivery artifacts

The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance Analytics application.

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
|Indicator Source|Impact VM - HR - HR case closed This month|Enhanced|
|Indicator Source|Impact VM - HR - User active last 365 days|Enhanced|
|Indicator Source|Impact VM - Active Users|Standard|
|Indicator Source|Impact VM - Employee Onboarded This Month|Standard|
|Indicator Source|Impact VM - HR life cycle Tasks Closed This Month|Standard|
|Indicator Source|Impact VM - HR Cases Opened This Month|Standard|
|Indicator Source|Impact VM - Employee Offboarded This Month|Standard|
|Indicator Source|Impact VM - Group Members|Standard|
|Indicator Source|Impact VM - Cases Closed This Month|Standard|
|Automated|Impact VM - HR - Number of T1 HR cases closed|Enhanced|
|Automated|Impact VM - HR - Number of T1 HR Agent FTEs|Enhanced|
|Automated|Impact VM - HR - Number of HR cases|Enhanced|
|Automated|Impact VM - HR - Count of Human active users logged in per last 365 days|Enhanced|
|Automated|Impact VM - HR - Number of T2 HR cases closed|Enhanced|
|Automated|Impact VM - Opened HR Cases Originating from Phonecalls|Standard|
|Automated|Impact VM - Number of Tier 2+ HR Agents \*|Standard|
|Automated|Impact VM - Number of TIer 1 HR Agents \*|Standard|
|Automated|Impact VM - Number of Transfer Tasks This Month|Standard|
|Automated|Impact VM – Number of Tier 2+ HR Cases Closed This Month|Standard|
|Automated|Impact VM - Number of Tier 1 HR Cases Closed This Month|Standard|
|Automated|Impact VM - Number of Transfer life cycle Event Cases Closed This Month|Standard|
|Automated|Impact VM - Number of Offboarding life cycle Event Cases Closed This Month|Standard|
|Automated|Impact VM - Number of New Hires Separated This Month|Standard|
|Automated|Impact VM - Number of Onboarding Tasks This Month|Standard|
|Automated|Impact VM - Number of Offboarding Tasks This Month|Standard|
|Automated|Impact VM - Number of Opened HR Cases This Month|Standard|
|Automated|Impact VM - Number of Onboarding life cycle Event Cases Closed This Month|Standard|
|Automated|Impact VM - Number of HR Cases Closed This Month|Standard|
|Automated|Impact VM - Number of New Hires This Month|Standard|
|Formula|Impact VM - HR - T1 HR cases closed per agent|Enhanced|
|Formula|Impact VM - HR - Number of HR cases per active user|Enhanced|
|Formula|Impact VM - HR - HR cases escalated beyond Tier 1|Enhanced|
|Formula|Impact VM - Year 1 New Hire Attrition Rate This Month|Standard|
|Formula|Impact VM - Ratio of Tier 2+ Cases per Tier 2+ Agent|Standard|
|Formula|Impact VM - Ratio of Tier 1 Cases per Tier 1 Agent|Standard|
|Formula|Impact VM - Average Activities per Transfer Case This Month|Standard|
|Formula|Impact VM - Average Activities per Offboarding Case This Month|Standard|
|Formula|Impact VM - Average Activities per Onboarding Case This Month|Standard|
|Formula|Impact VM - % of Opened HR Cases Originating from Phonecalls This Month|Standard|
|Manual|Impact VM - Legacy HR Systems Annual Run-Rate|Standard|
|Data Collection Job|Impact VM - HR - Historical Data Collection||
|Data Collection Job|Impact VM - HR - Monthly Data Collection||
|Widget|Impact VM - HR - T1 HR cases closed per agent|Enhanced|
|Widget|Impact VM - HR - HR cases escalated beyond Tier 1|Enhanced|
|Widget|Impact VM - HR - Number of HR cases per active user|Enhanced|
|Widget|Impact VM - HR - Number of HR cases per active user|Enhanced|
|Widget|Ratio of Tier 2+ Cases to Tier 2+ Agents|Standard|
|Widget|Percent of HR Cases Originating for Phonecalls|Standard|
|Widget|Legacy HR systems annual run-rate|Standard|
|Widget|Average Activities per Offboarding Case This Month|Standard|
|Widget|Number of HR Cases Closed This Month|Standard|
|Widget|First Year Employee Attrition Rate This Month|Standard|
|Widget|Number of Tier 1 HR Cases Closed This Month|Standard|
|Widget|Average Activities per Onboarding Case This Month|Standard|
|Widget|Ratio of T1 Cases to Tier 1 Agents|Standard|
|Widget|Average Activities per Transfer Case This Month|Standard|
|Widget|Number of Tier 2 HR Cases Closed This Month|Standard|
|Dashboard|Impact VM - HR Service Delivery| |
|Group Type|Tier 1| |
|Group Type|Tier 2+| |

**Parent Topic:**[Impact Value Management Data Collection Content Pack for HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/data-collection-hr.md)

