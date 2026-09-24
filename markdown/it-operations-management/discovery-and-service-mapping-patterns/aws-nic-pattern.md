---
title: AWS NIC pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS network interfaces \(NICs\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-nic-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 3
keywords: [Amazon AWS NIC, AWS network interface, AWS discovery, AWS patterns, NIC pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS NIC pattern-based discovery

Discovery and Service Mapping Patterns finds AWS network interfaces \(NICs\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - NIC \(LP\) pattern.

<table id="table_cmdb_ci_nic"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The Name or ID if no Name is specified for the network interface.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The ID of the network interface.

</td></tr><tr><td>

State \[state\]

</td><td>

The status of the network interface. Possible valid values: available, associated, attaching, in-use, or detaching.

</td></tr><tr><td>

Private IP \[private\_ip\]

</td><td>

The IPv4 address of the network interface within the subnet.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

If available, the address of the Elastic IP address bound to the network interface. If not available, the Private IP.

</td></tr><tr><td>

Public IP \[public\_ip\]

</td><td>

The address of the Elastic IP address bound to the network interface.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|IP address of the load balancer.|
|Object ID \[object\_id\]|If available, the address of the Elastic IP address bound to the network. If not available, the Private IP.|
|IP Address \[ip\_address\]|If available, the address of the Elastic IP address bound to the network interface. If not available, the Private IP.|
|Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the virtual network machine interface \(VNIC\) endpoint.|
|Object ID \[object\_id\]|Unique identifier, allocated by Amazon for this resource.|
|IP Address \[ip\_address\]|If available, the address of the Elastic IP address bound to the network interface. If not available, the Private IP.|
|Host \[host\]|The ID of the instance.|

## CI relationships and references

The Amazon AWS - NIC \(LP\) pattern creates the following relationships and references to support Amazon AWS NIC discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Owns::Owned by|Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|
|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Implement End Point To::Implement End Point From|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|
|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]|

## AWS Tag discovery

The Amazon AWS - NIC \(LP\) pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Mgmt Network Interface \[cmdb\_ci\_nic\] table.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

