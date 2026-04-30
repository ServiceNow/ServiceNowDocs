---
title: MetricBase retention policies
description: Retain data in MetricBase according to retention policies.
locale: en-US
release: yokohama
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Define and collect data, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MetricBase retention policies

Retain data in MetricBase according to retention policies.

Retention policies include multiple retention schedules with coarser granularity the longer that the data is kept. For example, the Coarse retention policy stores sampled data every:

-   Hour for one week \(7 Days per 1-hour period\)
-   Two hours for one month \(31 days per 2-hour period\)
-   Day for 13 months \(397 Days per 1-day period\)

In this policy, the specified metric is measured every hour for the first 7 days. It is then measured every other hour for the next 31 days, and once a day for the next 397 days. MetricBase deletes data that is older than 435 days.

To see the list of all supported retention policies, navigate to **MetricBase** &gt; **Retention Policies**.

<table id="table_umb_vn4_14b"><thead><tr><th>

Policy

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Coarse

</td><td>

This policy retains data for 1 week at 1-hour period, 1 month at 2-hour period, and 13 months at 1-day period.

 This policy is suitable for metrics that change less often or metrics that do not require high resolution, such as disk usage.

</td></tr><tr><td>

Dense

</td><td>

This policy retains data for 8 days at 1-minute period, 94 days at 10-minute period, and 13 months at 1-hour period. This policy is suitable for metrics that require higher resolution for longer terms.

</td></tr><tr><td>

High

</td><td>

This policy retains data for 1 week at 1-minute period, 1 month at 10-minute period, and 13 months at 1-hour period.

 This policy is suitable for metrics that require higher resolution for longer terms.

</td></tr><tr><td>

Medium

</td><td>

This policy retains data for 1 week at 10-minute period, 1 month at 30-minute period, and 13 months at 2-hour period.

 This policy is suitable for metrics that change less often such as job processing throughput.

</td></tr><tr><td>

Medium High

</td><td>

This policy retains data for 13 months at 1-hour period.

</td></tr><tr><td>

Operational Intelligence

</td><td>

Operational Intelligence \(OI\) policy retains data for 8 days at 1-minute period, 94 days at 10-minute period, and 13 months at 1-hour period.

</td></tr><tr><td>

Sparse

</td><td>

This policy retains data for 13 months at 1-day period.

</td></tr><tr><td>

Ultra Dense

</td><td>

This policy retains data for 1 day at 10-second period, 3 months at 1-minute period, and 1 year at 1-hour period.

</td></tr></tbody>
</table>