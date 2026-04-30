---
title: Review SecOps artifacts
description: The Data Collection app contains a pre-build data metric structure for the ServiceNow Performance/Platform Analytics application.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Impact Value Management Data Collection Content Pack for SecOps, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Review SecOps artifacts

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

|Artifact type|Name|
|-------------|----|
|Data Collection Job|Impact VM - SecOps - Monthly Data Collection|
|Data Collection Job|Impact VM - SecOps - Monthly Historical Data Collection|
|Dashboard|Impact VM - SecOps|
|Widget|Ratio of \# of vulnerable items with remediation task to vulnerability team|
|Widget|Ratio of closed vulnerability item to closed remediation task|
|Widget|% of SI's resolved by the SOC Tier 1 response team|
|Widget|Ratio of Security Incidents handled at Tier 1 to \# of SOC Tier 1 FTE|
|Widget|Ratio of Security Incidents handled at Tier 2+ to \# of SOC Tier 2+ FTE|
|Widget|% of critical vulnerable items not addressed|
|Widget|Average age of closed critical vulnerability items|
|Widget|% of non-critical vulnerable items not addressed|
|Widget|Avg. age of non-critical vulnerable item at closure \(days\)|
|Widget|Mean time to close a SI \(days\)|
|Formula|Impact VM - Ratio of number of vulnerable items with remediation task to the size of vulnerability team|
|Automated|Impact VM - \# of vulnerable items with remediation task opened this month|
|Automated|Impact VM - \# of vulnerability team FTEs|
|Formula|Impact VM - Ratio of closed vulnerability item to closed remediation task|
|Automated|Impact VM - \# of closed vulnerable items this month|
|Automated|Impact VM - \# of closed remediation task this month|
|Formula|Impact VM - % of Security Incidents resolved by the dedicated members of the SOC \(tier one\)|
|Automated|Impact VM - Number of security incidents closed by Tier1 this month|
|Automated|Impact VM - Number of closed security incidents this month|
|Formula|Impact VM - Ratio of total security incidents resolved at Tier 1 to the total number of SOC Tier 1 team|
|Automated|Impact VM - \# of SOC analyst \(Tier 1\)|
|Formula|Impact VM - Ratio of total security incidents resolved at Tier 2+ to the toal number of SOC Tier 2+ team|
|Automated|Impact VM - Number of security incidents closed by Tier 2+ this month|
|Automated|Impact VM - \# of SOC analyst \(Tier 2\)|
|Formula|Impact VM - % of critical vulnerable items not addressed|
|Automated|Impact VM - \# of open critical vulnerable items this month|
|Automated|Impact VM - \# of vulnerability opened this month|
|Formula|Impact VM - Average age of closed critical vulnerability items|
|Automated|Impact VM - Time to close critical vulnerability items|
|Automated|Impact VM - Vulnerable items P1 - P2 this month|
|Formula|Impact VM - % of non-critical vulnerable items not addressed|
|Automated|Impact VM - \# of open non-critical vulnerable items this month|
|Formula|Impact VM - Average age of closed non-critical vulnerability items|
|Automated|Impact VM - Average age of non-critical vulnerable items at closure \(days\)|
|Automated|Impact VM - \# of non critical \(P3, P4, P5\) vulnerable items this month|
|Formula|Impact VM - Mean time to close SI \(days\)|
|Automated|Impact VM - Summed duration of closed security incident|

