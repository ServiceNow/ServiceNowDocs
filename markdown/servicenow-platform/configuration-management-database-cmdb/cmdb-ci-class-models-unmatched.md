---
title: Unmatched API extension classes
description: The CMDB CI Class Models store app adds or updates classes for unmatched APIs \(application programming interface\).
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [API extension classes, CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Unmatched API extension classes

The CMDB CI Class Models store app adds or updates classes for unmatched APIs \(application programming interface\).

The app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships \(if applicable\). You can use the added classes as any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Unmatched APIs

API endpoints that are not structured well enough to populate the API \[cmdb\_ci\_api\] and API Component \[cmdb\_ci\_api\_component\] classes instead populate the Unmatched API Endpoint \[cmdb\_ci\_unmatched\_api\_endpoint\] class. Unmatched APIs are typically used by integrations like security scanners or observability tools.

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates.

CMDB CI Class Models: Release 1.49.0 adds the following class for unmatched API endpoints. For the list of CMDB classes in a base system, including ones that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_h2r_d5z_ryb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unmatched API Endpoint\[cmdb\_ci\_unmatched\_api\_endpoint\]

</td><td>

Configuration Item\[cmdb\_ci\]

</td><td>

APIs with unstructured endpoints that cannot populate cmdb\_ci\_api or cmdb\_ci\_api\_component.

</td></tr></tbody>
</table>## Class attributes

CMDB CI Class Models: Release 1.49.0 adds the following attributes to the Unmatched API Endpoint \[cmdb\_ci\_unmatched\_api\_endpoint\] class.

<table id="table_tqx_q3g_syb"><thead><tr><th>

Attribute

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Method

</td><td>

String

</td><td>

Backend protocol types of the API. Examples:-   Lambda
-   HTTP
-   Logic App

</td></tr><tr><td>

Protocol

</td><td>

String

</td><td>

Communication protocol. Example: HTTP, HTTPS.

</td></tr><tr><td>

URL

</td><td>

String \(1024\)

</td><td>

URL of the resource being called.

</td></tr><tr><td>

ID

</td><td>

String \(1024\)

</td><td>

Unique identifier from the source system.

</td></tr><tr><td>

Internet Facing

</td><td>

Boolean

</td><td>

Boolean that denotes whether the component is reachable from the public internet. Specify 1 or "true" if the component is reachable.

</td></tr><tr><td>

Authorization

</td><td>

String

</td><td>

Type of authorization or authentication method. Example:-   Basic
-   Key
-   Oauth
-   None

</td></tr><tr><td>

Request data types

</td><td>

String \(255\)

</td><td>

List of data types in the request. Examples:-   CC
-   Email
-   Address

</td></tr><tr><td>

Response data types

</td><td>

String \(255\)

</td><td>

List of data types in the response. Examples:-   CC
-   Email
-   Address

</td></tr></tbody>
</table>## Key Relationship Structures

The Unmatched API Endpoint \[cmdb\_ci\_unmatched\_api\_endpoint\] CMDB class and API Endpoint Discovered \[api\_endpoint\_discovered\] non-CMDB table are intended for scenarios where unstructured API data is ingested and needs to be processed beyond the capabilities of IntegrationHub-ETL.

API Endpoint Discovered \[api\_endpoint\_discovered\] can serve as a staging table for raw data for the API \[cmdb\_ci\_api\] and API Component \[cmdb\_ci\_api\_component\] classes. API data that does not come from a well-structured data source or cannot have standard identification rules applied can first populate the API Endpoint Discovered \[api\_endpoint\_discovered\] table. You can then use a customer-defined integration to ensure that well-formed data that matches the quality and condition requirements for API \[cmdb\_ci\_api\] and API Component \[cmdb\_ci\_api\_component\] populates the most appropriate table.

In cases where the data cannot be correctly parsed or is structured in an unexpected fashion, you can instead use a customer-defined integration to populate the Unmatched API Endpoint \[cmdb\_ci\_unmatched\_api\_endpoint\] table.

Data that populates the API Endpoint Discovered \[api\_endpoint\_discovered\] table is purged every 30 days.

<table id="table_tzf_mbr_tyb"><thead><tr><th>

Attribute

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

String \(100\)

</td><td>

Name of the API endpoint.

</td></tr><tr><td>

Method

</td><td>

String

</td><td>

REST API methods. Examples:-   GET
-   POST
-   DELETE

</td></tr><tr><td>

URL

</td><td>

String \(1024\)

</td><td>

URL of the resource being called.

</td></tr><tr><td>

Type

</td><td>

Choice list

</td><td>

Type of API. You can specify:-   REST
-   SOAP
-   HTTP
-   gRPC
-   GraphQL
-   Websocket

</td></tr><tr><td>

Authorization

</td><td>

String

</td><td>

Type of authorization or authentication method. Example:-   Basic
-   Key
-   OAuth
-   None

</td></tr><tr><td>

Internet Facing

</td><td>

Boolean

</td><td>

Boolean that denotes whether the component is reachable from the public internet. Specify 1 or "true" if the component is reachable.

</td></tr><tr><td>

Request Datatypes

</td><td>

String \(255\)

</td><td>

List of data types in the request. Examples:-   CC
-   Email
-   Address

</td></tr><tr><td>

Response Datatypes

</td><td>

String \(255\)

</td><td>

List of data types in the response. Examples:-   CC
-   Email
-   Address

</td></tr><tr><td>

Headers

</td><td>

String \(255\)

</td><td>

Comma-separated list of header names.

</td></tr><tr><td>

Configuration Item

</td><td>

Reference

</td><td>

Reference to a matching CMDB CI \(API Component or Unmatched API Endpoint\).

</td></tr></tbody>
</table>## Related non-CMDB tables

The Unmatched API extension class uses the API Deployment \[api\_deployment\] non-CMDB table as a related list:

|Attribute|Data type|Description|
|---------|---------|-----------|
|Name|String \(100\)|Name of the API deployment.|
|API|Reference|Reference to the deployed API \(cmdb\_ci\_api\).|
|Unmatched API Endpoint|Reference|Reference to the unmatched API endpoint, if the API doesn't match an existing API \(cmdb\_ci\_unmatched\_api\_endpoint\).|
|Configuration Item|Reference|Reference to the Configuration Item. This is typically manually specified as a reference, if you know what CI the API is deployed to.|

