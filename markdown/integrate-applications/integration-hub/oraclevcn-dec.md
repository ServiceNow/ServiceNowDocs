---
title: Oracle Virtual Cloud Network Spoke
description: Manage networks, route tables, security lists, and subnets in Oracle Virtual Cloud Network account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle Virtual Cloud Network Spoke

Manage networks, route tables, security lists, and subnets in Oracle Virtual Cloud Network account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle Virtual Cloud Network spoke v1.0.4 is the latest version.

## Supported versions

This spoke was built for Oracle Virtual Cloud Network API version 20160918, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Oracle Cloud IAM Spoke](oracle-iam-1.md)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Oracle Virtual Cloud Network spoke provides actions to automate Oracle Virtual Cloud Network tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Network Management|Change Network Compartment|Moves the specified VCN to a different compartment within the same tenancy.|
|Create Network|Creates a virtual cloud network.|
|Delete Network|Delete the specified VCN.|
|Get Network|Retrieves details of the required VCN.|
|Look up Networks|Lists the VCNs in the specified compartment.|
|Update Network|Updates details of the specified VCN.|
|Route Table Management|Change Route Table Compartment|Moves a route table to different compartment within the same tenancy.|
|Create Route Table|Creates a route table for the specified VCN.|
|Delete Route Table|Delete the specified route table.|
|Get Route Table|Retrieves the specified route table details.|
|Look up Route Tables|Lists the route table in the specified compartment.|
|Update Route Table|Updates details of the specified route table.|
|Security List Management|Change Security List Compartment|Moves the specified security list to different compartment within the same tenancy.|
|Create Security List|Creates a security list for the specified VCN.|
|Delete Security List|Deletes the specified security list.|
|Get Security List|Retrieves specified security list's information.|
|Look up Security Lists|Lists the security lists in the specified compartment.|
|Update Security List|Updates display name or rules of the specified security list.|
|Subnet Management|Change Subnet Compartment|Moves the specified subnet to a different compartment within the same tenancy.|
|Create Subnet|Creates a subnet in the specified VCN.|
|Delete Subnet|Deletes the specified subnet.|
|Get Subnet|Retrieves details of the specified subnet.|
|Look up Subnets|Lists the subnets in the specified compartment.|
|Update Subnet|Updates subnet in the specified VCN.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Oracle Virtual Cloud Network spoke](../task/oraclevcn-setup-dec.md).

