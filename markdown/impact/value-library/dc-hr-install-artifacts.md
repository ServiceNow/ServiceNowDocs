---
title: Review HR artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance Analytics application.
locale: en-US
release: yokohama
product: Value Library
classification: value-library
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Impact Value Management Data Collection Content Pack for HR, Data Collection Toolkit, Value Management, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Review HR artifacts

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

The app contains the following artifacts for each of the above-specified artifact types.

**Note:** The frequencies of all applicable indicators and indicator sources have been changed to monthly from quarterly. If this is not the first time using this content pack, you should run a baseline historical job \(data collection job\) to capture applicable historical data. The historical data will be visualized in a future enhancement of the dashboard.

|Artifact type|Name|
|-------------|----|
|Indicator Source|Impact VM - Active Users|
|Indicator Source|Impact VM - Employee Onboarded This Month|
|Indicator Source|Impact VM - HR Lifecycle Tasks Closed This Month|
|Indicator Source|Impact VM - HR Cases Opened This Month|
|Indicator Source|Impact VM - Employee Offboarded This Month|
|Indicator Source|Impact VM - Group Members|
|Indicator Source|Impact VM - Cases Closed This Month|
|Automated|Impact VM - Opened HR Cases Originating from Phonecalls|
|Automated|Impact VM - Number of Tier 2+ HR Agents|
|Automated|Impact VM - Number of TIer 1 HR Agents|
|Automated|Impact VM - Number of Transfer Tasks This Month|
|Automated|Impact VM – Number of Tier 2+ HR Cases Closed This Month|
|Automated|Impact VM - Number of Tier 1 HR Cases Closed This Month|
|Automated|Impact VM - Number of Transfer Lifecycle Event Cases Closed This Month|
|Automated|Impact VM - Number of Offboarding Lifecycle Event Cases Closed This Month|
|Automated|Impact VM - Number of New Hires Separated This Month|
|Automated|Impact VM - Number of Onboarding Tasks This Month|
|Automated|Impact VM - Number of Offboarding Tasks This Month|
|Automated|Impact VM - Number of Opened HR Cases This Month|
|Automated|Impact VM - Number of Onboarding Lifecycle Event Cases Closed This Month|
|Automated|Impact VM - Number of HR Cases Closed This Month|
|Automated|Impact VM - Number of New Hires This Month|
|Formula|Impact VM - Year 1 New Hire Attrition Rate This Month|
|Formula|Impact VM - Ratio of Tier 2+ Cases per Tier 2+ Agent|
|Formula|Impact VM - Ratio of Tier 1 Cases per Tier 1 Agent|
|Formula|Impact VM - Average Activities per Transfer Case This Month|
|Formula|Impact VM - Average Activities per Offboarding Case This Month|
|Formula|Impact VM - Average Activities per Onboarding Case This Month|
|Formula|Impact VM - % of Opened HR Cases Originating from Phonecalls This Month|
|Manual|Impact VM - Legacy HR Systems Annual Run-Rate|
|Data Collection Job|Impact VM - Monthly Data Collection|
|Widget|Ratio of Tier 2+ Cases to Tier 2+ Agents|
|Widget|Percent of HR Cases Originating for Phonecalls|
|Widget|Legacy HR systems annual run-rate|
|Widget|Average Activities per Offboarding Case This Month|
|Widget|Number of HR Cases Closed This Month|
|Widget|First Year Employee Attrition Rate This Month|
|Widget|Number of Tier 1 HR Cases Closed This Month|
|Widget|Average Activities per Onboarding Case This Month|
|Widget|Ratio of T1 Cases to Tier 1 Agents|
|Widget|Average Activities per Transfer Case This Month|
|Widget|Number of Tier 2 HR Cases Closed This Month|
|Dashboard|Impact VM - HR|
|Group Type|Tier 1|
|Group Type|Tier 2+|

