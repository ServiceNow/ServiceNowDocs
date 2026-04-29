---
title: IPAM Discovery integration
description: The IP Address Management \(IPAM\) to Discovery integration feature enables your organization to automatically create and manage Discovery schedules based on your IPv6 network infrastructure data stored in IPAM. This integration keeps your discovery processes synchronized with your IPv6 network changes, providing a complete and up-to-date view of your network environment.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# IPAM Discovery integration

The IP Address Management \(IPAM\) to Discovery integration feature enables your organization to automatically create and manage Discovery schedules based on your IPv6 network infrastructure data stored in IPAM. This integration keeps your discovery processes synchronized with your IPv6 network changes, providing a complete and up-to-date view of your network environment.

## How it works

The IPAM to Discovery integration automates schedule management through the following process:

-   Identifying resources marked as operational in your IPAM tables
-   Processing only the latest changes from your IPAM system
-   Creating Discovery schedules, organized by a tag key you specify
-   Disabling schedules that no longer have valid network targets

## Benefits

The following examples highlight the primary advantages of integrating IPAM with Discovery:

-   **Automated schedule management**: Eliminates the need to manually create and maintain Discovery schedules for IPv4 and IPv6 networks.
-   **Synchronization with network changes**: Automatically adjusts Discovery schedules when networks, subnets, or IP addresses change.
-   **Incremental updates**: Processes only resources that changed since the last synchronization, improving performance.
-   **IPv4 and IPv6 support**: Handles both IPv4 and IPv6 networks with separate capacity limits and mapping approaches.
-   **Audit capability**: Maintains history of synchronization activities and changes through execution records.

## Requirements

This feature requires the following:

-   Service Graph Connector Central \(SGC Central\) v2.4.0 with sgc\_admin access.
-   Service Graph Connector for Infoblox v1.5.0 with sgc\_admin access.
-   CMDB Workspace v9.0.0.
-   Discovery Admin Workspace v1.13.0 with discovery\_admin access.
-   Australia, ZP9 or later, or YP13 or later version of the ServiceNow AI Platform.

Before using the integration, ensure that your IPAM tables contain the following data:

-   Managed networks in the Managed Network \[cmdb\_ci\_managed\_network\] table with operational status set to operational.
-   IP subnets in the IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\] table with operational status set to operational.
-   IP addresses in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table with operational status set to operational.
-   IPv4 subnets should have valid Classless Inter-Domain Routing \(CIDR\) notation for address calculation.
-   Relationships between managed networks, subnets, and IP addresses must be established.

## Configuration

The following system properties control the behavior of the integration:

<table id="table_nff_rzp_23c"><thead><tr><th>

Property name

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

glide.discovery.schedule.autogenerate.debug

</td><td>

Enables detailed logging for troubleshooting.

</td><td>

false

</td></tr><tr><td>

glide.discovery.schedule.autogenerate.group

</td><td>

Groups auto-generated IPAM Discovery schedules by a specific tag or attribute. The value of this property represents a key that IPAM retrieves and stores in the Key Values \[cmdb\_key\_value\] table. For example, entering "location" as the value would group the schedules by their associated locations.

</td><td>

empty

</td></tr><tr><td>

glide.discovery.schedule\_ipv4\_limit

</td><td>

Defines the maximum number of IPv4 addresses that can be included in a single auto‑generated IPv4 Discovery schedule.

</td><td>

65,536

</td></tr><tr><td>

glide.discovery.schedule\_ipv6\_limit

</td><td>

Defines the maximum number of IPv6 addresses that can be included in a single auto‑generated IPv6 Discovery schedule.

</td><td>

20,000 **Note:** On instances below ZP3 and YP9, the maximum number of IPv6 addresses per schedule must not exceed 5,000, which is also the default value in Yokohama and earlier releases.

</td></tr></tbody>
</table>## Generated schedules

The integration creates Discovery schedules with the following characteristics:

-   **Maintenance source**: The maintenance source is set to Discovery-IPAM Integration.
-   **Initial state**: The initial state is set to inactive for review before activation.
-   **MID Server selection**: The MID Server selection is set to MID Cluster.
-   **Description**: Includes managed network, grouping criteria, and navigation links.

## Execution tracking

Each synchronization creates an execution record that captures performance metrics, configuration settings, and any errors. The integration helps prevent multiple simultaneous executions to avoid conflicts. Review these execution records to monitor integration health.

## Optimization

Follow these guidelines to get the most out of the IPAM Discovery integration:

-   **Assign subnets to groups**: In your IPAM product, assign subnets to groups so the integration can organize schedules based on those groupings.
-   **Regular maintenance**: Periodically review generated schedules and adjust configuration as needed.
-   **Test with debug logging**: Enable debug logging during initial implementation to understand behavior.
-   **Verify data quality**: Verify IPAM data quality before running synchronization.
-   **Monitor execution records**: Review execution records regularly to catch issues early.

