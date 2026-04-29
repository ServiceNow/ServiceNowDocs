---
title: AIOps LEAP settings fields
description: AIOps LEAP settings page field values helps estimate cost and time savings when automation is used. The default values can be modified as per your organizational requirement for savings calculations.
locale: en-US
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AIOps LEAP reference, AIOps Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# AIOps LEAP settings fields

AIOps LEAP settings page field values helps estimate cost and time savings when automation is used. The default values can be modified as per your organizational requirement for savings calculations.

## LEAP settings fields

<table id="table_ory_tlf_nhc"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost per work note \($\)

</td><td>

This value represents the cost for each work note that also includes labor and operational expenses for every incident.

</td></tr><tr><td>

Time per work note \(hrs\)

</td><td>

This value is the average time spent on each work note entry used to estimate the total time impact across incidents.

</td></tr><tr><td>

Overhead factor for P1 records

</td><td>

Overhead factors are multipliers that are used for high-priority incidents and represent hidden costs. Priority 1 incidents often require more coordination, communication, and escalation—beyond just the direct work notes. For P1 incidents, the base cost is multiplied by 1.8 to reflect the additional impact.

</td></tr><tr><td>

Overhead factor for P2 records

</td><td>

Overhead factors are multipliers that are used for high-priority incidents and represent hidden costs. For priority 2 incidents, the base cost is multiplied by 1.4 to reflect the additional impact.

</td></tr><tr><td>

Overhead factor for P3 records

</td><td>

Overhead factors are multipliers that are used for high-priority incidents and represent hidden costs. For priority 3 incidents, the base cost is multiplied by 1.1 to reflect the additional impact.

</td></tr><tr><td>

Overhead factor for P4 records

</td><td>

Overhead factors are multipliers that are used for high-priority incidents and represent hidden costs. For priority 4, the base cost is multiplied by 0.8 to reflect the additional impact.

</td></tr><tr><td>

Overhead factor for P5 records

</td><td>

Overhead factors are multipliers that are used for high-priority incidents and represent hidden costs. For priority 5, the base cost is multiplied by 0.4 to reflect the additional impact.

</td></tr><tr><td>

Large group size

</td><td>

Groups that have incidents more than the threshold set are marked as large groups. The default value set is 200 incidents.

</td></tr><tr><td>

Number of pinned groups

</td><td>

This value specifies the number of groups that can be pinned for tracking.

</td></tr><tr><td>

Groups with resolution steps in initial run

</td><td>

This value specifies the number of groups for which resolution steps are generated in the first run of AIOps LEAP.

</td></tr><tr><td>

Minimum incident-to-group ratio for remapping eligibility

</td><td>

AIOps LEAP can remap incidents to better groups when improved patterns are observed. This ratio determines the minimum incident-to-group size needed for remapping eligibility. Higher values means more selective remapping.

</td></tr></tbody>
</table>