---
title: Infoblox Spoke
description: Automate network management tasks in Infoblox from your ServiceNow instance. For example, register or delete IP addresses on an Infoblox server.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Infoblox Spoke

Automate network management tasks in Infoblox from your ServiceNow instance. For example, register or delete IP addresses on an Infoblox server.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Infoblox spoke v2.0.4 is the latest version.

## Supported version

Infoblox versions 2.7, 2.11 and may be compatible with other future API versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   Remote Tables plugin \(com.glide.script.vtable\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Infoblox spoke provides sample flows in the draft state to automate allocating IP addresses in the Infoblox grid server. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Infoblox Register or Reserve IP in IPAM|Registers or reserves an IP address in Infoblox based on a Service Catalog item request.|

## Spoke subflows

The Infoblox spoke provides sample subflows to register and reserve IP addresses.

|Flow|Description|
|----|-----------|
|Register AName Record and Get Network Details|Registers an AName record type in the DNS server and retrieves network details such as network options and ID.|
|Process Inbound Notifications from Infoblox|Receives the inbound notifications from Infoblox and logs the details.|

## Spoke module

The Infoblox spoke adds the Infoblox application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|CName Records|Lists all the CName records.|
|Webhook Registry|Lists all the webhook registries for the spoke.|

## Spoke actions

The Infoblox spoke provides actions to manage IP addresses and networks in Infoblox from your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|DHCP Management|Delete IP Reservation|Deletes IP address range from an Infoblox server.|
|Look up IP Address Reservation|Lists IP address reservation in the DHCP server for a given Infoblox network view.|
|Reserve IP Address Range|Reserves an IP address range in the Infoblox server.|
|DNS Management|Add IPs to Host Record|Adds the specified list of IPs to the existing IP addresses in the specified host record.|
|Change IPs of Host Record|Replaces the IP addresses of the specified host record with the new list of IPs.|
|Create Host Record|Creates a host record in Infoblox.|
|Delete DNS Record|Deletes a DNS record in the Grid Server.|
|Look up CName Records|Lists CName records present in the Infoblox server.|
|Look up DNS Records|Lists DNS records present in the Infoblox server.|
|Look up Host Record by Reference|Retrieves the details of the specified host record.|
|Look up Host Records Stream|Retrieves the details of all host records.|
|Register AName Record|Registers an AName record type in DNS server. An AName record stores mapping between the fully qualified domain name and the IP address.|
|Register CName Record|Registers a CName record in the Infoblox DNS Server. A CName record is an alias to the fully qualified domain name.|
|Update AName Record|Updates the properties of the specified AName record.|
|Update CName Record|Updates the properties of the specified CName record.|
|Update Host Record|Updates the properties of specified host record.|
|Generic|Create Record|Creates a record in Infoblox for the specified object.|
|Delete Record|Deletes the specified record.|
|Look up Record by Reference|Retrieves the details of the specified record.|
|Look up Records by Criteria Stream|Retrieves the details of all records for the specified schema object.|
|Look up Records Stream|Retrieves the details of all records of the specified object type.|
|Update Record|Updates a record in Infoblox for the specified object.|
|IPAM Management|Delete IPAM IP Address Reservation|Deletes an IPAM IP address Reservation in Infoblox.|
|Look up IPAM Reservations|Lists the IP addresses within a given Infoblox Server.|
|Register IPAM IP Address|Registers the IP addresses within a given Infoblox Server.|
|Reserve IPAM IP Addresses|Reserves the IP addresses within a given Infoblox Server.|
|Metadata Retrieval|Look up Definition of Extensible Attributes|Retrieves the definitions of the extensible attributes.|
|Look up Object Metadata|Retrieves the list of all supported fields for a given operation for the specified schema object.|
|Look up Overall WAPI Metadata|Retrieves the list of all supported objects in the configured API version.|
|Network Management|Create Network|Creates a network within a given Infoblox Server.|
|Delete Network|Deletes a network within a given Infoblox Server.|
|Look up Network Details|Retrieves the network details within a given InfoBlox Server.|
|Update Network|Updates the network within a given Infoblox Server.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the Infoblox alias record to authorize actions.

<table id="table_nnk_g2h_gfb"><thead><tr><th>

Connection &amp; Credential alias

</th><th>

Description

</th><th>

Connection alias requirements

</th></tr></thead><tbody><tr><td>

Infoblox

</td><td>

Connection to Infoblox server

</td><td>

-   Connection type: HTTP
-   Connection URL: URL of the host machine where the Infoblox server is installed.

</td></tr></tbody>
</table>To use the spoke connection alias, create an associated Connection record and an associated Credential record. For information about setting up the spoke, see [Set up the Infoblox spoke](../task/set-up-infoblox.md#).

## MID Server requirements

These actions use REST calls, which must run on a MID Server. Use the connection record associated with the Infoblox alias to configure where actions run as well as set MID Server selection attributes. For more information, see [MID server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

