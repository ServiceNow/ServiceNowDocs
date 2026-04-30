---
title: Score normalization
description: In Smart Assessment Engine normalization maps the actual scores to a standardized scale, typically from 0 through 100, enabling for a unified evaluation framework.
locale: en-US
release: xanadu
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Normalization in assessment, Scoring assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Score normalization

In Smart Assessment Engine normalization maps the actual scores to a standardized scale, typically from 0 through 100, enabling for a unified evaluation framework.

## Normalization approach overview

In Smart Assessment Engine normalization adjusts individual assessment scores to a common scale, enabling comparison across different assessments. Normalization of assessment scores can be achieved through two approaches: Maximizing values, where higher scores are desirable, and minimizing values, where lower scores are preferred.

<table id="table_b3d_yg3_1gc"><tbody><tr><td>

To maximize the value

</td><td>

Maximize the value when higher values are better. The following formula is used to get the normalized score:

 `Normalized Score (High) = ((raw score - minimum Score) / (maximum score - minimum score)) * (scale factor maximum - scale factor minimum) + scale factor minimum`

</td></tr><tr><td>

To minimize the value

</td><td>

Minimize the value when lower values are better. The following formula is used to get the normalized score:

 `Normalized Score (High) = (1 - (raw score - minimum Score) / (maximum score - minimum score)) * (scale factor maximum - scale factor minimum) + scale factor minimum`

</td></tr></tbody>
</table>Where,

-   Raw score = Actual score calculated
-   Minimum score = The minimum value of the current scale.
-   Maximum score = The maximum value of the current scale.
-   Scale factor maximum = The minimum value of the target scale.
-   Scale factor minimum = The maximum value of the target scale.
-   Scale definition = Specifies the scoring direction: 'high' for higher scores being better or 'low' for lower scores being better.
-   Relative Scaling = When enabled the normalized score is calculated relative to the maximum value.

**Note:** This approach is applicable only when the linear normalization strategy is used. The formulas may vary if a different strategy is selected.

