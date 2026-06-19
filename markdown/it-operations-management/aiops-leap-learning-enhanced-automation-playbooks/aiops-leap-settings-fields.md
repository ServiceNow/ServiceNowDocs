---
title: LEAP settings fields
description: LEAP settings page field values help estimate cost and time savings when automation is used. These settings support cost predictability with the fixed pricing model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-settings-fields.html
release: zurich
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: reference
last_updated: "2026-04-14"
reading_time_minutes: 3
breadcrumb: [LEAP reference, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# LEAP settings fields

LEAP settings page field values help estimate cost and time savings when automation is used. These settings support cost predictability with the fixed pricing model.

## LEAP settings fields

<table><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost per work note \($\)

</td><td>

This value represents the cost for each work note that also includes labor and operational expenses for every incident.

 **Example:** If your organization spends an average of $50 per work note entry including analyst time and overhead, enter 50. This value is used to calculate total cost savings when automation reduces the number of work notes.

</td></tr><tr><td>

Time per work note \(hrs\)

</td><td>

This value is the average time spent on each work note entry used to estimate the total time impact across incidents.

 **Example:** If analysts spend an average of 30 minutes on each work note, enter 0.5. For a cluster of 100 incidents with 4 work notes each, LEAP estimates 200 hours of time savings when automation is applied.

</td></tr><tr><td>

P1 - Critical priority incidents

</td><td>

Overhead factors are multipliers that are used for high-priority incidents and represent hidden costs. Priority 1 incidents often require more coordination, communication, and escalation — beyond just the direct work notes. For P1 incidents, the base cost is multiplied by 1.8 to reflect the additional impact.

 **Example:** If the base cost per work note is $50 and a P1 incident has 4 work notes, the adjusted cost is $50 × 4 × 1.8 = $360.

</td></tr><tr><td>

P2 - High priority incidents

</td><td>

Overhead factors are multipliers that are used for high-priority incidents and represent hidden costs. For priority 2 incidents, the base cost is multiplied by 1.4 to reflect the additional impact.

 **Example:** If the base cost per work note is $50 and a P2 incident has 4 work notes, the adjusted cost is $50 × 4 × 1.4 = $280.

</td></tr><tr><td>

P3 - Moderate priority incidents

</td><td>

Overhead factors are multipliers that are used for moderate-priority incidents and represent hidden costs. For priority 3 incidents, the base cost is multiplied by 1.1 to reflect the additional impact.

 **Example:** If the base cost per work note is $50 and a P3 incident has 4 work notes, the adjusted cost is $50 × 4 × 1.1 = $220.

</td></tr><tr><td>

P4 - Low priority incidents

</td><td>

Overhead factors are multipliers that are used for low-priority incidents and represent hidden costs. For priority 4, the base cost is multiplied by 0.8 to reflect the additional impact.

 **Example:** If the base cost per work note is $50 and a P4 incident has 4 work notes, the adjusted cost is $50 × 4 × 0.8 = $160.

</td></tr><tr><td>

P5 - Planning incidents

</td><td>

Overhead factors are multipliers that are used for low-priority incidents and represent hidden costs. For priority 5, the base cost is multiplied by 0.4 to reflect the additional impact.

 **Example:** If the base cost per work note is $50 and a P5 incident has 4 work notes, the adjusted cost is $50 × 4 × 0.4 = $80.

</td></tr><tr class="sub-head"><td colspan="2">

Grouping configuration

</td></tr><tr><td>

Large group threshold

</td><td>

Groups that have incidents more than the threshold set are marked as large groups. The default value set is 100 incidents.

 **Example:** If set to 200, any group containing more than 200 incidents is flagged as a large group, helping LEAP prioritize high-volume clusters for automation analysis.

</td></tr><tr><td>

Initial run: Groups with resolution steps

</td><td>

The maximum number of groups for which resolution steps are generated in the first run of LEAP. The default is 500.

 **Example:** If set to 500, LEAP generates resolution steps for up to 500 groups in the first run. Increasing this value generates broader coverage but may extend processing time.

</td></tr><tr><td>

Remapping eligibility threshold

</td><td>

The minimum ratio of incidents to group size required for a group to be eligible for remapping. The default is 0.2, which represents 20% of the group size. Higher values result in more selective remapping.

 **Example:** If set to 0.2, a group must contain at least 20% of the expected group size before it is eligible for remapping. Increasing this value limits remapping to only well-populated groups, reducing noise from small or transient clusters.

</td></tr><tr><td>

Default resolution steps filter

</td><td>

A condition builder filter that determines which automation opportunities are eligible for resolution step generation. The default filter is `automation_priority=40`, which corresponds to Critical priority. Update the filter using the condition builder to change the priority scope.

 **Example:** The default value `automation_priority=40` limits resolution step generation to critical priority automation opportunities. Modify the condition to include additional priority levels as needed.

</td></tr></tbody>
</table>