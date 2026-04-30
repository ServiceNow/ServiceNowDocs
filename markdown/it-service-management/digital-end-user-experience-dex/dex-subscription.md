---
title: DEX subscription
description: Digital End-User Experience \(DEX\) license counting provides the Subscription Unit \(SU\) consumption counting computers where any of the DEX features \(Desktop Assistant, Application and Device Health, and DEX Content Playbook\) are active.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Digital End-User Experience, IT Service Management]
---

# DEX subscription

Digital End-User Experience \(DEX\) license counting provides the Subscription Unit \(SU\) consumption counting computers where any of the DEX features \(Desktop Assistant, Application and Device Health, and DEX Content Playbook\) are active.

If multiple DEX features report usage on the same Configuration Items \(CIs\), the SU count removes the duplication.

## DEX capacity limitations

DEX uses the MetricBase datastore to store time-series data sampled at regular intervals. The MetricBase Series limit is controlled by data collection and retention policies for applications and devices that can’t be modified. For example, application and device metric data collected at five-minute intervals from each device is retained for up to seven days for troubleshooting purposes. Roll-ups of aggregated data is available for longer periods to analyze performance and usage trends. For information on policies and check definitions, see [DEX Content Playbook reference](../reference/dex-content-playbook-reference.md).

DEX can monitor up to 200 active applications per ServiceNow instance, with no more than 40 active applications per user per week. Active applications include Software as a Service \(SaaS\) and installed applications on end-user computing devices that are monitored by DEX.

DEX uses [metric rules](metric-rules.md) to analyze streams of metric data against sets of criteria and thresholds, triggering alerts when performance metrics deviate from specified parameters. An instance can have up to 50 active metric rules.

## DEX subscription unit calculation

DEX includes entitlement for up to the number of SUs purchased. A SU is a unit of measure applied to Managed IT Resources using Defined Ratios. For DEX, the Managed IT Resource Type is an End-user Computing \(EUC\) device. The SU to EUC device ratio is 1:4. For example, 1,000 SUs = 4,000 EUCs.

## Contact info

Contact your account team for additional information regarding DEX pricing and packaging.

