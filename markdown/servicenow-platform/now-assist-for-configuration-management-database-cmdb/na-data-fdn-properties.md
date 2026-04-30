---
title: Property settings for Now Assist for CMDB agentic workflows
description: List of sys properties for the agents used by Now Assist for CMDB agents.
locale: en-US
release: xanadu
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-05-02"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist for Configuration Management Database \(CMDB\), Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Property settings for Now Assist for CMDB agentic workflows

List of sys properties for the agents used by Now Assist for CMDB agents.

## Property settings

<table id="table_m2p_xvj_q2c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cmdb\_gen\_ai.principal\_class\_suggestion\_period

</td><td>

The CMDB data governance manager agentic workflow collects and aggregates Change Management, Incident Management, and Problem Management data for the specified CI class. If the workflow collects too much data, the process might fail. This property limits the duration in days \(integer zero to infinity\) for the query.

 **REVIEWERS**: Is &lt;blank&gt;==infinity?

 **REVIEWERS**: It seems that this description would be more accurate and helpful if we specified that it is the CMDB principal class manager AI agent that is collecting the data, and not the agentic workflow. Same for the next property. What do you think?

 Default 90 \(query all tasks updated in the last 90 days\).

 For instances with little data, set the property to a high value like 36000 \(10 years\). For instances with a large store of data, experiment to determine a practical value.

</td></tr><tr><td>

sn\_cmdb\_gen\_ai.health\_ownership\_evaluation\_period

</td><td>

If the CMDB data governance manager agentic workflow collects too much health data, the process might fail. This property limits the duration in days \(integer zero to infinity\) for the query.

 **REVIEWERS**: Is &lt;blank&gt;==infinity?

 Default 90 \(query all tasks updated in the last 90 days\).

</td></tr><tr><td>

sn\_cmdb\_gen\_ai.ownership\_evaluation\_health\_score\_thresholds

</td><td>

The CMDB data governance agentic workflow determines the percentage of CIs in the specified class that have values for the **Owned by** setting.

 The process returns a score that depends on this property setting. For example, the default setting of `40,60,80` returns a score of `Poor` for less than 40%, `Average` for 60%-79%, and `Healthy` for 80% and above.

</td></tr></tbody>
</table>