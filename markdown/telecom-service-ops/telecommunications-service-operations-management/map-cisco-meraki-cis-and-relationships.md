---
title: Mapping Cisco Meraki CIs and relationships
description: Use the Service Graph Connector \(SGC\) for Cisco Meraki to map discovered physical and logical network resources to telecom-aligned configuration item \(CI\) classes in the Configuration Management Database \(CMDB\). Service Graph Connectors support consistent service modeling, provide visibility into chassis-level components, and automate the creation of logical and physical relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/map-cisco-meraki-cis-and-relationships.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Cisco Meraki SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Mapping Cisco Meraki CIs and relationships

Use the Service Graph Connector \(SGC\) for Cisco Meraki to map discovered physical and logical network resources to telecom-aligned configuration item \(CI\) classes in the Configuration Management Database \(CMDB\). Service Graph Connectors support consistent service modeling, provide visibility into chassis-level components, and automate the creation of logical and physical relationships.

To confirm accurate CI classification and insertion, the connector uses the Robust Transform Engine \(RTE\) and Identification and Reconciliation Engine \(IRE\).

The connector classifies and relates discovered CIs using telecom-specific models based on device type, function, and chassis structure. This organization helps maintain a clean and normalized CMDB across vendors. Discovered model names from Cisco Meraki are automatically transformed into ServiceNow AI Platform standard model identifiers and categories for slot and subslot components.

## CI mapping and relationships

The following table lists the CI object types in the CMDB that can be discovered, along with their representations in the CMDB and how they relate to one another.

<table id="table_m5l_m1b_wfc"><thead><tr><th>

CMDB CI class

</th><th>

CMDB CI table

</th><th>

CMDB hierarchy

</th><th>

Object types / models

</th><th>

Description and relationships

</th></tr></thead><tbody><tr><td>

Network site

</td><td>

`cmdb_ci_ni_site`

</td><td>

CI → Site →Network Site

</td><td>

Organization network

</td><td>

-   Represents the physical location of IP routers according to their longitude, latitude, and address.
-   Network site contains IP routers and network interfaces.
-   Network site is a member of a group.

</td></tr><tr><td>

IP Camera

</td><td>

`cmdb_ci_ip_camera`

</td><td>



</td><td>

IP Camera

</td><td>

-   Represents an IP camera device discovered from a Meraki network.
-   Related to the network site.
-   Related to the network service instance.

</td></tr><tr><td>

OT industrial sensor

</td><td>

`cmdb_ci_ot_industrial_sensor`

</td><td>



</td><td>

Industrial Sensor

</td><td>

-   Represents an industrial sensor device discovered from a Meraki network.
-   Related to the network site.
-   Related to the network service instance.

</td></tr><tr><td>

IP router

</td><td>

`cmdb_ci_ip_router`

</td><td>

CI → HW →NG → IP router

</td><td>

SD-WAN Edge / network or service router is represented by the IP router

</td><td>

-   Represents the Meraki device.
-   Contains network interface CIs.
-   Contained by network sites and network service instances.
-   IP router is a member of a group.

</td></tr><tr><td>

Slot

</td><td>

`cmdb_ci_container_slot`

</td><td>

HW → Equipment → holder → Slot

</td><td>

Slot

</td><td>

-   Slot is the main device in the network hierarchy.
-   Contains slots for IP routers, IP switches, power supply units, and fans.

</td></tr><tr><td>

Subslot

</td><td>

`cmdb_ci_container_subslot`

</td><td>

HW → Equipment → holder → Slot

</td><td>

Subslot

</td><td>

-   Network card is the main device in the network hierarchy.
-   Contains IP router, IP switch subslots \(small form-factor pluggable or child cards\).

</td></tr><tr><td>

Network interface CI

</td><td>

`cmdb_ci_ni_interface`

</td><td>

Port → Network Port → Network interface

</td><td>

The list of support port models is defined in the vendor-specific network physical information.

</td><td>

-   IP router, IP switch, or wireless access point is the main device in the network hierarchy.
-   Network card within the IP router or IP switch is the primary component.
-   Represents the physical ports contained within the device \(IP router\).

</td></tr><tr><td>

Network service instance

</td><td>

`cmdb_ci_network_service_instance`

</td><td>

CI → Service instance → Network service instance

</td><td>

Network service instance

</td><td>

-   Network service instance includes IP routers and network interfaces.
-   Network site is a member of a group.

</td></tr><tr><td>

Group

</td><td>

`cmdb_ci_group`

</td><td>

CI → Group

</td><td>

Represents organization

</td><td>

Network sites and network service instance are members.

</td></tr><tr><td>

IP address CI

</td><td>

`cmdb_ci_ip_address`

</td><td>

CI → IP address

</td><td>

Represents discovered IP addresses for CIs.

</td><td>

Owned by the corresponding CI.

</td></tr></tbody>
</table>