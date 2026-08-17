---
title: Review ITSM artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/dc-itsm-install-artifacts.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Impact Value Management Data Collection Content Pack for ITSM, Enable data collection for Value Management, Configuring Impact, Impact]
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

|Artifact type|Description| |
|-------------|-----------|---|
|Indicator Source|Impact VM ITSM - User active last 365 days|Enhanced|
|Indicator Source|Impact VM - ITSM - \# of Incidents Closed This Month |Enhanced|
|Indicator Source|Impact VM - ITSM - Change request closed This month |Enhanced|
|Indicator Source|Impact VM - ITSM - Request item closed This month |Enhanced|
|Indicator Source|Impact VM - Group Members|Standard|
|Indicator Source|Impact VM – Active Users|Standard|
|Indicator Source|Impact VM - Incidents Closed This Month|Standard|
|Indicator Source|Impact VM - Outage Ended on This Month|Standard|
|Indicator Source|Impact VM - Changes Closed This Month|Standard|
|Indicator Source|Impact VM - Requested Items Closed This Month|Standard|
|Indicator Source|Impact VM - Requests Fulfilled in the This Month|Standard|
|Automated|Impact VM ITSM - Count of Human active users logged in per last  365 days |Enhanced|
|Automated|Impact VM ITSM - \# of incidents closed in This month |Enhanced|
|Automated|Impact VM - ITSM - Number of standard changes closed |Enhanced|
|Automated|Impact VM - ITSM - Number of changes closed |Enhanced|
|Automated|Impact VM - ITSM - Number of RITMs closed |Enhanced|
|Automated|Impact VM - ITSM - Mean Time to Restore - Unplanned Outages \(hrs\)|Standard|
|Automated|Impact VM - ITSM - Mean Time to Restore - Unplanned Outages \(hrs\)|Standard|
|Automated|Impact VM - ITSM - Average Time to Close an Incident \(hrs\)|Standard|
|Automated|Impact VM - Number of Closed Incident Originating from Phonecalls|Standard|
|Automated|Impact VM - Average Time to Close a Request \(hrs\)|Standard|
|Automated|Impact VM - Number of Closed Standard Changes|Standard|
|Automated|Impact VM - ITSM - \# of Tier 2+ Agents|Standard|
|Automated|Impact VM - \# of Unplanned Outages This Month|Standard|
|Automated|Impact VM - ITSM - Average Time To Close a Change in Hours|Standard|
|Automated|Impact VM - ITSM - \# of Tier 1 Agents|Standard|
|Automated|Impact VM - \# Requested Items Closed This Month|Standard|
|Automated|Impact VM - \# of Requests Fulfilled This Month|Standard|
|Automated|Impact VM - ITSM - \# of L1 Incidents Closed This Month|Standard|
|Automated|Impact VM - \# of Changes Closed This Month|Standard|
|Automated|Impact VM - ITSM - \# of L2+ Incidents Closed This Month|Standard|
|Automated|Impact VM - ITSM - \# of Incidents Closed This Month|Standard|
|Automated|Impact VM - \# Automated Requested Items Closed This Month|Standard|
|Automated|Impact VM - ITSM - Number of Active Users\*|Standard|
|Manual|Impact VM - Legacy ITSM Systems Annual Run-Rate|Standard|
|Formula|Impact VM ITSM - Incidents closed per active user |Enhanced|
|Formula|Impact VM - ITSM - Ratio of Incidents Closed per Tier 2+ Service Desk Agent This Month|Standard|
|Formula|Impact VM ITSM - Incidents closed per active user |Enhanced|
|Formula|Impact VM - ITSM - Changes that are standard |Enhanced|
|Formula|Impact VM - ITSM - RITMs closed per active user |Enhanced|
|Formula|Impact VM - % of Requested Items Fulfilled that were Automated This Month|Standard|
|Formula|Impact VM - % of Changes that are Standard Closed This Month|Standard|
|Formula|Impact VM - % of Closed Incidents Originating from Phone Call This Month|Standard|
|Formula|Impact VM – ITSM - Ratio of Incidents Closed per Tier 1 Service Desk Agent This Month|Standard|
|Data Collection Job|Impact VM – ITSM - Monthly Data Collection|Standard|
|Data Collection Job|Impact VM – ITSM – Historical Data Collection|Standard|
|Widget|Incidents closed per active user|Enhanced|
|Widget|RITMs closed per active user|Enhanced|
|Widget|Changes that are standard|Enhanced|
|Widget|Incidents Closed per active user|Enhanced|
|Widget|% Closed Changes that were Standard|Enhanced|
|Widget|% Closed Incidents Originating from Phone Call|Standard|
|Widget|% of Fulfilled Requested Items that were Automated|Standard|
|Widget|Average Time to Close a Change \(hrs\)|Standard|
|Widget|Average Time to Close a Request \(hrs\)|Standard|
|Widget|Average Time to Close an Incident \(hrs\)|Standard|
|Widget|Legacy ITSM System Monthly Run-Rate|Standard|
|Widget|Mean Time to Restore Unplanned Outages \(hrs\)|Standard|
|Widget|Number of Changes Closed|Standard|
|Widget|Number of Incidents Closed|Standard|
|Widget|Number of Incidents Closed at Tier 1|Standard|
|Widget|Number of Requests Fulfilled|Standard|
|Widget|Number of Tier 2+ Incidents Closed|Standard|
|Widget|Number of Unplanned Outages|Standard|
|Widget|Ratio of Closed Incident per Tier 2+ Agent|Standard|
|Widget|Ratio of Closed Incidents per Tier 1 Service Desk Agent|Standard|
|Widget|Number of Active Users|Standard|
|Dashboard|Impact VM - ITSM|Standard|
|Group Type|Tier 1|Standard|
|Group Type|Tier 2+|Standard|

**Parent Topic:**[Impact Value Management Data Collection Content Pack for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/data-collection-itsm.md)

