---
title: CMDB classes targeted in Service Graph Connector for BlueCat
description: When you complete setting up the connection, you can configure the integration to periodically pull data from BlueCat. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-bluecat-classes.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [BlueCat, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for BlueCat

When you complete setting up the connection, you can configure the integration to periodically pull data from BlueCat. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]

The following attributes in the Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Ip Version|ip\_version|
|Cidr|cidr|
|Managed Network|managed\_network|
|Name|name|
|Parent Pool|parent\_pool|
|Operational Status|operational\_status|

## Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]

The following attributes in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Ip Version|ip\_version|
|Managed Network|managed\_network|
|Is Dhcp|is\_dhcp|
|Ip Address|ip\_address|
|Is Dns|is\_dns|
|Subnet|subnet|
|Name|name|
|Is Reserved|is\_reserved|
|Operational Status|operational\_status|
|Is Broadcast|is\_broadcast|

## Managed Network \[cmdb\_ci\_managed\_network\]

The following attributes in the Managed Network \[cmdb\_ci\_managed\_network\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Correlation Id|correlation\_id|
|Name|name|
|Operational Status|operational\_status|
|Short Description|short\_description|

