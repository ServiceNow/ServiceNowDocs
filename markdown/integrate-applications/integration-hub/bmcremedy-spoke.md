---
title: BMC Remedy Spoke
description: Manage change requests, incidents, problems, and other records in BMC Remedy from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# BMC Remedy Spoke

Manage change requests, incidents, problems, and other records in BMC Remedy from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

BMC Remedy spoke v1.4.1 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for BMC Remedy AR server version 19.08, but may be compatible with later versions.

## Spoke flows

The BMC Remedy spoke provides the Look up Record sample flow to demonstrate retrieving the details of records based on last modified date. To customize the sample flow, copy it to the required application scope.

## Spoke subflows

The BMC Remedy spoke provides the Get Incident Request ID sample subflow to demonstrate retrieving the Request IDs of the specified incident numbers. To customize the sample subflow, copy it to the required application scope.

## Spoke actions

The BMC Remedy spoke provides actions to perform BMC Remedy tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Change Management|Create Change|Creates a change request in BMC Remedy.|
|CMDB Management|Get Class Attributes|Retrieves class attributes schema from BMC Remedy.|
|Get Classes|Retrieves the list of all non-abstract classes in the BMC Remedy CMDB.|
|Get Datasets|Retrieves the list of all datasets in BMC Remedy CMDB.|
|Get Namespace|Retrieves the list of all namespaces in BMC Remedy CMDB.|
|Look up CMDB Data|Get All Incidents all CMDB data for specified dataset, namespace, and class from BMC Remedy.|
|Incident Management|Create Incident|Creates an incident in BMC Remedy.|
|Get All Incidents|Retrieves details of all incidents from BMC Remedy.|
|Update Attachment|Updates the attachment of the required incident in BMC Remedy.|
|Get Incident By Number|Retrieves details of the specified incident.|
|Metadata Retrieval|Get All Objects|Retrieves name and label of all objects in BMC Remedy.|
|Alias Selector|Validates the given alias specific to the BMC Remedy spoke and retrieves the alias if it is valid.|
|Get Change Form Fields|Retrieves the list of fields in the Change Interface form table.|
|Get Change Status|Retrieves the list of all statuses in the BMC Remedy Change Management.|
|Get Change Timing|Retrieves the list of all change timings in BMC Remedy Change Management.|
|Get Creatable Fields|Retrieves the list of creatable fields in a required standard or custom BMC Remedy table.|
|Get Creatable Objects|Retrieves the list of creatable objects in BMC Remedy.|
|Get Impact|Retrieves the list of all impacts in the BMC Remedy.|
|Get Incident Form Fields|Retrieves the list of fields in the Incident Interface form table.|
|Get Incident Status|Retrieves the list of all statuses in BMC Remedy Incident Management.|
|Get Investigation Driver|Retrieves the list of all investigation drivers in BMC Remedy Problem Management.|
|Get Object Schema|Retrieves schema of the specified object in BMC Remedy.|
|Get Problem Form Fields|Retrieves the list of fields in the Problem Interface form table.|
|Get Problem Status|Retrieves the list of all statuses in BMC Remedy Problem Management.|
|Get Queryable Fields|Retrieves the list of updatable fields in a required standard or custom BMC Remedy table.|
|Get Reported Source|Retrieves the list of all reported sources in BMC Remedy Incident Management.|
|Get Risk Level|Retrieves the list of all risk levels in BMC Remedy Change Management.|
|Get Service Type|Retrieves the list of all service types in BMC Remedy Incident object.|
|Get Token|Generates access token for BMC Remedy.|
|Get Updatable Fields|Retrieves the list of updatable fields in the required standard or custom BMC Remedy table.|
|Get Urgency|Retrieves the list of all urgencies in BMC Remedy.|
|Problem Management|Create Problem|Creates a problem in BMC Remedy.|
|Record Management|Create Record|Creates record of the required type in BMC Remedy.|
|Get Record Details By ID|Retrieves details of the specified record.|
|Look up Record|Looks up a record in BMC Remedy based on the query fields.|
|Update Record|Updates details of the specified record in BMC Remedy.|
|Service Request Management|Create Service Request|Creates a service request in BMC Remedy.|
|Get Service Request Form Fields|Retrieves the list of fields in the Service Request Interface form table.|
|Get Service Request Status|Retrieves the list of all status in the BMC Remedy Service Request management.|

## Spoke modules

The BMC Remedy spoke adds a BMC Remedy application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Credentials|Credential records for the BMC Remedy spoke can be accessed here.|
|Objects|Information about the objects in BMC Remedy can be accessed here. You can also create an object that can be used in your flows. See [Create a BMC Remedy object in your ServiceNow instance](../task/create-obj-bmc.md) for information about creating an object.|

## Spoke user roles

The Remedy\_Admin \(sn\_bmcremedy\_spoke.Remedy\_Admin\) is available when the BMC Remedy spoke is installed. Users with role can view and create objects in the Objects module.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

Two aliases are available when you install the BMC Remedy spoke; one alias is of the **Connection and Credential** type and the other alias is of the **Credential** type. For information about setting up the spoke, see [Set up the BMC Remedy spoke](../task/setup-bmc.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the BMC Remedy alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

