---
title: Data collected for IBM Cloud Discovery
description: Discovery collects information about cloud resources in the IBM Cloud Platform and creates relationships between the CIs it finds. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
keywords: [Patterns]
breadcrumb: [Cloud resource discovery references, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Data collected for IBM Cloud Discovery

Discovery collects information about cloud resources in the IBM Cloud Platform and creates relationships between the CIs it finds. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date.**
    -   Discovery and Service Mapping Patterns.
    -   CMDB CI Class Models.
    -   Visibility Content.
-   **Configure a discovery schedule**

    [Create a discovery schedule in Cloud Discovery Workspace](../task/cloud-operations-disco-create-schedule.md)


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Load balancers

<table id="table_ljg_k2n_fhb"><thead><tr><th>

Table

</th><th>

Field Name / Description

</th></tr></thead><tbody><tr><td rowspan="8">

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td><td>

**object\_id**: The load balancer's unique identifier.

</td></tr><tr><td>

**name**: Name of the load balancer.

</td></tr><tr><td>

**fqdn**: Address \(Host name\) of the load balancer. This is the fully qualified domain name of the load balancer.

</td></tr><tr><td>

**dns\_name**: Address \(Host name\) of the load balancer.

</td></tr><tr><td>

**short\_description**: Description of the load balancer.

</td></tr><tr><td>

**operational\_status**: The operational status of the load balancer, either **ONLINE** or **OFFLINE**.

</td></tr><tr><td>

**location**: References the load balancer's location with type.

</td></tr><tr><td>

**state**: Provisioning status of the load balancer, either **Available** or **Terminated**.

</td></tr><tr><td rowspan="6">

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td><td>

**object\_id**: Unique identifier of the load balancer service.

</td></tr><tr><td>

**name**: Name created by the pattern that contains the following:-   Load balancer name
-   Protocol
-   Port
-   Resource type: **-listener**

</td></tr><tr><td>

**port**: Listener's protocol port number.

</td></tr><tr><td>

**front\_end\_port**: Listener's protocol port number.

</td></tr><tr><td>

**listener\_protocol**: Listener's protocol, either **TCP**, **HTTP**, or **HTTPS**.

</td></tr><tr><td>

**operational\_status**: The provisioning status of the listener.

</td></tr><tr><td rowspan="5">

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td><td>

**object\_id**: Unique identifier of the load balancer pool.

</td></tr><tr><td>

**name**: Name created by the pattern that contains the following:-   Load balancer name
-   Protocol
-   Port
-   Resource type: **-pool**

</td></tr><tr><td>

**port**: Protocol port of the back end.

</td></tr><tr><td>

**pool\_status**: Provisioning status of a load balancer pool.

</td></tr><tr><td>

**load\_balancing\_method**: Method used to load balance the pool.

</td></tr><tr><td rowspan="5">

Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]

</td><td>

**object-id**: Unique identifier of the pool member, created from the ID of the member and the listener ID.

</td></tr><tr><td>

**name**: Name created by the pattern that contains the following:-   Load balancer name
-   Protocol
-   Port
-   Resource type: **-member**
-   IP address of the pool member

</td></tr><tr><td>

**ip\_address**: IP address of a load balancer member.

</td></tr><tr><td>

**server\_id**: ID of the member in the IBM Cloud.

</td></tr><tr><td>

**load\_balancer**: Name of the related load balancer.

</td></tr><tr><td rowspan="5">

Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]

</td><td>

**object\_id**: Unique identifier of the healthservice check.

</td></tr><tr><td>

**name**: Name created by the pattern that contains the following:-   Load balancer name
-   Protocol
-   Resource type: **Health Check**
-   Resource ID

</td></tr><tr><td>

**monitor\_type**: Type of health check. Valid values are **TCP**, **HTTP**, or **HTTPS**.

</td></tr><tr><td>

**timeout\_sec**: Timeout in seconds to wait for the health check response.

</td></tr><tr><td>

**check\_interval\_sec**: Interval in seconds to perform the health check.

</td></tr></tbody>
</table>|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|
|cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_cloud\_load\_balancer|Contains::Contained by|cmdb\_ci\_lb\_health\_service|
|cmdb\_ci\_cloud\_load\_balancer|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
|cmdb\_ci\_availability\_zone|Contains::Contained by|cmdb\_ci\_cloud\_load\_balancer|
|cmdb\_ci\_lb\_service|Hosted on::Hosts|cmdb\_ci\_cloud\_load\_balancer|
|cmdb\_ci\_availability\_zone|Contains::Contained by|cmdb\_ci\_lb\_service|
|cmdb\_ci\_lb\_pool|Hosted on::Hosts|cmdb\_ci\_cloud\_load\_balancer|
|cmdb\_ci\_lb\_service|Contains::Contained by|cmdb\_ci\_lb\_pool|
|cmdb\_ci\_lb\_pool|Owns::Owned by|cmdb\_ci\_lb\_pool\_member|

