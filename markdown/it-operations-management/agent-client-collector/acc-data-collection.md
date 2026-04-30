---
title: Agent Client Collector data collection tables
description: Agent Client Collector performs data collection based on the scoped apps that you've installed. Agent Client Collector Framework performs basic data collection, and Agent Client Collector for Visibility - Content performs enhanced data collection.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector data collection tables

Agent Client Collector performs data collection based on the scoped apps that you've installed. Agent Client Collector Framework performs basic data collection, and Agent Client Collector for Visibility - Content performs enhanced data collection.

The Refresh Host Data for Agents scheduled job collects host data every hour on hosts that haven't had data collection run in the past 12 hours. The job collects the data described in the following tables.

<table id="table_chj_jd1_y5b"><thead><tr><th>

Data

</th><th>

CMDB field

</th></tr></thead><tbody><tr><td>

hostname

</td><td>

ci.name

</td></tr><tr><td>

physical memory

</td><td>

ci.ram

</td></tr><tr><td>

hardware vendor

</td><td>

ci.manufacturer

</td></tr><tr><td>

hardware model

</td><td>

ci.model\_id

</td></tr><tr><td>

CPU name

</td><td>

ci.cpu\_type

</td></tr><tr><td>

OS domain

</td><td>

ci.os\_domain

</td></tr><tr><td>

OS name

</td><td>

ci.os

</td></tr><tr><td>

OS version

</td><td>

ci.os\_version

</td></tr><tr><td>

IPv4 address

</td><td>

ci.ip\_address

</td></tr><tr><td>

Default gateway

</td><td>

ci.default\_gateway

</td></tr><tr><td>

Serial number

</td><td>

ci.serial\_number

</td></tr><tr><td>

DNS Name

</td><td>

ci.name

</td></tr><tr><td>

FQDN

</td><td>

ci.fqdn

</td></tr><tr><td>

TCP Connections

</td><td>

cmdb\_tcp

</td></tr><tr><td>

Running Processes

</td><td>

cmdb\_running\_process

</td></tr><tr><td>

Serial numbers**Note:** When collecting data from Linux hosts, `dmidecode` must be configured with `sudo` permissions to collect all serial numbers.

</td><td>

cmdb\_serial\_number

</td></tr></tbody>
</table>|Data|CMDB field|
|----|----------|
|CPU manufacturer|ci.cpu\_manufacturer|
|CPU speed|ci.cpu\_speed|
|OS arch|ci.os\_address\_width|
|CPU count|ci.cpu\_count|
|CPU core count|ci.cpu\_core\_count|
|CPU core thread|ci.cpu\_core\_thread|
|Is virtual|ci.virtual|
|Start date \(uptime\)|ci.start\_date|
|Object ID|ci.object\_id|
|TCP Connections|cmdb\_tcp|
|Running Processes|cmdb\_running\_process|

**Parent Topic:**[Agent Client Collector Framework reference](agent-client-collector-reference.md)

