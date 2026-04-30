---
title: Agent Client Collector policy collection properties
description: Description of the properties that determine the behavior of Agent Client Collector policy collection.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector policy collection properties

Description of the properties that determine the behavior of Agent Client Collector policy collection.

<table id="table_uyk_vcl_xyb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_agent.full\_policy\_calculation\_cycle\_days**

</td><td>

The number of days for a policy to reach a full calculation cycle. If the policy’s last full calculation cycle was more than 7 days ago, the policy is queried to fully calculate its calculation cycle.Default: 7

</td></tr><tr><td>

**sn\_agent.max\_number\_of\_monitored\_cis\_per\_policy**

</td><td>

The maximum number of monitored CIs that can be processed per policy.Default: 400000

</td></tr><tr><td>

**sn\_agent.max\_num\_of\_monitored\_ci\_to\_process\_with\_no\_agents\_association**

</td><td>

The maximum number of monitored CIs unassociated with agents that can be processed per policy. Default: 1000

</td></tr><tr><td>

**sn\_agent.policy\_force\_recalc\_interval\_min**

</td><td>

The interval limit, in minutes, used to determine whether forced recalculation is required for any policies. Forced recalculation redistributes both a policy's monitored CIs and the corresponding agent.

Default: 10

</td></tr><tr><td>

**sn\_agent.policy\_force\_recalc\_required**

</td><td>

When set to **true**, checks whether forced recalculation is required for policies.Forced recalculation redistributes a policy's monitored CIs and the corresponding agent.

Default: true

</td></tr><tr><td>

**sn\_agent.populate\_proxy\_agent\_monitored\_ci\_distribution\_always**

</td><td>

When set to **true**, repopulates the monitored CIs for given policies to show the distribution of CIs among proxy agents.Default: false

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

