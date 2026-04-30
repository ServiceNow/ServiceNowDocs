---
title: Agent Client Collector data collection properties
description: Description of the properties that determine the behavior of Agent Client Collector data collection.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector data collection properties

Description of the properties that determine the behavior of Agent Client Collector data collection.

<table id="table_pxw_szk_xyb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_agent.host-data\_collection\_refresh\_duration\_seconds**

</td><td>

The amount of time \(in seconds\) between agent data collections on the host. Applicable only when no host CI is assigned to the agent.Default: 43200 \(12 hours\)

</td></tr><tr><td>

**sn\_agent.disco\_minimum\_threshold\_for\_rediscovery\_minutes**

</td><td>

The minimum number of minutes since the last endpoint Discovery on a given IP before Discovery can be triggered again. This property prevents running endpoint Discovery too often, such as in cases where a network intermittently has a break or a laptop is repeatedly rebooted.Default: 60

</td></tr><tr><td>

**sn\_agent.disco\_disable\_ci\_clobber\_of\_agentless\_disco**

</td><td>

When set to **true**, indicates that data collected by the ServiceWatch or ServiceNow Discovery sources takes precedence over Agent Client Collector when the threshold in the **sn\_agent.disco\_ci\_clobber\_of\_agentless\_disco\_threshold\_days** property hasn’t been exceeded.Default: true

</td></tr><tr><td>

**sn\_agent.disco\_ci\_clobber\_of\_agentless\_disco\_threshold\_days**

</td><td>

Maximum number of days since an existing CI has been discovered using agentless Discovery where the existing CI is linked instead of being rediscovered by the agent. Takes effect when **endpoint\_disco\_disable\_ci\_clobber\_of\_agentless\_disco** = **true** and over 14 days \(by default\) have passed since a non-ACC Discovery source \(such as ServiceWatch or ServiceNow\) has discovered the CI. After this threshold has been exceeded, agent Discovery can execute and overwrite an existing CI regardless of whether the CI has been previously discovered by a non-ACC Discovery source. This process presents the most recently discovered data in the CMDB.Default: 14

</td></tr><tr><td>

**sn\_agent.ci\_prefers\_ip\_version**

</td><td>

Indicates whether IPv4 or IPv6 is the preferred version when saving an IP Address value in the IP Address field of the CI record.Default: 4

</td></tr><tr><td>

**sn\_agent.ci\_serial\_number.pref\_order**

</td><td>

Specify the order of the fields to locate a serial number value to be saved to the host CI's **serial\_number** field during agent data collection. Values must be comma-separated, without spaces, and in lowercase.Default: bios,system,uuid,baseboard,chassis

</td></tr><tr><td>

**sn\_agent.mac\_ci\_name\_pref\_order**

</td><td>

Specify the order of the values by which the CI record's **Name** field is populated during macOS data collection. Values must be comma-separated, without spaces, and in lowercase.Default: name,hostname,computer\_name,local\_hostname

</td></tr><tr><td>

**sn\_agent.host\_data\_collection.disable\_when\_container**

</td><td>

When set to **true**, indicates that data collection is disabled for containerized agents.Default: true

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

