---
title: Kong extension classes
description: The CMDB CI Class Models store app adds or updates classes for Kong gateways.
locale: en-US
release: yokohama
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Kong extension classes

The CMDB CI Class Models store app adds or updates classes for Kong gateways.

The CMDB CI Class Models app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Kong

Kong is an API management platform that enables enterprise companies to better manage client and host traffic.

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

CMDB CI Class Models: Release 1.49.0 adds the following classes for Kong.

<table id="table_h2r_d5z_ryb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Kong Gateway\[cmdb\_ci\_kong\_gateway\]

</td><td>

API Gateway\[cmdb\_ci\_api\_gateway\]

</td><td>

The Kong gateway application that hosts and manages individual APIs. Example: Kong Gateway instanceName.

</td></tr><tr><td>

Kong Load Balancer\[cmdb\_ci\_kong\_lb\]

</td><td>

Load Balancer Application\[cmdb\_ci\_lb\_appl\]

</td><td>

The default load balancer on the Kong gateway application that points to backend service instances when fulfilling API requests. Example: httpbin-upstream.

</td></tr><tr><td>

Kong Target\[cmdb\_ci\_kong\_target\]

</td><td>

API Component\[cmdb\_ci\_api\_component\]

</td><td>

The load-balanced backend of the gateway that fulfills API requests. Example: httpbin-target1.

</td></tr></tbody>
</table>## Class attributes

CMDB CI Class Models: Release 1.49.0 adds the following attributes to the respective classes.

|Attribute|Data type|Description|
|---------|---------|-----------|
|Admin URL|String \(255\)|URL for making admin API requests.|
|Database|String|Type of database used by the Kong gateway. Example: Postgres or Cassandra.|

|Attribute|Data type|Description|
|---------|---------|-----------|
|Algorithm|String|Type of algorithm used for load balancing. Example: round robin.|
|ID|String \(255\)|Unique identifier from the source system.|

|Attribute|Data type|Description|
|---------|---------|-----------|
|Target|String \(255\)|URL of target integration.|

## Key Relationship Structures

There are a number of key relationships that must be defined for API and Kong classes.

|Parent class|Relationship|Child class|Relationship type|
|------------|------------|-----------|-----------------|
|API Backend \[cmdb\_ci\_api\_backend\]|Uses::Used By|Kong Load Balancer|Suggested|
|Kong Load Balancer \[cmdb\_ci\_lb\_appl\]|Contains::Contained By|Kong Target|Dependent|
|Kong Gateway \[cmdb\_ci\_kong\_gateway\]|Provides::Provided By|Kong Load Balancer|Dependent|

## Related non-CMDB tables

The Kong Gateway class uses the Kong Workspace non-CMDB table as a related list:

|Attribute|Data type|Description|
|---------|---------|-----------|
|Name|String \(100\)|Name of the Kong workspace.|
|ID|String \(255\)|Unique identifier from the source system.|
|API Gateway|Reference|Reference to the Kong API gateway.|

## Kong gateway example

Here is an example of a dependency view for the Kong gateway class that shows how a gateway would populate the dependent managed API-dependent class with related APIs and components. The Managed API class is considered a first-level relationship with respect to the gateway, while the frontend and backend components are considered second-level relationships. From here, you can then bind alerts to these CIs, configure dynamic CIs for service views and incidents, or establish any additional workflows that use CIs.

![Dependency View of the Kong data model populated from a gateway.](../image/cmdb-ci-class-models-kong.png)

