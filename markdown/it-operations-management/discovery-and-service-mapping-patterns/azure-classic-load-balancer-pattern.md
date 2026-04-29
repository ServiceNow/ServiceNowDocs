---
title: Azure Classic Load Balancer pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Classic Load Balancers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Azure - Classic LB \(LP\), Azure LoadBalancer TD, Azure Load Balancer, Azure Classic Load Balancer, Azure discovery, Azure patterns]
breadcrumb: [Microsoft Azure discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Classic Load Balancer pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Classic Load Balancers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Classic LB \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Name \[name\]|The name of the load balancer.|
|State \[state\]|The current state of the load balancer.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Name \[name\]|IP address of the load balancer.|
|IP Address \[ip\_address\]|IP address of the load balancer.|
|IPAddress Type \[ipaddress\_type\]|The type of the IP address, which can be private or public.|
|Fully qualified domain name \[fqdn\]|The fully qualified domain name \(FQDN\) of the load balancer.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Name \[name\]|The name of the load balancing rule or inbound NAT rule.|
|Port \[port\]|The TCP port that the load balancer service listens to.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Name \[name\]|The name of the backend address pool.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - Classic LB \(LP\) pattern creates these relationships to support Azure Classic Load Balancer discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Owns::Owned by|Cloud LB IP Address \[cmdb\_ci\_cloud\_lb\_ipaddress\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|Load Balancer Service \[cmdb\_ci\_lb\_service\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

## Connections discovered by Service Mapping during top-down discovery

The Azure LoadBalancer TD pattern performs top-down discovery of Azure Classic Load Balancers. Service Mapping discovers cluster connections from the load balancer service to backend pool member IP addresses using either load balancing rules or inbound NAT rules.

**Parent Topic:**[Microsoft Azure Cloud discovery using patterns](azure-cloud-discovery-patterns.md)

