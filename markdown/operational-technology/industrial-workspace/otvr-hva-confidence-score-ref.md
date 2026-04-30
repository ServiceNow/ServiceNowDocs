---
title: Confidence score reference tables for hardware vulnerability assessment
description: Reference values used to calculate the confidence score.
locale: en-US
release: zurich
product: Industrial Workspace
classification: industrial-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Operational Technology Hardware Vulnerability Assessment, Explore, Industrial Workspace, Operational Technology]
---

# Confidence score reference tables for hardware vulnerability assessment

Reference values used to calculate the confidence score.

## Reference tables

|Information available in discovery model for OT device|Information available in CPE mapped to OT device|Partial match score|Additional score for full match|
|------------------------------------------------------|------------------------------------------------|-------------------|-------------------------------|
|Discovered Publisher name|Publisher|20|5|
|Discovered Model name|Model|20|5|
|Discovered Version|Version|0|25|

<table id="table_hsz_zjc_2yb"><thead><tr><th>

Score

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Sum of all scores

</td><td>

75

</td></tr><tr><td>

Base score**Note:** Minimum score given to all matched discovery models.

</td><td>

25

</td></tr><tr><td>

Total score

</td><td>

100

</td></tr></tbody>
</table>**Parent Topic:**[Operational Technology Hardware Vulnerability Assessment](../concept/understanding-hwd-vuln-assessment.md)

