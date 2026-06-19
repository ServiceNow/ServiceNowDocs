---
title: Configuring Discovery
description: Configure the elements that Discovery requires to investigate your network, such as credentials, schedules, and IP addresses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/c\_DiscoveryConfiguration.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Discovery, ITOM Visibility, IT Operations Management]
---

# Configuring Discovery

Configure the elements that Discovery requires to investigate your network, such as credentials, schedules, and IP addresses.

## Configuration overview

Discovery can run on a regular, configurable schedule, or can be launched manually. The IP address ranges you provide tell Discovery which specific devices to investigate. To retrieve useful information, Discovery needs credentials for devices within a particular range, so that Discovery can connect to and run various probes on the devices it finds. Discovery compares the devices it finds with configuration items \(CI\) in the CMDB and updates any matching devices. If Discovery does not find a matching CI in the CMDB, it creates a CI.

## Discovery configuration procedures

Use the following links to configure Discovery for your environment. You don't need to perform all these procedures to run a Discovery. The platform provides many defaults you can use to explore your network that are suitable for most discoveries. To get started quickly with Discovery, you can use the ITOM Configuration Console, which offers a faster way to install and update apps, with interactive configuration pages, task assignment, and automated implementation by Now Assist. For more information, see [ITOM Configuration Console for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/itom-conf-console.md).

<table id="table_c4r_ztp_2cb"><tbody><tr><td>

[Discovery IP address configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-ip-address-configuration.md)

</td><td>

[Discovery classifiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-classifiers.md)

</td><td>

[Discovery status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_DiscoveryStatus.md)

</td></tr><tr><td>

[Domain Separation and Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_DiscoveryDomainSeparation.md)

</td><td>

[Discovery classification parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/classification-parameters.md)

</td><td>

[Discovery Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_DiscoveryConfigurationConsole.md)

</td></tr><tr><td>

[SNMP support for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_SNMPSupportForDiscovery.md)

</td><td>

[Discovery identifiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_DiscoveryIdentifiers.md)

</td><td>

 

</td></tr><tr><td>

[Discovery and SCCM together](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_DiscoveryAndSCCMTogether.md)

</td><td>

[Discovery properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/r_DiscoveryProperties.md)

</td><td>

[Discovery Home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-home-page.md)

</td></tr></tbody>
</table>