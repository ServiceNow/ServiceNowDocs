---
title: Oracle NetSuite Spoke
description: Automate create, read, update, and delete \(CRUD\) record management operations in Oracle NetSuite from your ServiceNow instance by using the Oracle NetSuite spoke. It provides preconfigured actions, subflows, connection and credential aliases, and scripted REST APIs to do these operations.Also reuse this short description in the release notes.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-06"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle NetSuite Spoke

Automate create, read, update, and delete \(CRUD\) record management operations in Oracle NetSuite from your ServiceNow instance by using the Oracle NetSuite spoke. It provides preconfigured actions, subflows, connection and credential aliases, and scripted REST APIs to do these operations.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle NetSuite spoke v1.0.3 is the latest version.

## Supported versions

This spoke was built for Oracle NetSuite API version 1.0, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.object\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The Oracle NetSuite spoke provides sample subflows to demonstrate automating Oracle NetSuite tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Get Record Details \(Inbound\)​|Triggers the 'Look up Record Details' action. The output of the action is logged for reference. You can replace the logging step with custom logic, such as creating records in a desired table, depending on the requirement to store record details.​|
|Create Purchase Order \(Outbound\)​|Triggers the 'Create Record' action of the Oracle NetSuite Spoke. Required data is provided through subflow inputs, and all fields are structured exactly as per the API requirements. All subflow inputs are passed directly to the action, except for one: the input of type Array of Objects is converted to a string using the OracleNetsuiteUtils.stringifyArray\(array\) method before being passed. This method should be used for all Array of Object type inputs.​|

## Spoke actions

The Oracle NetSuite spoke provides actions to automate Oracle NetSuite tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Record Management|Create Record|Creates a record corresponding to an object in Oracle NetSuite. For example, create a new record for the object: “purchaseOrder”.|
|Delete Record|Delete a record corresponding to an object in Oracle NetSuite. For example, delete a record for the object: “account”.|
|Look up Record Details|Retrieves any type of record details from Oracle NetSuite.|
|Update Record|Updates a record corresponding to an object in Oracle NetSuite. For example, update a record for the object: "purchaseOrder".|
|Look up Record List Stream|Retrieves the list for a given record or object from Oracle NetSuite. For example, retrieve the list of all purchaseOrder\(s\).|
|Metadata Retrieval|Get Objects \(Metadata\)|Retrieves the list of all records or objects from Oracle NetSuite.|
|Get Object Schema \(Metadata\)|Retrieves all schema or fields related data from Oracle NetSuite for a given object.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.



For information about setting up the spoke, see [Set up Oracle NetSuite Spoke](../task/set-up-oracle-netsuite-spoke.md#).

