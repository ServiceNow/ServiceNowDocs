---
title: Review IRM artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Impact Value Management Data Collection Content Pack for IRM, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Review IRM artifacts

The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.

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

|Artifact type|Description|
|-------------|-----------|
|Data Collection Job|Impact VM – IRM - Monthly Data Collection|
|Data Collection Job|Impact VM – IRM - Historical Data Collection|
|Dashboard|Impact VM - IRM|
|Widget|\# of employees : \# of internal audit team FTEs|
|Widget|\# of controls : \# of risk manager FTEs \(IT, Ent Op\)|
|Widget|\# of major risk events|
|Widget|Avg. loss per major risk event|
|Widget|Avg. loss per minor risk event|
|Widget|Avg. time spent per control per year \(hrs\)|
|Widget|\# of privacy-related controls : \# of privacy team FTEs|
|Widget|\# of minor risk events|
|Widget|Outsourced risk mgmt. spend as % of avg. risk mgmt. spend|
|Widget|Legacy IRM and privacy systems annual run-rate|
|Formula|Impact VM - Ratio of \# of employees : \# of Internal Audit team FTEs|
|Automated|Impact VM - \# of Internal Audit team FTEs|
|Automated|Impact VM - \# of Employee|
|Formula|Impact VM - Ratio of Total number of Controls to \# of Risk Managers FTE|
|Automated|Impact VM - \# of Risk Managers FTE|
|Automated|Impact VM - \# of Privacy related controls|
|Automated|Impact VM - \# of Major Risk Events|
|Formula|Impact VM - Reduction in avg. loss per major risk event|
|Automated|Impact VM - Gross loss of major risk event|
|Automated|Impact VM - \# of major risk event|
|Formula|Impact VM - Reduction in avg. loss per minor risk event|
|Automated|Impact VM - Gross loss for minor risk event|
|Automated|Impact VM - \# of Minor Risk Event|
|Formula|Impact VM - Avg. time spent per control per year \(hrs\)|
|Automated|Impact VM - Total \# of controls|
|Manual|Impact VM - Total time spent per year \(Hrs\)|
|Formula|Impact VM - Ratio of \# of Privacy related controls: \# of privacy team FTEs|
|Automated|Impact VM - \# of Privacy related controls|
|Automated|Impact VM - \# of Privacy team FTEs|
|Automated|Impact VM - \# of Minor Risk Events|
|Manual|Outsourced risk mgmt. spend as % of avg. risk mgmt. spend|
|Manual|Legacy IRM and privacy systems annual run-rate|

