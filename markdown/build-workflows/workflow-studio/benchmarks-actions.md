---
title: Benchmarks Spoke
description: Provides read-only actions for the read-only Benchmark Recommendation Evaluator flow.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Spokes, Flow integrations, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Benchmarks Spoke

Provides read-only actions for the read-only Benchmark Recommendation Evaluator flow.

The Benchmarks Spoke is designed for the Recommendations feature of the [Benchmarks](https://www.servicenow.com/docs/access?context=r_Benchmarks&version=australia&pubname=australia-it-service-management&ft:locale=en-US) application.

<table id="table_hkd_s53_jbb"><thead><tr><th>

Action

</th><th>

Description

</th><th>

Action Inputs

</th><th>

Action Outputs

</th></tr></thead><tbody><tr><td>

Create Recommendation Activity Records

</td><td>

Create or update recommendation activity records.

</td><td>

Recommendation

</td><td>

N/A

</td></tr><tr><td>

Delete Recommendation Evaluations

</td><td>

Delete recommendation evaluations for the specified month.

</td><td>

Activity record

</td><td>

N/A

</td></tr><tr><td>

Evaluate Recommendation Condition

</td><td>

Evaluate the conditions and script specified for the recommendation.

</td><td>

-   Record count
-   Threshold
-   Direction
-   Recommendation
-   Activity record

</td><td>

-   Result
-   Score

</td></tr></tbody>
</table>**Parent Topic:**[Spokes](../concept/spokes.md)

