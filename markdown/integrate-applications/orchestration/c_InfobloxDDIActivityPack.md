---
title: Infoblox DDI activity pack
description: This activity pack supports Infoblox DDI management through ServiceNow Orchestration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/orchestration/c\_InfobloxDDIActivityPack.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Infoblox DDI activity pack

This activity pack supports Infoblox DDI management through ServiceNow Orchestration.

The Infoblox DDI activity pack manages the IP addresses used in a network by integrating DNS and DHCP. Custom Orchestration activities use Infoblox Web API \(WAPI\) REST web services to access the Infoblox GRID server.

**Important:** Managing IP addresses through the Infoblox server requires a fully functional MID Server.

Starting with the Jakarta release, the Infoblox activity pack updates to version 2. This update supports Infoblox network views, which can restrict the visibility of network data. The view parameter can be passed as a query parameter or payload content, to do operations in a specific view. Version 2 also supports specifying the version of WAPI to use in integration endpoints.

Supported for Infoblox:

-   WAPI version 2.0 for REST messages
-   NIOS appliance version 7.0

**Note:** To use the Infoblox DDI activities and workflow, you must [request activation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_ActivateAnActivityPack.md) of the Orchestration - Infoblox DDI Activty Pack plugin.

-   **[Create a REST credential for Infoblox activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/t_CreateRESTCredRecInfoBloxAct.md)**  
All Infoblox activities require a REST credential to manage IP addresses from the Infoblox DDI server.
-   **[Infoblox workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/r_InfobloxWorkflows.md)**  
The Infobox DDI activity pack includes two default workflows, one that reserves and registers IP addresses and another that releases IP addresses.
-   **[Infoblox roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/infoblox-roles-permissions.md)**  
Define the roles and permissions that the Infoblox activities need to access the various resources on the Infoblox server.
-   **[Infoblox DHCP activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_InfobloxDHCPActivities.md)**  
The Infoblox DHCP activities manage the IP addresses reserved for DHCP in your network.
-   **[Infoblox DNS activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_InfobloxDNSActivities.md)**  
The Infoblox DNS activities manage DNS records in your network using an Infoblox DDI Grid Server.
-   **[Infoblox IPAM activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_InfobloxIPAMActivities.md)**  
The Infoblox IPAM activities manage IP addresses in your network using an Infoblox DDI Grid Server.
-   **[Infoblox network activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_InfobloxNetworkActivities.md)**  
The Infoblox network activities manage networks using an Infoblox DDI Grid Server.

**Parent Topic:**[Orchestration activity packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/orchestration/c_OrchestrationActivityPacks.md)

