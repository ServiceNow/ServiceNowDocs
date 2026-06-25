---
title: Set the preferred IP version for network adapter discovery
description: Control which IP version Discovery populates on a Network Adapter CI during Linux, Windows, and Solaris discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/set-network-adapter-preferred-ip.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 1
breadcrumb: [Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Set the preferred IP version for network adapter discovery

Control which IP version Discovery populates on a Network Adapter CI during Linux, Windows, and Solaris discovery.

## Before you begin

Verify that you have at least version 6.32.0 of Visibility Content.

Role required: discovery\_admin

## About this task

When a network adapter supports both IPv4 and IPv6, Discovery populates the IP Address \[ip\_address\] field on the Network Adapter \[cmdb\_ci\_network\_adapter\] CI with one IP address. Before Visibility Content version 6.32.0, Discovery selected the value randomly. Starting from this release, IPv4 is populated by default. Use the **network\_adaptor\_preferred\_ip\_version** MID Server property to specify which IP version to populate.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** column, search for `network_adaptor_preferred_ip_version`.

3.  Select the **network\_adaptor\_preferred\_ip\_version** property.

4.  In the **Value** field, enter the accepted value for the IP version to populate.

    Values are case-sensitive. Use only the accepted values listed in the table.

    |IP version|Accepted values|
    |----------|---------------|
    |IPv4|ipv4, IPv4, or v4.|
    |IPv6|ipv6, IPv6, or v6.|

5.  Select **Update**.


## What to do next

Run discovery again or wait for the scheduled run to apply the changes.

**Parent Topic:**[Data collected by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/data-collected-by-itom-visibility.md)

**Related topics**  


[Linux discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoLinuxComputers.md)

[Solaris discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoSolarisComputers.md)

[Windows discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DataCollDiscoWindowsComputers.md)

