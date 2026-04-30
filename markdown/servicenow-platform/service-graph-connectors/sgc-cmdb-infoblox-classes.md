---
title: CMDB classes targeted in Service Graph Connector for Infoblox
description: When you complete setting up the connection, you can configure the integration to pull data periodically from Infoblox. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 2
breadcrumb: [Infoblox, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classes targeted in Service Graph Connector for Infoblox

When you complete setting up the connection, you can configure the integration to pull data periodically from Infoblox. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.

## Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]

The following attributes in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Managed Network|managed\_network|
|IP Version|ip\_version|
|Is Broadcast|is\_broadcast|
|Is Conflict|is\_conflict|
|Is DHCP|is\_dhcp|
|Is DNS|is\_dns|
|Is Reserved|is\_reserved|
|Name|name|
|Operational status|operational\_status|
|Subnet|subnet|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]|Reference|Key Value \[cmdb\_key\_value\]|

## DNS Alias \[cmdb\_ci\_dns\_alias\]

The following attribute in the DNS Alias \[cmdb\_ci\_dns\_alias\] table is populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|

## Key Value \[cmdb\_key\_value\]

The following attributes in the Key Value \[cmdb\_key\_value\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Key|key|
|Value|value|

The Key Value table is populated with Infoblox extensible attributes for all IPAM tables.

## Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]

The following attributes in the Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Managed Network|managed\_network|
|Name|name|
|Parent Pool|parent\_pool|
|CIDR|cidr|
|Correlation ID|correlation\_id|
|IP Version|ip\_version|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]|Reference|SG-Infoblox Detailed Subnetwork \[sn\_infoblox\_integ\_sg\_infoblox\_detailed\_subnetwork\]|
|Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]|Reference|Key Value \[cmdb\_key\_value\]|

**Note:** The IP Network Subnet table is renamed as Managed IP Network Subnet in Service Graph Connector for Infoblox version 1.5.0. The table is renamed to differentiate managed entities from discovered entities \(network subnets\).

## Managed IP Pool \[cmdb\_ci\_ip\_pool\]

The following attributes in the Managed IP Pool \[cmdb\_ci\_ip\_pool\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Managed Network|managed\_network|
|Name|name|
|Parent Pool|parent\_pool|
|CIDR|cidr|
|Correlation ID|correlation\_id|
|IP Version|ip\_version|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Managed IP Pool \[cmdb\_ci\_ip\_pool\]|Reference|Key Value \[cmdb\_key\_value\]|

**Note:** The IP Pool table is renamed as Managed IP Pool in Service Graph Connector for Infoblox version 1.5.0. The table is renamed to differentiate managed entities from discovered entities \(IP pools\).

## Managed Network \[cmdb\_ci\_managed\_network\]

The following attributes in the Managed Network \[cmdb\_ci\_managed\_network\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Correlation ID|correlation\_id|
|Name|name|
|Operational status|operational\_status|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|Managed Network \[cmdb\_ci\_managed\_network\]|Reference|Key Value \[cmdb\_key\_value\]|

**Note:** In Service Graph Connector for Infoblox version 1.5.0 and later, the Managed Network \[cmdb\_ci\_managed\_network\] table imports Infoblox Network View data.

## SG-Infoblox Detailed Subnetwork \[sn\_infoblox\_integ\_sg\_infoblox\_detailed\_subnetwork\]

The following attributes in the SG-Infoblox Detailed Subnetwork \[sn\_infoblox\_integ\_sg\_infoblox\_detailed\_subnetwork\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Network|network|
|Get Ip Address|list\_ip\_address|
|Network Type|network\_type|
|Network View|network\_view|
|Operational status|operational\_status|
|Connection ID|connection\_id|

