---
title: Configuring Discovery
description: Configure the elements that Discovery requires to investigate your network, such as credentials, schedules, and IP addresses.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Discovery, ITOM Visibility, IT Operations Management]
---

# Configuring Discovery

Configure the elements that Discovery requires to investigate your network, such as credentials, schedules, and IP addresses.

## Configuration overview

Discovery can run on a regular, configurable schedule, or can be launched manually. The IP address ranges you provide tell Discovery which specific devices to investigate. To retrieve useful information, Discovery needs credentials for devices within a particular range, so that Discovery can connect to and run various probes on the devices it finds. Discovery compares the devices it finds with configuration items \(CI\) in the CMDB and updates any matching devices. If Discovery does not find a matching CI in the CMDB, it creates a CI.

## Discovery configuration procedures

Use the following links to configure Discovery for your environment. You do not need to perform all these procedures to run a Discovery. The platform provides many defaults you can use to explore your network that are suitable for most discoveries. To get started quickly with Discovery, you can use Guided Setup, which expedites the setup of a basic Discovery.

<table id="table_c4r_ztp_2cb"><tbody><tr><td>

[Discovery IP address configuration](../reference/discovery-ip-address-configuration.md#)

</td><td>

[Discovery classifiers](discovery-classifiers.md)

</td><td>

[Discovery status](c_DiscoveryStatus.md)

</td></tr><tr><td>

[Domain Separation and Discovery](c_DiscoveryDomainSeparation.md)

</td><td>

[Discovery classification parameters](../reference/classification-parameters.md)

</td><td>

[Discovery Configuration Console](c_DiscoveryConfigurationConsole.md#)

</td></tr><tr><td>

[SNMP support for Discovery](c_SNMPSupportForDiscovery.md#)

</td><td>

[Discovery identifiers](c_DiscoveryIdentifiers.md)

</td><td>

 

</td></tr><tr><td>

[Discovery and SCCM together](c_DiscoveryAndSCCMTogether.md#)

</td><td>

[Discovery properties](../reference/r_DiscoveryProperties.md)

</td><td>

[Discovery Home page](discovery-home-page.md#)

</td></tr></tbody>
</table>