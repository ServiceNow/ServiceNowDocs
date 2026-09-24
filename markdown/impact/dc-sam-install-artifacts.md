---
title: Review IT Asset Management artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/dc-sam-install-artifacts.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Impact Value Management Data Collection Content Pack for IT Asset Management, Enable data collection for Value Management, Configuring Impact, Impact]
---

# Review IT Asset Management artifacts

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

The app contains the following artifacts for each of the befor-specified artifact types.

**Note:** The frequencies of all applicable indicators and indicator sources have been changed from quarterly to monthly. If this is not the first time using this content pack, you should run a baseline historical job \(data collection job\) to capture applicable historical data. The historical data will be visualized in a future enhancement of the dashboard.

|Artifact type|Name| |
|-------------|----|---|
|Formula|% new hires with all SW provisioned by day 1|Software Asset Management|
|Automated|Impact VM - \# of New Hire catalog Item Requests Completed by 1st day|Software Asset Management|
|Automated|Impact VM - Total Number of New Hires|Software Asset Management|
|Formula|Avg. time to close a SW request \(hrs\)|Software Asset Management|
|Automated|Impact VM - Total \# of completed sw requests|Software Asset Management|
|sset ManagementAutomated|Impact VM - Total 'business duration' of completed sw requests|Software Asset Management|
|Formula|Impact VM - % of SaaS licenses unused / underutilized \(per publisher\)|Software Asset Management|
|Formula|Impact VM - unused / underutilized software licenses|Software Asset Management|
|Automated|Impact VM - Total \# of used software licenses|Software Asset Management|
|Automated|Impact VM - Total \# of software licenses|Software Asset Management|
|Formula|Impact VM - % of on-prem SW license unused / underutilized \(per publisher\)|Software Asset Management|
|Formula|Impact VM - % of SW that is centrally managed|Software Asset Management|
|Manual|Impact VM - Total \# of software|Software Asset Management|
|Automated|Impact VM - \# of managed software|Software Asset Management|
|Formula|Impact VM - \# of employees : \# of SAM FTEs|Software Asset Management|
|Automated|Impact VM - Total \# of employees|Software Asset Management|
|Automated|Impact VM - \# of SAM FTEs|Software Asset Management|
|Manual|Impact VM - Avg. time to respond to an audit \(hrs\)|Software Asset Management|
|Manual|Impact VM - Legacy SAM systems monthly run-rate|Software Asset Management|
|Formula|Impact VM - SW audit financial settlements as a % of SW spend|Software Asset Management|
|Automated|Impact VM - Current Subscription Spend|Software Asset Management|
|Automated|Impact VM - True-up Cost|Software Asset Management|
|Manual|Impact VM - \# of material security breaches due to vulnerable SW|Software Asset Management|
|Automated|Impact VM - \# of unplanned outages from SW issues|Software Asset Management|
|Automated|\# of unplanned outages from SW issues|Software Asset Management|
|Manual|Impact VM - % new hires with all HW provisioned by day 1|Hardware Asset Management|
|Formula|Impact VM - Backlog as a % HW requests|Hardware Asset Management|
|Automated|Impact VM - Number of created HW requests this month|Hardware Asset Management|
|Automated|Impact VM - Number of closed HW requests this month|Hardware Asset Management|
|Formula|Impact VM - % unaccounted for HW assets|Hardware Asset Management|
|Automated|Impact VM - \# HW assets accounted|Hardware Asset Management|
|Automated|Impact VM - \# HW assets missing|Hardware Asset Management|
|Formula|Impact VM - % HW assets in circulation|Hardware Asset Management|
|Automated|Impact VM - \# HW assets|Hardware Asset Management|
|Automated|Impact VM - \# HW assets in inventory|Hardware Asset Management|
|Manual|Impact VM - % of leased HW assets returned late|Hardware Asset Management|
|Manual|Impact VM - % of HW assets that have 'end of useful life' field populated|Hardware Asset Management|
|Manual|Impact VM - \# of employees: \# of HAM FTEs|Hardware Asset Management|
|Manual|Impact VM - Legacy HAM systems annual run-rate|Hardware Asset Management|
|Automated|Impact VM - \# of unplanned outages from HW issues this month|Hardware Asset Management|
|Widget|\# of employees : \# of SAM FTEs - monthly|Software Asset Management|
|Widget|\# of material security breaches due to vulnerable SW - monthly|Software Asset Management|
|Widget|\# of unplanned outages from SW issues - monthly|Software Asset Management|
|Widget|% new hires with all SW provisioned by day 1 - monthly|Software Asset Management|
|Widget|% of on-prem SW license unused / underutilized \(per publisher\) - monthly|Software Asset Management|
|Widget|% of SaaS licenses unused / underutilized \(per publisher\) - monthly|Software Asset Management|
|Widget|% of SW that is centrally managed - monthly|Software Asset Management|
|Widget|Avg. time to close a SW request \(hrs\) - monthly|Software Asset Management|
|Widget|Avg. time to respond to an audit \(hrs\) - monthly|Software Asset Management|
|Widget|Legacy SAM systems monthly run-rate|Software Asset Management|
|Widget|SW audit financial settlements as a % of SW spend - monthly|Software Asset Management|
|Widget|% new hires with all HW provisioned by day 1|Hardware Asset Management|
|Widget|Backlog as a % HW requests|Hardware Asset Management|
|Widget|% unaccounted for HW assets|Hardware Asset Management|
|Widget|% HW assets in circulation|Hardware Asset Management|
|Widget|% of leased HW assets returned late|Hardware Asset Management|
|Widget|% of HW assets that have 'end of useful life' field populated|Hardware Asset Management|
|Widget|\# of Employees : \# of HAM FTEs|Hardware Asset Management|
|Widget|Legacy HAM systems annual run-rate|Hardware Asset Management|
|Widget|\# of unplanned outages from HW issues|Hardware Asset Management|
|Data Collection Job|Impact VM - IT Asset Management - Monthly Data Collection|IT Asset Management|
|Data Collection Job|Impact VM - IT Asset Management - Historical Data Collection|IT Asset Management|
|Dashboard|Impact VM - IT Asset Management|IT Asset Management|

**Parent Topic:**[Impact Value Management Data Collection Content Pack for IT Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/data-collection-sam.md)

