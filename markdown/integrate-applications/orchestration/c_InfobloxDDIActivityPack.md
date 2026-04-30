---
title: Infoblox DDI activity pack
description: This activity pack supports Infoblox DDI management through ServiceNow Orchestration.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Orchestration activity packs, Classic Orchestration, Creating integrations with applications]
---

# Infoblox DDI activity pack

This activity pack supports Infoblox DDI management through ServiceNow Orchestration.

The Infoblox DDI activity pack manages the IP addresses used in a network by integrating DNS and DHCP. Custom Orchestration activities use Infoblox Web API \(WAPI\) REST web services to access the Infoblox GRID server.

**Important:** Managing IP addresses through the Infoblox server requires a fully functional MID Server.

Starting with the Jakarta release, the Infoblox activity pack updates to version 2. This update supports Infoblox network views, which can restrict the visibility of network data. The view parameter can be passed as a query parameter or payload content, to do operations in a specific view. Version 2 also supports specifying the version of WAPI to use in integration endpoints.

Supported for Infoblox:

-   WAPI version 2.0 for REST messages
-   NIOS appliance version 7.0

**Note:** To use the Infoblox DDI activities and workflow, you must [request activation](../task/t_ActivateAnActivityPack.md) of the Orchestration - Infoblox DDI Activty Pack plugin.

-   **[Create a REST credential for Infoblox activities](../task/t_CreateRESTCredRecInfoBloxAct.md)**  
All Infoblox activities require a REST credential to manage IP addresses from the Infoblox DDI server.
-   **[Infoblox workflows](../reference/r_InfobloxWorkflows.md)**  
The Infobox DDI activity pack includes two default workflows, one that reserves and registers IP addresses and another that releases IP addresses.
-   **[Infoblox roles and permissions](../reference/infoblox-roles-permissions.md)**  
Define the roles and permissions that the Infoblox activities need to access the various resources on the Infoblox server.
-   **[Infoblox DHCP activities](c_InfobloxDHCPActivities.md#)**  
The Infoblox DHCP activities manage the IP addresses reserved for DHCP in your network.
-   **[Infoblox DNS activities](c_InfobloxDNSActivities.md#)**  
The Infoblox DNS activities manage DNS records in your network using an Infoblox DDI Grid Server.
-   **[Infoblox IPAM activities](c_InfobloxIPAMActivities.md#)**  
The Infoblox IPAM activities manage IP addresses in your network using an Infoblox DDI Grid Server.
-   **[Infoblox network activities](c_InfobloxNetworkActivities.md#)**  
The Infoblox network activities manage networks using an Infoblox DDI Grid Server.

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

