---
title: Sensitivity detection configuration tables
description: Many types of components are configured to activate sensitivity detection, including table configurations.
locale: en-US
release: xanadu
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Reference for Now Assist for HR Service Delivery \(HRSD\), Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Sensitivity detection configuration tables

Many types of components are configured to activate sensitivity detection, including table configurations.

<table id="id_shh_f1w_nbc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_gen\_ai\_filter\_group

</td><td>

Table that enables you to define groups that can help bundle all relevant filters together.

</td></tr><tr><td>

sys\_gen\_ai\_filter

</td><td>

Table that contains all the filter categories that you defined \(including the thresholds, portals that the filter is mapped to a description that is used to generate utterances\).

</td></tr><tr><td>

sys\_gen\_ai\_filter\_sample

</td><td>

Table that contains the sample utterances for each filter that tries to match against to determine sensitivity.

</td></tr><tr><td>

sys\_gen\_ai\_filter\_config

</td><td>

Table that maps the filter to the generative AI capability that it is supposed to be executed before.

</td></tr><tr><td>

sys\_one\_extend\_definition\_attribute

 sys\_one\_extend\_capability

</td><td>

Table that defines the inputs and outputs for the generative AI capabilities \(in the **sys\_one\_extend\_capability**table that is available on the platform.

</td></tr></tbody>
</table>