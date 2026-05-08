---
title: OpenStack resource discovery
description: The ServiceNow Discovery application uses OpenStack resource discovery patterns to find OpenStack resources through REST API calls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OpenStack resource discovery

The ServiceNow Discovery application uses OpenStack resource discovery patterns to find OpenStack resources through REST API calls. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses OpenStack resource discovery patterns to run horizontal discovery.

Starting with the Discovery and Service Mapping Patterns August 2024 store release, OpenStack resource discovery patterns support both private and public cloud discovery.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **OpenStack requirements**
    -   In the OpenStack Identity service catalog, find the access URL that is used as the OpenStack identity service endpoint. For example: https://&lt;openstack dns&gt;:&lt;port&gt;.
    -   Configure an OpenStack user with permissions to generate a project scope token. Setting Domain ID, User Name, Project Name, and Password values is required for generating a token.
-   **MID Server requirements**

    Deploy and connect a dedicated MID Server for cloud discovery.

    The dedicated MID Server must have access to OpenStack and an open port for each OpenStack service to be discovered.

-   **Credentials**

    On the ServiceNow AI Platform, create OpenStack credentials for the ServiceNow cloud service account. Enter the Domain ID, User Name, Project Name, and Password values you've configured in OpenStack requirements. For more information, see Create and test your credentials.

-   **Service account**

    On the ServiceNow AI Platform, configure a ServiceNow cloud service account using the created OpenStack credentials and the OpenStack datacenter details. In the **Account Id** field, provide the Project ID of the OpenStack Project to be discovered.

-   **Create a discovery schedule**

    For more information, see [Create an OpenStack Discovery schedule in Discovery Admin Workspace](../../discovery/task/create-openstack-schedule-DAW.md).

