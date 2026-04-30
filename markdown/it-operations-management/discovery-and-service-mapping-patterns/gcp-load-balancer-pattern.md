---
title: GCP Load Balancer pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP Load Balancers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-01-12"
reading_time_minutes: 4
keywords: [GCP Load Balancer, Google Cloud Platform Load Balancer, GCP discovery, GCP patterns, HTTP load balancer, HTTPS load balancer, TCP load balancer, UDP load balancer]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP Load Balancer pattern-based discovery

Discovery and Service Mapping Patterns finds GCP Load Balancers on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The Discovery patterns discover GCP Load Balancing infrastructure:

-   Google Cloud Platform \(GCP\) - Load Balancer - HTTP pattern: Discovers Layer 7 \(application layer\) load balancers that use HTTP and HTTPS protocols
-   Google Cloud Platform \(GCP\) - Load Balancer - TCP - UDP pattern: Discovers Layer 4 \(transport layer\) load balancers that use TCP and UDP protocols

Both patterns populate the same CMDB tables.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Load Balancer patterns.

|Field|Description|
|-----|-----------|
|Account Id \[account\_id\]|Name of the project used for the discovery.|
|Object ID \[object\_id\]|Name of the project used for the discovery.|
|Datacenter Type \[datacenter\_type\]|Datacenter type: Google Datacenter \[cmdb\_ci\_google\_datacenter\].|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the availability zone.|
|Description \[short\_description\]|Description of the availability zone.|
|State \[state\]|State of the Availability Zone. Possible values are Available or Terminated.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Datacenter or region name.|
|Region \[region\]|Datacenter or region name.|
|Object ID \[object\_id\]|Unique identifier allocated by GCP for this resource.|
|Description \[short\_description\]|Datacenter or region description.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Unique identifier for the load balancer.|
|Name \[name\]|Name of the load balancer.|
|State \[state\]|State of the load balancer. Default value is Available.|

<table id="table_lb_service"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the load balancer service.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the load balancer service.

</td></tr><tr><td>

Service Type \[service\_type\]

</td><td>

Type of service. Possible values are Frontend or Backend.

</td></tr><tr><td>

Listener Protocol \[listener\_protocol\]

</td><td>

Protocol used by the service listener.

</td></tr><tr><td>

Port \[port\]

</td><td>

Port number used by the service.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address of the frontend service.

</td></tr><tr><td>

Pool \[pool\]

</td><td>

References the Load Balancer Pool \[cmdb\_ci\_lb\_pool\] table.This field is populated only by the Google Cloud Platform \(GCP\) - Load Balancer - HTTP pattern.

</td></tr></tbody>
</table><table id="table_lb_pool"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the load balancer pool.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the load balancer pool.

</td></tr><tr><td>

Load balancing method \[load\_balancing\_method\]

</td><td>

Load balancing method used by the pool.This field is populated only by the Google Cloud Platform \(GCP\) - Load Balancer - TCP - UDP pattern.

</td></tr></tbody>
</table><table id="table_lb_pool_member"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the pool member, known as a VM instance ID in GCP.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the pool member, known as a VM instance name in GCP.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the pool member.-   Operational: Instance status is running
-   Non-Operational: Other instance states

</td></tr></tbody>
</table><table id="table_lb_health"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the health check service.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the health check service.

</td></tr><tr><td>

Monitor type protocol \[monitor\_type\]

</td><td>

Type of health check monitor For example: HTTP or TCP.

</td></tr><tr><td>

Port \[port\]

</td><td>

Port number used for health checks.

</td></tr><tr><td>

Timeout in seconds \[timeout\_sec\]

</td><td>

Timeout in seconds for health check requests.

</td></tr><tr><td>

Unhealthy threshold \[unhealthy\_threshold\]

</td><td>

Number of consecutive failures before marking as unhealthy.

</td></tr><tr><td>

Healthy threshold \[healthy\_threshold\]

</td><td>

Number of consecutive successes before marking as healthy.

</td></tr><tr><td>

Interval in seconds \[check\_interval\_sec\]

</td><td>

Interval in seconds between health checks.

</td></tr><tr><td>

Request path \[request\_path\]

</td><td>

Request path for HTTP and HTTPS health checks.This field is populated only by the Google Cloud Platform \(GCP\) - Load Balancer - HTTP pattern.

</td></tr></tbody>
</table>## CI relationships

Both Load Balancer patterns create these relationships to support GCP Load Balancer discovery.

|CI|Relationship|CI|
|---|------------|---|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Owns::Owned by|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

The Google Cloud Platform \(GCP\) - Load Balancer - HTTP pattern creates relationships to support GCP Load Balancer discovery.

|CI|Relationship|CI|
|---|------------|---|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Uses::Used by|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|References|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|Used by::Uses|Load Balancer Service \[cmdb\_ci\_lb\_service\]|

The Google Cloud Platform \(GCP\) - Load Balancer - TCP - UDP pattern creates relationships to support GCP Load Balancer discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Uses::Used by|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|Used by::Uses|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

