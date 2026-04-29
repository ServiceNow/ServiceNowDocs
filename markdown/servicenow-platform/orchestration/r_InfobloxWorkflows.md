---
title: Infoblox workflows
description: The Infobox DDI activity pack includes two default workflows, one that reserves and registers IP addresses and another that releases IP addresses.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Infoblox DDI activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Infoblox workflows

The Infobox DDI activity pack includes two default workflows, one that reserves and registers IP addresses and another that releases IP addresses.

To access these workflows, navigate to **Workflow** &gt; **Workflow Editor** and select the **Workflows** tab. Click on a workflow to open it, and then click the information icon in the workflow header to display the properties dialog box.

## Infoblox Reserve/Register IP in IPAM

Use this workflow to register IPv4 addresses or request the next available IP address on IPAM. Optionally, you can use it to register IP addresses on DNS. The custom Infoblox activities used in this workflow are:

-   [IPAM Register IP Address](../concept/c_InfobloxIPAMActivities.md#)
-   [IPAM Reserve IP Address](../concept/c_InfobloxIPAMActivities.md#)
-   [Register DNS A-Record](../concept/c_InfobloxDNSActivities.md#)
-   [Get Network Details](../concept/c_InfobloxNetworkActivities.md#)

|Field|Description|
|-----|-----------|
|Infoblox Server|IP address of the Infoblox DDI server.|
|Network|Network containing the target IP address.|
|Zone|The DNS zone for the IP address being registered.|
|Rest Credentials|The sys\_id of the REST credentials from the ServiceNow instance.|
|DNS Host Name|Name of the DNS server machine on which the IP address is being registered.|
|IPv4 Address|IP address being reserved or registered.|

## Infoblox Release IPAM Reservations

Use this workflow to release \(delete\) all the IPAM reservations associated with an IPv4 address. The custom Infoblox activities used in this workflow are:

-   [IPAM List IP Reservations](../concept/c_InfobloxIPAMActivities.md#)
-   [List DNS Record](../concept/c_InfobloxDNSActivities.md#)
-   [DNS Delete](../concept/c_InfobloxDNSActivities.md#)
-   [IPAM Delete](../concept/c_InfobloxIPAMActivities.md#)

|Field|Description|
|-----|-----------|
|Rest Credentials|The sys\_id of the REST credentials from the ServiceNowinstance.|
|IP to Delete|IP address to release.|
|Infoblox Server|IP address of the Infoblox DDI server.|

**Parent Topic:**[Infoblox DDI activity pack](../concept/c_InfobloxDDIActivityPack.md)