-   **Create an automatic discovery schedule for OpenStack service accounts—for private cloud only**

    Create an automatic serverless discovery schedule for OpenStack service accounts using the OpenStack - Discover Service Accounts pattern. For more information, see the [Auto Cloud discovery schedule for Open stack \[KB1638685\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1638685) article in the Now Support Knowledge Base.

-   **\(Optional\) Populate Service Account and Logical Datacenter fields in cloud CIs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating Service Account and Logical Datacenter fields directly in cloud CIs. For more information, see [Improved query performance with direct field population in CI tables](../concept/query-service-account-ldc-fields.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the OpenStack resource discovery patterns.

<table id="table_bph_wsf_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Server UUID.

</td></tr><tr><td>

Name \[name\]

</td><td>

Server name.

</td></tr><tr><td>

Status \[status\]

</td><td>

Server status.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

\(Optional\) Server description.

</td></tr><tr><td>

CPUs \[cpus\]

</td><td>

Number of virtual CPUs \(vCPUs\) from the Flavor that the VM instance is provisioned with.

</td></tr><tr><td>

Disks \[disks\]

</td><td>

Number of all managed volumes by Cinder that are returned from the VM instance.

</td></tr><tr><td>

Disks size \(GB\) \[disk\_size\]

</td><td>

Total amount of all managed volumes by Cinder that are used by the VM instance measured in gigabytes \(GB\).

</td></tr><tr><td>

Memory \(MB\) \[memory\]

</td><td>

The **ram** value from the Flavor that the VM instance is provisioned with, measured in megabytes \(MB\).

</td></tr><tr><td>

Network adapters \[nics\]

</td><td>

Number of unique interfaces configured in the VM instance.

</td></tr><tr><td>

State \[state\]

</td><td>

Mapped status value returned for the VM instance. The OpenStack Server statuses and their related ServiceNow **State** values are:

-   ACTIVE: on
-   RESCUED: on
-   PAUSED: paused
-   SUSPENDED: off
-   STOPPED: off
-   SOFT\_DELETED: terminated
-   HARD\_DELETED: terminated
-   RESIZED: off
-   ERROR: error
-   INITIALIZED: starting

For any **status** value not listed, the default value is off.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Keypair UUID.|
|Name \[name\]|Keypair name that is used to reference it.|
|Finger print \[finger\_print\]|Keypair fingerprint.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Load balancer ID.|
|Name \[name\]|Human-readable resource name.|
|Description \[short\_description\]|\(Optional\) Human-readable resource description.|
|Install Status \[install\_status\]|Resource provisioning status.|
|Operational Status \[operational\_status\]|Resource operational status.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Listener ID.|
|Name \[name\]|Human-readable name of the resource.|
|Install Status \[install\_status\]|Provisioning status of the resource.|
|Listener Protocol \[listener\_protocol\]|Protocol for the resource. One of HTTP, HTTPS, TCP, TERMINATED\_HTTPS, or UDP.|
|Listener Port \[listener\_port\]|Protocol port number for the resource.|
|Operational status \[operational\_status\]|Resource operational status.|
|Description \[short\_description\]|\(Optional\) Human-readable resource description.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Pool ID.|
|Name \[name\]|Human-readable resource name.|
|Install Status \[install\_status\]|Resource provisioning status.|
|Operational Status \[operational\_status\]|Resource operational status.|
|Description \[short\_description\]|\(Optional\) Human-readable resource description.|
|Load Balancing Method \[load\_balancing\_method\]|Load balancing algorithm for the pool. One of these values: LEAST\_CONNECTIONS, ROUND\_ROBIN, SOURCE\_IP, or SOURCE\_IP\_PORT.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Pool member ID.|
|Name \[name\]|Human-readable resource name.|
|Install Status \[install\_status\]|Resource provisioning status.|
|IP address \[ip\_address\]|Back-end member server IP address.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Volume UUID.|
|Name \[name\]|Volume name.|
|Status \[status\]|Volume status.|
|Description \[short\_description\]|\(Optional\) Human-readable description.|
|Storage type \[storage\_type\]|Associated volume type.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Volume UUID.|
|Name \[name\]|Volume name.|
|Status \[status\]|Volume status.|
|Description \[short\_description\]|\(Optional\) Human-readable description.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|User-defined image UUID.|
|Name \[name\]|Image name. The value can be null \(the JSON Null data type\).|
|Status \[status\]|Image status.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Network ID.|
|Name \[name\]|Human-readable network name.|
|Operational Status \[operational\_status\]|Network status. Possible values: ACTIVE, DOWN, BUILD, or ERROR.|
|Description \[short\_description\]|\(Optional\) Human-readable description.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Subnet ID.|
|Name \[name\]|Human-readable resource name.|
|DHCP enabled \[is\_dhcp\_enabled\]|Whether DHCP is enabled or disabled for the subnet.|
|Description \[short\_description\]|\(Optional\) Human-readable description.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Security group ID.|
|Name \[name\]|Human-readable resource name.|
|Description \[short\_description\]|\(Optional\) Human-readable description.|

<table id="table_rrs_xsf_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

This field has the same value as the object\_id field.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Security group rule ID.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

\(Optional\) Human-readable description.

</td></tr><tr><td>

Ethertype \[ethertype\]

</td><td>

Ethertype. Must be IPv4 or IPv6. Addresses represented in CIDR must match the ingress or egress rules.

</td></tr><tr><td>

Port range max \[port\_range\_max\]

</td><td>

The last port of the range to which the rule applies. This value is the maximum port number in the range that is matched by the security group rule. -   If the protocol is TCP, UDP, DCCP, SCTP or UDP-Lite, this value must be greater than or equal to the port\_range\_min attribute value.
-   If the protocol is ICMP, this value must be an ICMP code.

</td></tr><tr><td>

Port range min \[port\_range\_min\]

</td><td>

The first port of the range to which the rule applies. This value is the minimum port number in the range that is matched by the security group rule.-   If the protocol is TCP, UDP, DCCP, SCTP or UDP-Lite, this value must be less than or equal to the port\_range\_max attribute value.
-   If the protocol is ICMP, this value must be an ICMP type.

</td></tr></tbody>
</table><table id="table_i5t_xsf_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Domain ID.

</td></tr><tr><td>

Name \[name\]

</td><td>

Domain name.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

\(Optional\) Human-readable description.

</td></tr><tr><td>

Enabled \[enabled\]

</td><td>

Defines whether the domain is enabled or disabled.-   True - The domain is enabled.
-   False - The domain is disabled.

</td></tr></tbody>
</table><table id="table_nv5_xsf_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Service ID.

</td></tr><tr><td>

Name \[name\]

</td><td>

Service name.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

\(Optional\) Human-readable description.

</td></tr><tr><td>

Type \[type\]

</td><td>

Service type. Describes the API implemented by the service. Possible values: Compute, ec2, identity, image, network, or volume.

</td></tr><tr><td>

Catalog enabled \[enabled\]

</td><td>

Defines whether the service and its endpoints appear in the service catalog.-   True - The service and its endpoints appear in the service catalog.
-   False - The service and its endpoints do not appear in the service catalog.

</td></tr></tbody>
</table><table id="table_jzv_xsf_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Endpoint ID.

</td></tr><tr><td>

Name \[name\]

</td><td>

Service name.

</td></tr><tr><td>

Interface \[interface\]

</td><td>

Interface type that describes the visibility of the endpoint. Possible values:-   Public - Visible by end users on a publicly available network interface.
-   Internal - Visible by end users on an unmetered internal network interface.
-   Admin - Visible by administrative users on a secure network interface.

</td></tr><tr><td>

Catalog enabled \[enabled\]

</td><td>

Defines whether the service and its endpoints appear in the service catalog.-   True - The service and its endpoints appear in the service catalog.
-   False - The service and its endpoints do not appear in the service catalog.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|The **name** field of OpenStack Flavor.|
|Object ID \[object\_id\]|The **id** field of OpenStack Flavor.|
|vCPUs \[vcpus\]|The **vcpus** field of OpenStack Flavor.|
|Memory MB \[memory\_mb\]|The **ram** field of OpenStack Flavor.|
|Local Storage GB \[local\_storage\_gb\]|The **disk** field of OpenStack Flavor.|

The discovered data includes the OpenStack Hypervisor View \[cmdb\_ci\_openstack\_hypervisor\_view\] table and its fields for private cloud only.

|Field|Description|
|-----|-----------|
|Name \[name\]|Concatenated value of **hypervisor\_type** and **hypervisor\_hostname** fields. For example: QEMU@host.acmecorp.com.|
|IP Address \[ip\_address\]|The value of **host\_ip** field.|
|Hypervisor technology \[hypervisor\_technology\]|The value of **hypervisor\_type** field.|
|Object ID \[object\_id\]|The value of **id** field.|
|State \[state\]|The value of **state** field.|
|Version \[version\]|The value of **hypervisor\_version** field.|

The Dependency Views map shows all discovered OpenStack resources in your organization that are available through REST API calls and the relationships between them.

![CIs and connections on a Dependency Views map](../image/openstack-network-dependency.PNG "OpenStack Network Dependency")

![CIs and connections on a Dependency Views map](../image/openstack-VM-dependency.PNG "OpenStack VM Dependency")

## CI relationships

The relationships listed in the following table are created to support OpenStack resource discovery.

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_openstack\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_cloud\_openstack\_service|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_cloud\_openstack\_endpoint|Use endpoint to::Use endpoint from|cmdb\_ci\_cloud\_openstack\_service|
|cmdb\_ci\_cloud\_openstack\_endpoint|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_cloud\_openstack\_domain|Owns::Owned by|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_network|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_network|Contains::Contained by|cmdb\_ci\_cloud\_subnet|
|cmdb\_ci\_compute\_security\_group|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_compute\_security\_group|Contains::Contained by|cmdb\_ci\_compute\_security\_group\_rule|
|cmdb\_ci\_cloud\_load\_balancer|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_cloud\_load\_balancer|Contains::Contained by|cmdb\_ci\_lb\_listener|
|cmdb\_ci\_lb\_pool|Hosted on::Hosts|cmdb\_ci\_cloud\_load\_balancer|
|cmdb\_ci\_lb\_pool|Owns::Owned by|cmdb\_ci\_lb\_pool\_member|
|cmdb\_ci\_storage\_volume|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_vm\_instance|Uses::Used by|cmdb\_ci\_storage\_volume|
|cmdb\_ci\_storage\_vol\_snapshot|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_storage\_vol\_snapshot|Provisioned from::Provisioned|cmdb\_ci\_storage\_volume|
|cmdb\_ci\_vm\_instance|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_cloud\_key\_pair|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_os\_template|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_vm\_instance|Provisioned from::Provisioned|cmdb\_ci\_os\_template|
|cmdb\_ci\_vm\_instance|Virtualized by::Virtualizes|cmdb\_ci\_server|

The relationships listed in the following table are created to support OpenStack resource discovery in private cloud only.

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_vm\_instance|Registered on::Has registered|cmdb\_ci\_openstack\_hypervisor\_view|
|cmdb\_ci\_openstack\_hypervisor\_view|Hosted on::Hosts|cmdb\_ci\_openstack\_datacenter|
|cmdb\_ci\_openstack\_hypervisor\_view|Uses::Hosts Used by|cmdb\_ci\_server|

**Parent Topic:**[Available cloud discovery patterns](../concept/available-patterns-cloud.md)

