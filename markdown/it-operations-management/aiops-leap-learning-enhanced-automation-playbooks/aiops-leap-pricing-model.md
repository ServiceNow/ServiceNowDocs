---
title: LEAP assist pricing
description: LEAP charges assists based on the size and complexity of incident clusters it analyzes. Starting with the 202606 release, LEAP uses a fixed pricing model to simplify cost predictability.
locale: en-US
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [LEAP pricing assists cluster analysis]
breadcrumb: [Exploring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# LEAP assist pricing

LEAP charges assists based on the size and complexity of incident clusters it analyzes. Starting with the 202606 release, LEAP uses a fixed pricing model to simplify cost predictability.

When LEAP analyzes incident clusters to generate resolution steps, playbooks, and knowledge base articles, it consumes assists from your entitlement. The number of assists consumed depends on the pricing model active on your instance.

## Tiered pricing model \(pre-202606\)

Before the 202606 release, LEAP uses a tiered pricing model based on cluster size. The assist cost scales with the number of records in each cluster, using map-reduce, sampling, and batching to process incidents efficiently.

|Cluster size \(records\)|Assist cost|
|------------------------|-----------|
|1–10|25 assists|
|11–20|50 assists|
|21–30|75 assists|
|31–40|100 assists|
|41 or more|125 assists|

## Fixed pricing model \(202606 and later\)

Starting with the 202606 release, LEAP uses a fixed pricing model. Each cluster analysis is charged at a flat rate of **125 assists**, regardless of cluster size. This simplifies cost tracking and aligns pricing with the value delivered for large incident clusters.

**Note:** The fixed cost of 125 assists is deducted per cluster analysis. Manual assist deductions also apply at 125 assists per operation.

## Pricing impact by cluster size

The following table compares assist costs before and after the 202606 release and shows the impact on each cluster size tier.

|Cluster size \(records\)|Pre-202606 cost|Post-202606 cost|Impact|
|------------------------|---------------|----------------|------|
|1–10|25 assists|125 assists|+400%|
|11–20|50 assists|125 assists|+150%|
|21–30|75 assists|125 assists|+67%|
|31–40|100 assists|125 assists|+25%|
|41 or more|125 assists|125 assists|No change|

Customers running clusters of 41 or more records see no change in assist consumption. Customers with smaller clusters will see an increase in assist costs per analysis.

## Optimizing assist consumption

To get the most value from the fixed pricing model, consider the following:

-   Consolidate smaller incident clusters where possible to maximize the value of each 125-assist charge
-   Prioritize high-impact clusters with 41 or more records, where the cost per record is lowest
-   Review your assist entitlement to account for the pricing change if your workloads consist primarily of small clusters

