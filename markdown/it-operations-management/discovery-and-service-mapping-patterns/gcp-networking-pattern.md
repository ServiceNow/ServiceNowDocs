---
title: GCP Networking pattern-based discovery
description: Discovery and Service Mapping Patterns finds GCP networking resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-18"
reading_time_minutes: 4
keywords: [GCP networking pattern, GCP discovery, GCP patterns, GCP VPC discovery, GCP subnet discovery, GCP network ACL, GCP firewall rules, Google Cloud networking]
breadcrumb: [GCP discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP Networking pattern-based discovery

Discovery and Service Mapping Patterns finds GCP networking resources on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Networking pattern.

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
|Name \[name\]|Name of the Google Cloud Virtual Private Cloud \(VPC\) network.|
|Object ID \[object\_id\]|Unique identifier for the VPC network resource in Google Cloud.|
|Description \[short\_description\]|Description of the VPC network.|
|Default Gateway \[default\_gateway\]|Default gateway IPv4 address for the network.|
|State \[state\]|Current state of the VPC network. Default value is Available.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Google Cloud subnetwork. If the network has auto-creation enabled, the Classless Inter-Domain Routing \(CIDR\) notation is used as the name.|
|Object ID \[object\_id\]|Unique identifier for the subnetwork resource in GCP.|
|CIDR \[cidr\]|IP address range of the subnetwork in CIDR notation. May include primary IPv4, secondary IPv4, and IPv6 ranges as a comma-separated list.|
|Subnet Mask \[subnet\_mask\]|Dotted representation of the subnet mask. For example: 255.255.240.0.|
|Gateway \[gateway\]|Gateway address for default routing out of the network.|
|Broadcast Address \[broadcast\_address\]|Broadcast address of the subnet.|
|Available IP Count \[available\_ip\_count\]|Number of IPs that are available in the subnet. This amount does not include network and broadcast addresses.|
|State \[state\]|Current state of the subnetwork. Default value is Available.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Google Cloud firewall rule.|
|Object ID \[object\_id\]|Unique identifier for the firewall rule in Google Cloud.|
|Description \[short\_description\]|Description of the firewall rule.|
|Install Status \[install\_status\]|Install status of the firewall rule. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

<table id="table_acl_rule_dgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the firewall rule.

</td></tr><tr><td>

Allow Deny \[allow\_deny\]

</td><td>

Indicates whether traffic is allowed or denied.

</td></tr><tr><td>

Outbound \[is\_outbound\]

</td><td>

Traffic direction for the firewall rule.-   true: EGRESS
-   false: INGRESS

</td></tr><tr><td>

Source Ranges \[source\_ranges\]

</td><td>

Source IP address ranges in CIDR notation for the firewall rule.

</td></tr><tr><td>

Destination Ranges \[destination\_ranges\]

</td><td>

Destination IP address ranges in CIDR notation for the firewall rule.

</td></tr><tr><td>

Target Tags \[target\_tags\]

</td><td>

Network tags that identify which instances the firewall rule affects.

</td></tr><tr><td>

Allowed\\Denied Traffic \[allowed\_denied\_traffic\]

</td><td>

Protocols and ports that are allowed or denied by this rule.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table>## CI relationships

The Google Cloud Platform \(GCP\) - Networking pattern creates these relationships to support GCP networking discovery.

|CI|Relationship|CI|
|---|------------|---|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Cloud Network \[cmdb\_ci\_network\]|Contains::Contained by|Network ACL \[cmdb\_ci\_network\_acl\]|
|Network ACL \[cmdb\_ci\_network\_acl\]|Contains::Contained by|Network ACL Rule \[cmdb\_ci\_network\_acl\_rule\]|

**Parent Topic:**[Google Cloud Platform \(GCP\) Cloud discovery using Patterns](gcp-cloud-discovery-patterns.md)

