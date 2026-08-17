---
title: Azure Application LB pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure application load balancers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery-and-service-mapping-patterns/azure-application-lb-pattern.html
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-17"
reading_time_minutes: 3
keywords: [Azure Application LB, Azure Application Gateway, Azure discovery, Azure patterns, Application LB pattern]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Application LB pattern-based discovery

Discovery and Service Mapping Patterns finds Azure application load balancers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the Microsoft Azure discovery prerequisites**

    For more information, see the prerequisites section in [Microsoft Azure Cloud components discovery using patterns]().

-   **Configure the Discovery schedule to support GovCloud**

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/setup-azure-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure - Application LB \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the load balancer.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Location \[location\]|The path of the load balancer.|
|State \[state\]|The current state of the load balancer.|
|IP Address \[ip\_address\]|IP address of the load balancer.|
|Fully qualified domain name \[fqdn\]|The fully qualified domain name of the load balancer.|
|DNS Name \[dns\_name\]|The DNS name of the load balancer.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|IP Address \[ip\_address\]|IP address of the load balancer.|
|IPAddress Type \[ipaddress\_type\]|The type of the IP address. Possible values are private or public.|
|Fully qualified domain name \[fqdn\]|The fully qualified domain name of the load balancer.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the load balancer pool.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Location \[location\]|Path of the load balancer pool.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The Name or ID if no Name is specified for the load balancer service.|
|Object ID \[object\_id\]|A unique identifier, allocated by Azure for this resource.|
|Location \[location\]|Path of the load balancer service.|
|Port \[port\]|The TCP port that the load balancer service listens to.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|

## CI relationships

The Azure - Application LB \(LP\) pattern creates the following relationships and references to support Azure Application LB discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Owns::Owned by|Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

## Azure Tag discovery

The Azure - Application LB \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\] table.|

**Parent Topic:**[Available discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

