---
title: Microsoft Dynamics 365 for Finance and Operations Spoke
description: Provides baseline actions to integrate your ServiceNow instance with Microsoft Dynamics 365 Finance and Operations. You can retrieve and process business events that are triggered in Microsoft Dynamics 365 Finance and Operations application.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-10-27"
reading_time_minutes: 5
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Microsoft Dynamics 365 for Finance and Operations Spoke

Provides baseline actions to integrate your ServiceNow instance with Microsoft Dynamics 365 Finance and Operations. You can retrieve and process business events that are triggered in Microsoft Dynamics 365 Finance and Operations application.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Dynamics 365 for Finance and Operations spoke v 2.4.3 is the latest version.

## Supported versions

This spoke was built for Microsoft Dynamics version: 10.0.16 PU40, but may be compatible with later versions.

## Spoke requirements

Microsoft Dynamics 365 Finance and Operations account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   IHUB Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\)
-   ServiceNow IntegrationHub Starter Pack Installer \(com.glide.hub.integrations\)
-   Explicit Roles \(com.glide.explicit\_roles\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Streaming \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Microsoft Dynamics 365 for Finance and Operations spoke provides sample flows to demonstrate automating the syncing data tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Microsoft D365 FinOps Record Sync|Synchronises data from Microsoft Dynamics 365 Finance and Operations with your ServiceNow instance.|

## Spoke subflows

The Microsoft Dynamics 365 for Finance and Operations spoke provides sample subflows to demonstrate automating Microsoft Dynamics 365 for Finance and Operations tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Create Fixed Asset Records|Creates multiple fixed asset records in Microsoft Dynamics 365 Finance and Operations.|
|Create Purchase Order and Purchase Order Lines|Creates purchase order and multiple purchase order lines in Microsoft Dynamics 365 Finance and Operations.|
|Download/Refresh Metadata|Downloads and refreshes the metadata from Microsoft Dynamics 365 Finance and Operations.|
|Update Purchase Order and Purchase Order Lines|Updates the purchase order and purchase order lines in Microsoft Dynamics 365 Finance and Operations.|

## Spoke actions

The Microsoft Dynamics 365 for Finance and Operations spoke provides actions to automate  tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Account Codes Management|Look up Account Codes Stream|Retrieves account codes from Microsoft Dynamics 365 Finance and Operations.|
|Delivery Location Management|Look up Delivery Location Stream|Retrieves delivery locations from Microsoft Dynamics 365 Finance and Operations.|
|Fixed Asset Management|Create Fixed Assets|Creates fixed asset records in Microsoft Dynamics 365 Finance and Operations.|
|Item Master Management|Look up Item Master Stream|Retrieves item masters from Microsoft Dynamics 365 Finance and Operations.|
|Legal Entity Management|Legal Entity Management|Retrieves legal entities from Microsoft Dynamics 365 Finance and Operations.|
|Metadata Retrieval|Look up Choices Metadata|Retrieves the choices values from Microsoft Dynamics 365 Finance and Operations.|
|Look up Creatable Fields Metadata|Retrieves creatable fields for an entity from Microsoft Dynamics 365 Finance and Operations.|
|Look up Editable Entities Metadata|Retrieves editable entities from Microsoft Dynamics 365 Finance and Operations.|
|Look up Entity Filter Metadata|Retrieves filter fields of an entity from Microsoft Dynamics 365 Finance and Operations.|
|Look up Navigation Properties Metadata|Retrieves navigation prosperities of an entity Microsoft Dynamics 365 Finance and Operations.|
|Look up OData Metadata|Retrieves metadata document from Microsoft Dynamics 365 Finance and Operations.|
|Look up Readable Entities Metadata|Retrieves all readable entities from Microsoft Dynamics 365 Finance and Operations.|
|Look up Record Schema Metadata|Retrieves the schema table of a record from Microsoft Dynamics 365 Finance and Operations.|
|Look up Related Record Schema Metadata|Retrieves schema of a related entity from Microsoft Dynamics 365 Finance and Operations.|
|Look up Updatable Fields Metadata|Retrieves updatable fields of an entity from Microsoft Dynamics 365 Finance and Operations.|
|Purchase Order Management|Create Purchase Order|Creates a purchase order record from Microsoft Dynamics 365 Finance and Operations.|
|Create Purchase Order Line|Creates a purchase order line record from Microsoft Dynamics 365 Finance and Operations.|
|Record Management|Create Record|Creates a record in Microsoft Dynamics 365 Finance and Operations.|
|Delete Record|Deletes a record in Microsoft Dynamics 365 Finance and Operations.|
|Look up Record by Business Keys|Retrieves details of a record for the specified business key from Microsoft Dynamics 365 Finance and Operations.|
|Look up Records by Search Query|Retrieves records for the specified search query from Microsoft Dynamics 365 Finance and Operations.|
|Look Up Records Stream|Retrieves records of a table through data streaming from Microsoft Dynamics 365 Finance and Operations.|
|Look up Related Records|Retrieves the related records of an entity from Microsoft Dynamics 365 Finance and Operations.|
|Update Record|Updates the specified record in Microsoft Dynamics 365 Finance and Operations.|
|Supplier Management|Look up Suppliers Stream|Retrieves suppliers information from Microsoft Dynamics 365 Finance and Operations.|

## Spoke module

The Microsoft Dynamics 365 for Finance and Operations spoke adds the  application to your instance and includes these modules:

<table id="table_epl_vq5_drb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Microsoft D365 FinOps Metadata

</td><td>

Displays the details of all the Microsoft Dynamic 365 Finance and Operations entities.**Note:** The **Look up Updatable Fields Metadata** and **Look up Creatable Fields Metadata** actions use the entity records from this module to create dynamic input fields.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Microsoft Dynamics 365 for Finance and Operations spoke](../task/setup-msdynamics365-fin-ops.md#).

