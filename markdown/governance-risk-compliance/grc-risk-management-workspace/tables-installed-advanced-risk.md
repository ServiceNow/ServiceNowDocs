---
title: Tables installed with Advanced Risk
description: Tables are added with activation of GRC: Advanced Risk.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Components installed with Advanced Risk, Reference, Risk Management, Governance, Risk, and Compliance]
---

# Tables installed with Advanced Risk

Tables are added with activation of GRC: Advanced Risk.

<table id="table_qlq_g3m_vs"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk Event Task\[sn\_risk\_advanced\_mitigation\]

</td><td>

Track the mitigation tasks associated with the risk event reported.

</td></tr><tr><td>

Aggregated Risk Report\[sn\_risk\_advanced\_risk\_report\_definition\]

</td><td>

Create this definition where the customer can choose entities and associate some risk statements with these entities to report aggregated risk scores.

</td></tr><tr><td>

Risk Report\[sn\_risk\_advanced\_risk\_report\]

</td><td>

Based on the aggregated risk report definition, a record for each combination of entity and risk statement is created. The tolerance status and calculated score is also displayed.

</td></tr><tr><td>

Event Entry\[sn\_risk\_advanced\_event\_impact\]

</td><td>

Impact entries for the risk event to be added by the Risk Manager during the Analyze state.

</td></tr><tr><td>

Risk Event to Risk\[sn\_risk\_advanced\_m2m\_event\_risk\]

</td><td>

Each risk event can be associated to applicable risks. This table enables tracking the risk event to risk relationships.

</td></tr><tr><td>

Risk Event\[sn\_risk\_advanced\_event\]

</td><td>

Tracks the loss or gain events reported by different users.

</td></tr><tr><td>

Associated Risk Events\[sn\_risk\_advanced\_m2m\_event\_event\]

</td><td>

A risk event can be linked to multiple other risk events. This table contains those associations.

</td></tr><tr><td>

Risk Event to Entity\[sn\_risk\_advanced\_m2m\_event\_profile\]

</td><td>

A Risk Manager can relate multiple entities that are impacted by the risk event. This table tracks the impacted entities linked to the risk event.

</td></tr><tr><td>

Risk Event to Control\[sn\_risk\_advanced\_m2m\_event\_control\]

</td><td>

A Risk Manager can relate multiple controls related to the entities that are linked to the risk event. This table tracks the impacted entities linked to the risk event.

</td></tr><tr><td>

Risk Event to Citation\[sn\_risk\_advanced\_m2m\_event\_citation\]

</td><td>

A risk manager can relate risk events to regulatory obligations and citations. This association facilitates breach reporting and compliance with regulations.

</td></tr></tbody>
</table>**Note:** All additional tables installed by the dependent plugins are also needed for GRC: Advanced Risk.

**Parent Topic:**[Components installed with Advanced Risk](components-risk-advanced.md)