## Organizations and spaces

<table id="table_rf4_p5n_fhb"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

IBM Cloud Organizations \[cmdb\_ci\_cloud\_org\]

</td><td>

-   **guid**: The organization's unique identifier.
-   **url**: The organization's unique URL.
-   **billing\_enabled**: Indicates if the organization's billing method is enabled or disabled.
-   **name**: Unique name of the cloud organization.
-   **quota\_definition\_url**: Resources that are available to the organization.
-   **spaces\_url**: Unique URL of the space assigned to the organization.
-   **operational\_status**: Operational status of the organization.

</td></tr><tr><td>

IBM Cloud Space \[cmdb\_ci\_cloud\_space\]

</td><td>

-   **object\_id**: Unique identifier \(GUID\) of the space.
-   **name**: Unique name of the space.
-   **url**: Unique URL of the space.
-   **allow\_ssh**: The IP address of a storage resource.

</td></tr></tbody>
</table>|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|
|cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_cloud\_org|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_cloud\_space|Hosted on::Hosts|cmdb\_ci\_cloud\_org|
|cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_cloud\_space|

## SSH Keys

<table id="table_e2p_4ps_fhb"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Cloud Key Pairs \[cmdb\_ci\_cloud\_key\_pair\]

</td><td>

-   **object\_id**: ID of the SSH key record.
-   **name**: Descriptive name used to identify the SSH key.
-   **key**: The SSH key.
-   **finger\_print**: Short sequence of bytes used to authenticate or lookup a longer SSH key. This is generated automatically when adding or modifying the SSH key. This property is read only. Changes made are ignored.
-   **created\_date**: Date the SSH key was added. This property is read only. Changes made are ignored.
-   **modify\_date**: Date the SSH key was last modified. This property is read only. Changes made are ignored.
-   **short\_description**: Brief note about the SSH key.

</td></tr></tbody>
</table>|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_ibm\_datacenter|Contained by::Contains|cmdb\_ci\_availability\_zone|
|cmdb\_ci\_cloud\_key\_pair|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
|cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_cloud\_key\_pair|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|

## IBM Cloud storage

<table id="table_umt_15s_fhb"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

-   **object\_id**: Unique identifier of the storage account.
-   **size**: Capacity of the storage account, measured in gigabytes.
-   **size\_bytes**: Capacity of the storage account, measured in bytes.
-   **name**: Username used to access a non-EVault Storage volume. This username is used to register the EVault server agent with the vault backup system.
-   **label**: Network resource name for the storage.
-   **storage\_type**: Description of the storage object.
-   **fqdn**: IP address of the storage resource.
-   **device**: Unique identification number of the guest associated with the storage volume.

</td></tr><tr><td>

Storage Volume Snapshot \[cmdb\_ci\_storage\_vol\_snapshot\]

</td><td>

-   **object\_id**: Unique identifier of the storage account.
-   **name**: Name of the storage's network resource.
-   **capacity**: The volume's configured snapshot space size.
-   **fqdn**: IP address of the storage resource.
-   **location**: Unique availability zone where the storage volume is located.

</td></tr></tbody>
</table>|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_ibm\_datacenter|Contains::Contained by|cmdb\_ci\_availability\_zone|
|cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_storage\_volume|Provisioned::Provisioned From|cmdb\_ci\_storage\_vol\_snapshot|
|cmdb\_ci\_storage\_vol\_snapshot|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
|cmdb\_ci\_storage\_volume|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
|cmdb\_ci\_storage\_vol\_snapshot|Located in Zone::Zone contains|cmdb\_ci\_availability\_zone|
|cmdb\_ci\_availability\_zone|Contains::Contained by|cmdb\_ci\_storage\_volume|

## IBM Cloud virtual servers

<table id="table_pzn_yht_fhb"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]

</td><td>

-   **name**: Name of the virtual machine.
-   **object\_id**: ID of the virtual machine.
-   **dns\_domain**: Domain of the virtual machine.
-   **fqdn**: IP address of the virtual machine.
-   **short\_description**: Notes attached to the virtual machine on the IBM console.
-   **cpus**: Number of CPUs on the virtual machine.
-   **memory**: Amount of memory on the virtual machine.
-   **disks**: Number of disks used by the virutal machine.
-   **state**: The running state of the virtual machine. The choices are:
    -   **Running**
    -   **Halted**
