---
title: Review ITOM artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance Analytics application and includes artifact types.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Impact Value Management Data Collection Content Pack for ITOM, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Review ITOM artifacts

The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance Analytics application and includes artifact types.

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

**Note:** The frequencies of all applicable indicators and indicator sources have been changed to monthly from quarterly. If this is not the first time using this content pack, you should run a baseline historical job \(data collection job\) to capture applicable historical data. The historical data will be visualized in a future enhancement of the dashboard.

Also, this version of the ITOM Data Collection app relies on ITSM product licensing for the metrics highlighted below. Currently, the workaround involves manually updating these metrics in Impact.

The app contains the following artifacts for each of the above-specified artifact types.

|Artifact type|Name|
|-------------|----|
|Automated|Impact VM - ITOM - \# of Incidents Closed This Month|
|Automated|Impact VM - ITOM - \# of L1 Incidents Closed This Month|
|Automated|Impact VM - ITOM - \# of L2+ Incidents Closed This Month|
|Automated|Impact VM - ITOM - Average Time to Close an Incident \(hrs\)|
|Automated|Impact VM - Auto-Created Incidents in This Month|
|Automated|Impact VM - Number Alerts Triggered in This Month|
|Automated|Impact VM - Number of Virtual Events in This Month|
|Automated|Impact VM - Number of Non-Secondary Alerts in This Month|
|Automated|Impact VM - ITOM - \# of Unplanned Outages This Month|
|Automated|Impact VM - ITOM - Mean Time to Restore - Unplanned Outages \(hrs\)|
|Automated|Impact VM - ITOM - Number of Active Users|
|Automated|Impact VM - ITOM - \# of Tier 1 Agents|
|Automated|Impact VM - ITOM -\# of Tier 2+ Agents|
|Formula|Impact VM - ITOM - Ratio of Incidents Closed per Tier 1 Service Desk Agent This Month|
|Formula|Impact VM - ITOM - Ratio of Incidents Closed per Tier 2+ Service Desk Agent This Month|
|Formula|Impact VM - % of Auto-Created Incidents this Month|
|Formula|Impact VM - % Alert Correlation in This Month|
|Manual|Impact VM - Legacy ITOM Systems Monthly Run-Rate|
|Data Collection Job|Impact VM - Monthly Data Collection|
|Widget|% of Auto-Created Incidents|
|Widget|% of Alert Correlation|
|Widget|Average Time to Close an Incident \(hrs\)|
|Widget|Legacy ITOM System Run-Rate|
|Widget|Mean Time to Restore Unplanned Outages \(hrs\)|
|Widget|Number of Active Users|
|Widget|Number of Incident Closed|
|Widget|Number of Incidents Closed at Tier 1|
|Widget|Number of Tier 2+ Incidents Closed|
|Widget|Number of Unplanned Outages|
|Widget|Ratio of Closed Incident per Tier 2+ Agent|
|Widget|Ratio of Closed Incidents per Tier 1 Service Desk Agent|
|Dashboard|Impact VM - ITOM|
|Group Type|Tier 1|
|Group Type|Tier 2+|

