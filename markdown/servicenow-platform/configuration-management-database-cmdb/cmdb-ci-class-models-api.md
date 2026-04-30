---
title: API extension classes
description: The CMDB CI Class Models store app adds or updates classes for APIs \(application programming interface\).
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-10-10"
reading_time_minutes: 6
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# API extension classes

The CMDB CI Class Models store app adds or updates classes for APIs \(application programming interface\).

The app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships \(if applicable\). You can use the added classes as any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## APIs

APIs are a set of definitions and protocols that enable computer programs to communicate with each other, which enables you to build or integrate application software. APIs typically use web-based technology to communicate with other APIs. APIs are generally used to programmatically perform jobs or tasks, or to view, import, export, delete, or modify data.

The classes added in this release extend the data model and provide a foundation for the representation of API CI classes. You can use this foundation to do the following:

-   Gain greater visibility into your APIs.
-   Identify security issues and vulnerabilities associated with an API endpoint.

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates.

CMDB CI Class Models: Release 1.49.0 adds the following classes for API. For the list of CMDB classes in a base system, including ones that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_h2r_d5z_ryb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

API\[cmdb\_ci\_api\]

</td><td>

Configuration Item\[cmdb\_ci\]

</td><td>

APIs that enable two computer programs to communicate with each other, typically using web-based technologies. Example: ChatAPI \(https://\[apiID\].execute-api.use-east-2.amazonaws.com\).

</td></tr><tr><td>

API Component\[cmdb\_ci\_api\_component\]

</td><td>

Configuration Item\[cmdb\_ci\]

</td><td>

Reusable objects related to your API definition that facilitate functionality or exchange of data. Example: GET https://\[instance\].service-now.com/api/now/table/\{tablename\}.

</td></tr><tr><td>

API Frontend\[cmdb\_ci\_api\_frontend\]

</td><td>

API Component\[cmdb\_ci\_api\_component\]

</td><td>

The part of an API from which a client or user interacts or makes requests. Example: GET https://\[apiID\].execute-api.us-east-2.amazonaws.com/\{proxy+\}.

</td></tr><tr><td>

API Backend\[cmdb\_ci\_api\_backend\]

</td><td>

API Component\[cmdb\_ci\_api\_component\]

</td><td>

The part of an API that fulfills requests by interacting with backend services, such as servers. Example: Lambda:Chat-API-Proxy.

</td></tr><tr><td>

API Gateway\[cmdb\_ci\_api\_gateway\]

</td><td>

Application\[cmdb\_ci\_appl\]

</td><td>

API infrastructure that centralizes client API requests and manages backend processes and services. Example: Kong Gateway.

</td></tr><tr><td>

Managed API\[cmdb\_ci\_managed\_api\]

</td><td>

Configuration Item\[cmdb\_ci\_api\]

</td><td>

API discovered from a gateway or management service. You can enforce a dependency on a gateway for APIs in this class.

</td></tr></tbody>
</table>## Class attributes

CMDB CI Class Models: Release 1.49.0 adds the following attributes to the respective classes.

<table id="table_ch3_b1l_tlb"><thead><tr><th>

Attribute

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base URL

</td><td>

String \(1024\)

</td><td>

Base address from which all API components extend.

</td></tr><tr><td>

ID

</td><td>

String \(1024\)

</td><td>

Unique identifier from the source system.

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

Version

</td><td>

Numeric

</td><td>

Version of the API.

</td></tr><tr><td>

Spec Location

</td><td>

URL

</td><td>

URL to the location of the API specification. Example: OpenAPI spec definition.

</td></tr></tbody>
</table><table id="table_jlv_fmg_syb"><thead><tr><th>

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

REST API methods. Examples:-   GET
-   POST
-   DELETE

</td></tr><tr><td>

Protocol

</td><td>

String

</td><td>

Communication protocol. Example: HTTP, HTTPS.

</td></tr><tr><td>

Host

</td><td>

String \(100\)

</td><td>

System that hosts the API.

</td></tr><tr><td>

Path

</td><td>

String \(1024\)

</td><td>

Specific route the API follows.

</td></tr><tr><td>

Port

</td><td>

String

</td><td>

Communication port. Example: 80, 443, and so on.

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
-   OAuth
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
</table>|Attribute|Data type|Description|
|---------|---------|-----------|
|Parent ID|Reference to \[cmdb\_ci\_api\_frontend\]|Reference to a parent API component.|

<table id="table_tqx_q3g_syb"><thead><tr><th>

Attribute

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

String

</td><td>

Backend protocol types of the API. Examples:-   Lambda
-   HTTP
-   Logic App

</td></tr></tbody>
</table>|Attribute|Data type|Description|
|---------|---------|-----------|
|ID|String \(255\)|Unique identifier from the source system.|

**Note:** Managed API \[cmdb\_ci\_managed\_api\] is specific to APIs discovered from gateways and other managed services, and does not introduce new attributes at this time.

## Key Relationship Structures

There are a number of key relationships that must be defined for API and Kong classes.

<table id="table_b1s_t32_5yb"><thead><tr><th>

Parent class

</th><th>

Relationship

</th><th>

Child class

</th><th>

Relationship type

</th></tr></thead><tbody><tr><td>

API \[cmdb\_ci\_api\]

</td><td>

Uses::Used by

</td><td>

API Component\[cmdb\_ci\_api\_component\]

</td><td>

Suggested

</td></tr><tr><td>

API Gateway \[cmdb\_ci\_api\_gateway\]

</td><td>

Provides::Provided By

</td><td>

Managed API\[cmdb\_ci\_managed\_api\]

</td><td>

Dependent

</td></tr><tr><td>

API Frontend \[cmdb\_ci\_api\_frontend\]

</td><td>

Use End Point To::Use End Point From

</td><td>

API Backend\[cmdb\_ci\_api\_backend\]

</td><td>

Suggested

</td></tr><tr><td>

API Backend\[cmdb\_ci\_api\_backend\]

</td><td>

Uses::Used By

</td><td>

Kong Load Balancer\[cmdb\_ci\_kong\_lb\]

</td><td>

Suggested

</td></tr></tbody>
</table>## Related non-CMDB tables

CMDB CI Class Models v 1.49.0 introduces these non-CMDB tables as related lists for the following API extension classes:

-   **API related list**

    |Attribute|Data type|Description|
    |---------|---------|-----------|
    |Name|String \(100\)|Name of the API deployment.|
    |API|Reference|Reference to the deployed API \(cmdb\_ci\_api\).|
    |Unmatched API Endpoint|Reference|Reference to the unmatched API endpoint, if the API doesn't match an existing API \(cmdb\_ci\_unmatched\_api\_endpoint\).|
    |Configuration Item|Reference|Reference to the Configuration Item. This is typically manually specified as a reference, if you know what CI the API is deployed to.|

    **Note:** The API Deployment non-CMDB table relates to both the API \[cmdb\_ci\_api\] and Unmatched API Endpoint \[cmdb\_ci\_unmatched\_api\_endpoint\] classes.

-   **API Component related list**

    |Attribute|Data type|Description|
    |---------|---------|-----------|
    |Name|String \(100\)|Name of the API header.|
    |API Component|Reference|Reference to the component where the API header is defined \(cmdb\_ci\_api\_component\).|
    |Unmatched API Endpoint|Reference|Reference to the unmatched API when the endpoint can't be matched to an existing API or component \(cmdb\_ci\_unmatched\_endpoint\).|

-   **API Gateway related lists**

<table id="table_swj_lch_syb"><thead><tr><th>

Attribute

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Username

</td><td>

String \(100\)

</td><td>

Name of the API consumer.

 **Note:** The **Consumer** field in the api\_policy table is a reference field. To display the username in the **Username** field on the API Policies list, you must set the **display** attribute of **Username** to `true`. If the attribute is not set to `true`, then the list displays the Sys ID instead.

</td></tr><tr><td>

ID

</td><td>

String \(255\)

</td><td>

Unique identifier from the source system.

</td></tr><tr><td>

Custom ID

</td><td>

String \(100\)

</td><td>

Alternate display name of the user.

</td></tr><tr><td>

API Gateway

</td><td>

Reference

</td><td>

Reference to the gateway where the consumer is defined \(cmdb\_ci\_api\_gateway\).

</td></tr></tbody>
</table><table id="table_l41_wch_syb"><thead><tr><th>

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

Name of the API policy.

</td></tr><tr><td>

ID

</td><td>

String \(255\)

</td><td>

Unique identifier from the source system.

</td></tr><tr><td>

Frontend

</td><td>

Reference

</td><td>

Reference to the API Frontend \(cmdb\_ci\_api\_frontend\).

</td></tr><tr><td>

Managed API

</td><td>

Reference

</td><td>

Reference to the Managed API \(cmdb\_ci\_managed\_api\).

</td></tr><tr><td>

Consumer

</td><td>

Reference

</td><td>

Reference to the API Consumer \(api\_consumer\) non-CMDB table. **Note:** **Consumer** is a reference field. To display the Username in the API Policies list, you must set the **display** attribute to `true` for **Username** field in the api\_consumer table. If the attribute is not set to `true`, then the list displays the Sys ID instead.

</td></tr><tr><td>

Protocols

</td><td>

String

</td><td>

Array of protocols that this API policy can apply to.

</td></tr><tr><td>

Active

</td><td>

Boolean

</td><td>

Determines if this non-CMDB table is considered active or inactive.

</td></tr><tr><td>

API Gateway

</td><td>

Reference

</td><td>

Reference to the gateway where the consumer is defined \(cmdb\_ci\_api\_gateway\).

</td></tr></tbody>
</table>
