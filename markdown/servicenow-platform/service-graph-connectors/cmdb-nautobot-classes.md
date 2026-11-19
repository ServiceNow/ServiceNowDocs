---
title: CMDB classes targeted in Service Graph Connector for Nautobot
description: When you complete setting up the connection, you can configure the integration to periodically pull data from Nautobot. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/cmdb-nautobot-classes.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-04-07"
reading_time_minutes: 1
breadcrumb: [Nautobot, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Nautobot

When you complete setting up the connection, you can configure the integration to periodically pull data from Nautobot. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Server \[cmdb\_ci\_server\]

The following attributes in the Server \[cmdb\_ci\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Os|os|
|Cpu Count|cpu\_count|
|Install Status|install\_status|
|Name|name|
|Virtual|virtual|

## Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]

The following attributes in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Managed Network|managed\_network|
|Name|name|
|Is Dns|is\_dns|
|Subnet|subnet|
|Ip Address|ip\_address|
|Operational Status|operational\_status|
|Is Dhcp|is\_dhcp|
|Ip Version|ip\_version|
|Is Reserved|is\_reserved|

## Linux Server \[cmdb\_ci\_linux\_server\]

The following attributes in the Linux Server \[cmdb\_ci\_linux\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Cpu Count|cpu\_count|
|Virtual|virtual|
|Name|name|
|Install Status|install\_status|
|Os|os|

## Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]

The following attributes in the Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Ip Version|ip\_version|
|Managed Network|managed\_network|
|Parent Pool|parent\_pool|
|Operational Status|operational\_status|
|Short Description|short\_description|
|Cidr|cidr|

## Managed Network \[cmdb\_ci\_managed\_network\]

The following attributes in the Managed Network \[cmdb\_ci\_managed\_network\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Short Description|short\_description|
|Name|name|
|Correlation Id|correlation\_id|

## Windows Server \[cmdb\_ci\_win\_server\]

The following attributes in the Windows Server \[cmdb\_ci\_win\_server\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Install Status|install\_status|
|Cpu Count|cpu\_count|
|Virtual|virtual|
|Os|os|
|Name|name|

