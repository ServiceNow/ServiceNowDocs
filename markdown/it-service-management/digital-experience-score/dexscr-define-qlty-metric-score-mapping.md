---
title: Define qualitative mapping for a DEX Score metric
description: Define mapping between the qualitative value and normalized score of a DEX Score metric according to your business needs.
locale: en-US
release: yokohama
product: Digital Experience Score
classification: digital-experience-score
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Digital Experience Score​, Digital Experience Score​, Digital End-User Experience, IT Service Management]
---

# Define qualitative mapping for a DEX Score metric

Define mapping between the qualitative value and normalized score of a DEX Score metric according to your business needs.

## Before you begin

Role required: sn\_dex\_score.digital\_workplace\_leader

## Procedure

1.  Navigate to **All** &gt; **Digital Experience Score​** &gt; **Qualitative Metric Score Mapping**.

2.  From the Qualitative Metric Score Mappings page, open a metric record using one of the following options.

    -   Hover over the metric name, select the reference icon \(![Reference icon](../../service-operations-workspace/image/inc-preview-record.png)\) next to it, and then select **Open Record** on the preview pop-up.
    -   Select a number in the **Normalized score** column.
3.  In the form, customize the metric mapping details.

<table id="table_atw_ygm_wdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Metric

</td><td>

Name of the metric for which the qualitative mapping is to be set.For example, Battery health.

</td></tr><tr><td>

Normalized score

</td><td>

Normalized score for the metric. This score is in the range 1–100 and maps to a performance category. For example, 45.For information about how normalized scores are calculated, see [DEX Score normalization for metric scores](../reference/dexscr-dex-score-normalization.md).

</td></tr><tr><td>

Qualitative value

</td><td>

Performance category such as Poor, Moderate, or Good that you can map to a normalized score.For example, you can map a normalized score of 45 to the Poor category and a score of 75 to the Moderate category, for the Battery health metric.

</td></tr></tbody>
</table>4.  Select **Update**.


**Parent Topic:**[Configuring Digital Experience Score​](../concept/dexscr-configuring-dex-score.md)

**Related topics**  


[Customize metric definitions](dexscr-customize-dex-score-metric-defs.md)

[Metric scores in Digital Experience Score​](../concept/dexscr-dex-score-defs.md)

[DEX Score metrics calculation](../reference/dexscr-dex-score-metrics-calc.md)

