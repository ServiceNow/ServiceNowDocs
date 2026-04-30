---
title: Review HAM artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Impact Value Management Data Collection Content Pack for HAM, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Review HAM artifacts

The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.

## Performance/Platform analytics

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
|Data Collection Job|Impact VM - HAM - Monthly Data Collection|
|Data Collection Job|Impact VM - HAM - Historical Data Collection|
|Dashboard|Impact VM - HAM|
|Widget|% new hires with all HW provisioned by day 1|
|Widget|Backlog as a % HW requests|
|Widget|% unaccounted for HW assets|
|Widget|% HW assets in circulation|
|Widget|% of leased HW assets returned late|
|Widget|% of HW assets that have 'end of useful life' field populated|
|Widget|\# of Employees : \# of HAM FTEs|
|Widget|Legacy HAM systems annual run-rate|
|Widget|\# of unplanned outages from HW issues|
|Manual|Impact VM - % new hires with all HW provisioned by day 1|
|Formula|Impact VM - Backlog as a % HW requests|
|Automated|Impact VM - Number of created HW requests this month|
|Automated|Impact VM - Number of closed HW requests this month|
|Formula|Impact VM - % unaccounted for HW assets|
|Automated|Impact VM - \# HW assets accounted|
|Automated|Impact VM - \# HW assets missing|
|Formula|Impact VM - % HW assets in circulation|
|Automated|Impact VM - \# HW assets|
|Automated|Impact VM - \# HW assets in inventory|
|Manual|Impact VM - % of leased HW assets returned late|
|Manual|Impact VM - % of HW assets that have 'end of useful life' field populated|
|Manual|Impact VM - \# of employees: \# of HAM FTEs|
|Manual|Impact VM - Legacy HAM systems annual run-rate|
|Automated|Impact VM - \# of unplanned outages from HW issues this month|

