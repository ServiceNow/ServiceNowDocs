---
title: Ad hoc metric data task limitations
description: Ad hoc metric data tasks don't support certain features that are available for scheduled metric data tasks.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-30"
reading_time_minutes: 1
keywords: [ad hoc, metric data task, limitations]
breadcrumb: [Create ad hoc metric data tasks, Using GRC: Metrics to provide data, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Ad hoc metric data task limitations

Ad hoc metric data tasks don't support certain features that are available for scheduled metric data tasks.

-   **Threshold evaluation**

    Threshold fields and metric status are not evaluated for ad hoc tasks.

-   **Estimation**

    The **Type of Data** field is not available on ad hoc tasks. Estimation methods can't be used because ad hoc tasks are not tied to the metric calendar and have no period context from which to calculate estimates.

-   **Percentage variance**

    Percentage variance is not calculated for ad hoc metric data because there is no prior period to compare against.

-   **Last period data**

    The **Last Period Data** field is hidden and not tracked for ad hoc tasks.

-   **Score aggregation**

    Ad hoc metric data is excluded from metric definition score roll-ups and aggregate calculations.

-   **Composite metric definition calculation**

    Ad hoc metric data from a child metric is not included in composite metric definition \(CMD\) formula calculations. Only data from scheduled child metric tasks feeds into the CMD score. This applies at both levels:

    -   Entity-level CMD: Ad hoc task metric data is not included in aggregate calculations.
    -   Metric definition CMD: Ad hoc task metric data is not included in the CMD formula calculation.
-   **Target source**

    Only metric data from scheduled reporting cycles is used as the source value for targets. Ad hoc metric data is not considered for target calculations.


**Important:**

For calculated metric definitions with the **Calculation level** field set to **Entity**, ad hoc task data contributes to the metric score. This is the only exception. All other limitations listed before apply to both manual and calculated metric definitions.

**Parent Topic:**[Create ad hoc metric data tasks](../task/create-an-adhoc-metric-data-task.md)