-   **placement\_group\_id**: Name of the IBM placement group containing the virtual machine.
-   **nics**: Number of network interfaces on the virtual machine.

</td></tr><tr><td>

Cloud Mgmt Network Interface \[cmdb\_ci\_nic\]

</td><td>

-   **name**: Name and port of the NIC, in the format **&lt;name&gt;&lt;port&gt;**.
-   **ip\_address**: IP address configured on the NIC.
-   **mac\_address**: MAC address of the NIC.
-   **netmask**: Netmask of the NIC.
-   **object\_id**: ID of the NIC.
-   **status**: State of the NIC - AVAILABLE.

</td></tr><tr><td>

Image \[cmdb\_ci\_os\_template\]

</td><td>

-   **name**: Long description of the template. For example: **CentOS 7.0-64 Minimal for VSI**.
-   **version**: Operating system version. For example, **7.0-64 Minimal for VSI**.
-   **object\_id**: ID of the image.
-   **guest\_os**: Operating system of the virtual machine, such as Windows, Ubuntu, or CentOS.

</td></tr><tr><td>

Cloud Key Pair \[cmdb\_ci\_cloud\_key\_pair\]

</td><td>

-   **name**: The key label.
-   **object\_id**: ID of the key.

</td></tr><tr><td>

Compute Security Group \[cmdb\_ci\_compute\_security\_group\]

</td><td>

-   **name**: Security group name.
-   **object\_id**: ID of the security group
-   **short\_description**: Security group notes.

</td></tr><tr><td>

Storage Volume \[cmdb\_ci\_storage\_volume\]

</td><td>

**object\_id**: The storage volume ID.

</td></tr></tbody>
</table>|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_vm\_instance|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
|cmdb\_ci\_vm\_instance|Located in::Houses|cmdb\_ci\_availability\_zone|
|cmdb\_ci\_nic|Contained by::Contains|cmdb\_ci\_vm\_instance|
|cmdb\_ci\_os\_template|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_os\_template|Provisioned by::Provisions|cmdb\_ci\_vm\_instance|
|cmdb\_ci\_cloud\_key\_pair|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_cloud\_key\_pair|Used by::Uses|cmdb\_ci\_vm\_instance|
|cmdb\_ci\_compute\_security\_group|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_compute\_security\_group|Implement End Point From::Implement End Point To|cmdb\_ci\_vm\_instance|
|cmdb\_ci\_storage\_volume|Hosted on::Hosts|cmdb\_ci\_ibm\_datacenter|
|cmdb\_ci\_storage\_volume|Implement End Point From::Implement End Point To|cmdb\_ci\_vm\_instance|

## IBM Cloud service account

<table id="table_nf5_bg3_ghb"><thead><tr><th>

Table

</th><th>

Field

</th></tr></thead><tbody><tr><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

-   **name**: Display name of the cloud service account.
-   **account\_id**: Service account ID.
-   **object\_id**: Cloud ID of the service account. This is the same as the account\_id.
-   **datacenter\_type**: This is **cmdb\_ci\_ibm\_datacenter**.
-   **discovery\_credentials**: The sys\_id of the credentials.

</td></tr><tr><td>

IBM Datacenter \[cmdb\_ci\_ibm\_datacenter\]

</td><td>

-   **name**: Display name of the cloud service account.
-   **account\_id**: Service account ID.
-   **object\_id**: Cloud ID of the service account. This is the same as the account\_id.
-   **datacenter\_type**: This is **cmdb\_ci\_ibm\_datacenter**.

</td></tr></tbody>
</table>|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_cloud\_service\_account|Contained by::Contains|cmdb\_ci\_availability\_zone|
|cmdb\_ci\_cloud\_service\_account|Contained by::Contains|cmdb\_ci\_ibm\_datacenter|
|cmdb\_ci\_cloud\_service\_account|Hosts::Hosted on|cmdb\_ci\_cloud\_key\_pair|
|cmdb\_ci\_cloud\_service\_account|Hosts::Hosted on|cmdb\_ci\_vm\_instance|
|cmdb\_ci\_cloud\_service\_account|Hosts::Hosted on|cmdb\_ci\_lb\_service|
|cmdb\_ci\_ibm\_datacenter|Contained by::Contains|cmdb\_ci\_availability\_zone|
|cmdb\_ci\_ibm\_datacenter|Hosted on::Hosts|cmdb\_ci\_cloud\_service\_account|
|cmdb\_ci\_ibm\_datacenter|Hosts::Hosted on|cmdb\_ci\_network|

**Parent Topic:**[Cloud resource discovery references](cloud-discovery-collected-data.md)

