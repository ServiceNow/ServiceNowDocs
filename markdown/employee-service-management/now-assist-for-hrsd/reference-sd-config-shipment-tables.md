---
title: Sensitivity detection configuration table filters
description: Many types of components are configured to activate sensitivity detection, including table filter configurations.
locale: en-US
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Reference for Now Assist for HR Service Delivery \(HRSD\), Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Sensitivity detection configuration table filters

Many types of components are configured to activate sensitivity detection, including table filter configurations.

<table id="id_qc1_lbw_nbc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_gen\_ai\_filter\_group

</td><td>

Single filter group that contains all the relevant filters for sensitivity detection.

</td></tr><tr><td>

sys\_gen\_ai\_filter

</td><td>

Eight Filters that have a different sensitive category that enables you to identify sensitive employee cases with reasonable accuracy.

</td></tr><tr><td>

sys\_gen\_ai\_filter\_sample

</td><td>

Filter samples \(371\), that are mapped to a specific filter to help you identify the kinds of phrases that should be detected by the filter.

</td></tr><tr><td>

sys\_gen\_ai\_filter\_config

</td><td>

Records in this table that map to each filter for the following three capabilities:

Semantic Search: This capability narrows down the potential topics.

Skill search: This capability sends the narrowed down topics for the final selection.

 Free-form Prompt: This capability takes the user input.

</td></tr><tr><td>

sys\_one\_extend\_definition\_attribute

 sys\_one\_extend\_capability

</td><td>

Not applicable

</td></tr></tbody>
</table>