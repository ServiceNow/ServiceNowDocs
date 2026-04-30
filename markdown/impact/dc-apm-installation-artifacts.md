---
title: Review APM artifacts
description: The data collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Impact Value Management Data Collection for APM, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Review APM artifacts

The data collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.

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
|Data Collection Job|Impact VM – APM - Monthly Data Collection|
|Data Collection Job|Impact VM – APM - Historical Data Collection|
|Dashboard|Impact VM - APM|
|Widget|% of Business Capability Model with a Major Gap|
|Widget|Avg. application data certification %|
|Widget|\# of application retired|
|Widget|Legacy APM systems annual run-rate|
|Widget|% of applications with indicator score|
|Widget|\# of application migrated|
|Formula|Impact VM - % of Business Capability Model with a Major Gap|
|Automated|Impact VM - \# of Business Capabilities Linked to a Business Application|
|Automated|Impact VM - \# of Business Capabilities|
|Manual|Impact VM - Avg. application data certification %|
|Automated|Impact VM - \# of applications retired|
|Manual|Impact VM - Legacy APM systems annual run-rate|
|Manual|Impact VM - % of applications with indicator score|
|Automated|Impact VM - \# of applications migrated|

