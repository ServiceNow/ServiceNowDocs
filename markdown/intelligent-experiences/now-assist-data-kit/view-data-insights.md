---
title: View data insights
description: You can view data insights to see metrics for your generated data and data collections.
locale: en-US
release: zurich
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# View data insights

You can view data insights to see metrics for your generated data and data collections.

## Before you begin

Role required: sn\_data\_kit.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**.

2.  Select the dataset or data collection that you want to see data insights for.

3.  Select the **Data insights** tab.

    |Metric|Description|
    |------|-----------|
    |Data volume|This metric identifies rows with unusually low character count or significantly fewer words compared to the dataset average.|
    |Semantic similarity to seed|This metric is LLM-based and measures how closely each record’s meaning matches a given reference \(seed\).|
    |Data hygiene|This metric is LLM-based and checks that fields follow the correct types and formats.|
    |Missing/Empty values|This metric identifies fields that are null, empty, or contain placeholder values without valid justification.|
    |Temporal consistency|This metric is LLM-based and ensures that data remains logically correct over time.|

    ![Now Assist Data Kit data insights page](../image/nadk-data-insights.png)

    |Metric|Description|
    |------|-----------|
    |Data volume|Identifies rows with unusually low character count or significantly fewer words compared to the dataset average.|
    |Missing/empty values|Identifies fields that are null, empty, or contain placeholder values.|


