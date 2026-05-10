---
title: Using push-based Discovery and horizontal IP-based Discovery together
description: Discovery performed by Agent Client Collector for Visibility - Content \(ACC-VC\) is compatible and can coexist with horizontal IP-based Discovery. You may have ACC installed on a given target host and still have that host as part of a horizontal IP-based Discovery schedule as well.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [ACC Discovery, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Using push-based Discovery and horizontal IP-based Discovery together

Discovery performed by Agent Client Collector for Visibility - Content \(ACC-VC\) is compatible and can coexist with horizontal IP-based Discovery. You may have ACC installed on a given target host and still have that host as part of a horizontal IP-based Discovery schedule as well.

To avoid conflicts, ACC-VC does not perform Discovery when the target host’s IP already has a CI that has been discovered by horizontal IP-based Discovery \(discovery\_source is ServiceNow\). To override this behavior, set the system property \[**sn\_agent.disco\_disable\_ci\_clobber\_of\_agentless\_disco**\] to false. This setting is ignored if horizontal IP-based Discovery was not performed over a specific time. Update the system property \[**sn\_agent.disco\_ci\_clobber\_of\_agentless\_disco\_threshold\_days**\] if necessary. The default is 14 days. See [System properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md) for more details.

To enable Discovery using Agent Client Collector, enable the following Discovery properties on the Discovery properties page \(**All** &gt; **Discovery Definition** &gt; **Properties**\):

<table id="table_vsm_bjb_4fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.discovery.domain.name.nbt

</td><td>

Set OS domain name by NBT or WMI. If set to **true**, Windows domain name is set by NBT. Otherwise it’s set by WMI.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.enable.software\_simplify

</td><td>

Enables cleanup for software’s name and version. If set to **true**, it removes any appended version or commonly found phrases from the name and removes leading 0s in the version. If set to **false**, raw data is persisted in the table. Use with the **glide.discovery.enable.software\_simplify\_sccm** property to avoid software data discrepancy between Discovery and SCCM.-   Type: true \| false
-   Default value: true

 **Note:** Once the property is set to **false**, to disable the cleanup, duplicate records are generated for a given software. Name and Version are the primary identifiers.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Client Collector Discovery](acc-discovery.md)

