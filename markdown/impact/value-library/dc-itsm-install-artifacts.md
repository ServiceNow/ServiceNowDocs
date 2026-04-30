---
title: Review ITSM artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
release: yokohama
product: Value Library
classification: value-library
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Impact Value Management Data Collection Content Pack for ITSM, Data Collection Toolkit, Value Management, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Review ITSM artifacts

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

The app contains the following artifacts for each of the above specified types.

|Artifact type|Description|
|-------------|-----------|
|Indicator Source|Impact VM - Changes Closed This Month|
|Indicator Source|Impact VM - Group Members|
|Indicator Source|Impact VM – Active Users|
|Indicator Source|Impact VM - Incidents Closed This Month|
|Indicator Source|Impact VM - Outage Ended on This Month|
|Indicator Source|Impact VM - Requested Items Closed This Month|
|Indicator Source|Impact VM - Requests Fulfilled in the This Month|
|Automated|Impact VM - ITSM - Mean Time to Restore - Unplanned Outages \(hrs\)|
|Automated|Impact VM - ITSM - Average Time to Close an Incident \(hrs\)|
|Automated|Impact VM - Number of Closed Incident Originating from Phonecalls|
|Automated|Impact VM - Average Time to Close a Request \(hrs\)|
|Automated|Impact VM - Number of Closed Standard Changes|
|Automated|Impact VM - ITSM - \# of Tier 2+ Agents|
|Automated|Impact VM - \# of Unplanned Outages This Month|
|Automated|Impact VM - ITSM - Average Time To Close a Change in Hours|
|Automated|Impact VM - ITSM - \# of Tier 1 Agents|
|Automated|Impact VM - \# Requested Items Closed This Month|
|Automated|Impact VM - \# of Requests Fulfilled This Month|
|Automated|Impact VM - ITSM - \# of L1 Incidents Closed This Month|
|Automated|Impact VM - \# of Changes Closed This Month|
|Automated|Impact VM - ITSM - \# of L2+ Incidents Closed This Month|
|Automated|Impact VM - ITSM - \# of Incidents Closed This Month|
|Automated|Impact VM - \# Automated Requested Items Closed This Month|
|Automated|Impact VM - ITSM - Number of Active Users|
|Manual|Impact VM - Legacy ITSM Systems Annual Run-Rate|
|Formula|Impact VM - ITSM - Ratio of Incidents Closed per Tier 2+ Service Desk Agent This Month|
|Formula|Impact VM - % of Requested Items Fuflfilled that were Automated This Month|
|Formula|Impact VM - % of Changes that are Standard Closed This Month|
|Formula|Impact VM - % of Closed Incidents Originating from Phone Call This Month|
|Formula|Impact VM – ITSM - Ratio of Incidents Closed per Tier 1 Service Desk Agent This Month|
|Data Collection Job|Impact VM – ITSM - Monthly Data Collection|
|Data Collection Job|Impact VM – ITSM – Historical Data Collection|
|Widget|% Closed Changes that were Standard|
|Widget|% Closed Incidents Originating from Phone Call|
|Widget|% of Fulfilled Requested Items that were Automated|
|Widget|Average Time to Close a Change \(hrs\)|
|Widget|Average Time to Close a Request \(hrs\)|
|Widget|Average Time to Close an Incident \(hrs\)|
|Widget|Legacy ITSM System Monthly Run-Rate|
|Widget|Mean Time to Restore Unplanned Outages \(hrs\)|
|Widget|Number of Changes Closed|
|Widget|Number of Incidents Closed|
|Widget|Number of Incidents Closed at Tier 1|
|Widget|Number of Requests Fulfilled|
|Widget|Number of Tier 2+ Incidents Closed|
|Widget|Number of Unplanned Outages|
|Widget|Ratio of Closed Incident per Tier 2+ Agent|
|Widget|Ratio of Closed Incidents per Tier 1 Service Desk Agent|
|Widget|Number of Active Users|
|Dashboard|Impact VM - ITSM|
|Group Type|Tier 1|
|Group Type|Tier 2+|

