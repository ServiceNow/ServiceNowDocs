---
title: Review App Engine artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
release: yokohama
product: Value Library
classification: value-library
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Impact Value Management Data Collection Content Pack for App Engine, Data Collection Toolkit, Value Management, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Review App Engine artifacts

The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.

|Artifact type|Description|
|-------------|-----------|
|Indicator Source|Captures the basic data sets and commits them to the working memory of the platform to provide the foundation for the calculations. This is also called a data cube.|
|Automated Indicator|Basic calculation definition on the indicator source data set, potentially with additional filter conditions that you apply before making the calculation.|
|Manual Indicator|Metric for which there is no data set within the platform. Requires you to manually add a data point.|
|Formula Indicator|A more comprehensive calculation, such as % and ratio calculations that require multiple automated indicator data points for the calculation.|
|Data Collection Jobs|One data collection job that you can schedule to run every month, and another data collector for historical collection that you can run on demand.|
|Widgets|Configuration for the UI visualization of an indicator.|
|Dashboard|Display of a collection of widgets on a pane. This dashboard contains two tabs. One tab contains widgets showing quarterly values, and the other contains widgets showing monthly values.|

## Artifacts by type

The app contains the following artifacts for each of the above-specified artifact types.

|Artifact type|Name|
|-------------|----|
|Data Collection Job|Impact VM – App Engine - Monthly Data Collection|
|Data Collection Job|Impact VM – App Engine - Historical Data Collection|
|Dashboard|Impact VM - App Engine|
|Widget|\# of applications built by core development team \(IT\), using LCAP|
|Widget|\# of applications \(and/or services\) built outside of core development team|
|Widget|Avg. time for application delivery \(IT\): idea to prod \(weeks\)|
|Widget|Avg. time for application delivery \(LOB\): idea to prod \(weeks\)|
|Widget|Former LCAP systems annual run-rate|
|Automated|Impact VM - \# of applications built by core development team \(IT\), using LCAP|
|Automated|Impact VM - \# of applications \(and/or services\) built outside of core development team|
|Manual|Impact VM - Avg. time for application delivery \(IT\): idea to prod \(Weeks\)|
|Manual|Impact VM - Avg. time for application delivery \(LOB\): idea to prod \(Weeks\)|
|Manual|Impact VM - Former LCAP systems run-rate|

