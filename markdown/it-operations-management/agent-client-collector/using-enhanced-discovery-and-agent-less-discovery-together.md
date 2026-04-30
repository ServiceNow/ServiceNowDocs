---
title: Using push-based Discovery and horizontal IP-based Discovery together
description: Discovery performed by Agent Client Collector for Visibility - Content \(ACC-VC\) is compatible and can coexist with horizontal IP-based Discovery. You may have ACC installed on a given target host and still have that host as part of a horizontal IP-based Discovery schedule as well.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Using Agent Client Collector for Visibility - Content, Agent Client Collector for Visibility - Content, Agent Client Collector, IT Operations Management]
---

# Using push-based Discovery and horizontal IP-based Discovery together

Discovery performed by Agent Client Collector for Visibility - Content \(ACC-VC\) is compatible and can coexist with horizontal IP-based Discovery. You may have ACC installed on a given target host and still have that host as part of a horizontal IP-based Discovery schedule as well.

To perform Discovery by Agent Client Collector for Visibility - Content, enable the **glide.discovery.domain.name.nbt** and **glide.discovery.enable.software\_simplify** parameters. For details on these parameters, see [Discovery properties](../../discovery/reference/r_DiscoveryProperties.md).

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
</table>**Parent Topic:**[Using Agent Client Collector for Visibility - Content](acc-v-using-agent-client-collector-for-visibility.md)

