---
title: Adobe Experience Platform Spoke
description: Automate the process of managing datasets and entities in Adobe Experience Platform from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Adobe Experience Platform Spoke

Automate the process of managing datasets and entities in Adobe Experience Platform from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Adobe Experience Platform spoke v2.1.1 is the latest version.

## Supported versions

This spoke was built for Adobe Experience Platform released on September 10, 2019, but may be compatible with later versions.

## Spoke requirements

-   Registered Adobe ID account
-   User with developer access
-   Details such as API key and client secret

See the [Adobe Experience Platform documentation](https://www.adobe.io/apis/experienceplatform/home.html) for instructions on creating Adobe ID and adding developer.

## Spoke actions

The Adobe Experience Platform spoke provides actions manage datasets and entities when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Dataset Management|Get All Data Inlets|Retrieves the details of all data inlets.|
|Get All Datasets|Retrieves the details of all datasets.|
|Get All Union Schemas|Retrieves the list of all schemas that are part of unions.|
|Entity Management|Get Entity Information|Retrieves the information of an entity as a dynamic object.|
|Load Entity Data|Ingest the information of an entity to Adobe Experience Platform.|
|Metadata Retrieval|Get Metadata For All Attributes In A Schema|Retrieves all attributes for the selected union schema.|
|Get All Sandboxes|Retrieves information about all active sandboxes.|
|Get Metadata For All Data Inlets|Retrieves the metadata of all data inlets.|
|Get Metadata For All Datasets|Retrieves the metadata of all datasets.|
|Get Metadata For All Fields In A Union|Retrieves the metadata of all fields in the selected union.|
|Get Metadata For All Identity Fields|Retrieves the metadata of all identity fields or namespaces.|
|Get Metadata For All Union Schemas|Retrieves the list of all schemas that are part of unions.|
|Get Metadata For All Unions|Retrieves the metadata of all union views.|
|Get Metadata For Union Schema|Retrieves schema for the selected fields of a union.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Note:** Two connection and credential alias records are needed for the Adobe Experience Platform spoke; one for data inlet management and batch ingestion, and other for data collection. Each alias should be associated with the respective Adobe Experience Platform API.

For information about setting up the spoke, see [Set up Adobe Experience Platform spoke](../task/setup-aep-spoke.md#).

