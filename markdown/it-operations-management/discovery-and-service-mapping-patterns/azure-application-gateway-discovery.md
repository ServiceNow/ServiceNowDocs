---
title: Microsoft Azure Application Gateway discovery with Patterns
description: The ServiceNow Discovery application uses the Azure Application Gateway \(LP\) pattern for discovering this product, while the Service Mapping application discovers Application Gateway using the Azure Application Gateway TD \(LBS\) pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Microsoft Azure Application Gateway discovery with Patterns

The ServiceNow Discovery application uses the Azure Application Gateway \(LP\) pattern for discovering this product, while the Service Mapping application discovers Application Gateway using the Azure Application Gateway TD \(LBS\) pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Azure Principal credentials**

    On the ServiceNow platform, create a service account for cloud discovery. Set the account Id to the Azure Service Principal as it appears at the Microsoft Azure Console.

-   **Privileges**

    On the Microsoft Azure Console, provide a user a user with the reader role.


## Data collected by Discovery during horizontal discovery

<table id="table_olk_1pq_f56b"><thead><tr><th>

Table and field

</th><th>

Additional information

</th></tr></thead><tbody><tr><td colspan="2">

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td></tr><tr><td>

name

</td><td>

The name of the Azure Application Gateway.

</td></tr><tr><td>

Fqdn

</td><td>

The fully qualified domain name of the Azure Application Gateway.

</td></tr><tr><td>

Object\_id

</td><td>

The ID of the gateway.

</td></tr><tr><td>

Install\_status

</td><td>

The install status of the of the Azure Application Gateway.

</td></tr><tr><td>

state

</td><td>

The state of the Azure Application Gateway.

</td></tr><tr><td colspan="2">

Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]

</td></tr><tr><td>

name

</td><td>

The IP address of the Azure Application Gateway.

</td></tr><tr><td>

Object\_id

</td><td>

The ID of the Azure Application Gateway.

</td></tr><tr><td>

ipaddress \_type

</td><td>

The type of the IP address, which can be private or public.

</td></tr><tr><td>

ip\_address

</td><td>

The IP address of the Azure Application Gateway.

</td></tr><tr><td>

state

</td><td>

The state of the IP address of the Azure Application Gateway.

</td></tr><tr><td>

operational\_state

</td><td>

The operational state of the IP address of the Azure Application Gateway.

</td></tr><tr><td>

install\_status

</td><td>

The install status of the IP address of the Azure Application Gateway.

</td></tr><tr><td colspan="2">

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td></tr><tr><td>

serial number

</td><td>

The ID of the Azure Application Gateway service.

</td></tr><tr><td>

port

</td><td>

The TCP port that the Azure Application Gateway service listens to.

</td></tr><tr><td>

name

</td><td>

The FQDN with the port number of the Azure Application Gateway service, following this syntax: &lt;fqdn&gt;:&lt;port&gt;.

</td></tr><tr><td>

ip\_address

</td><td>

The IP address of the Azure Application Gateway on which the service runs.

</td></tr><tr><td>

object\_id

</td><td>

The ID of the Azure Application Gateway service.

</td></tr><tr><td>

operational\_state

</td><td>

The operational state of the Azure Application Gateway service.

</td></tr></tbody>
</table>## CI relationships

These relationships are created to support Azure Application Gateway discovery:

<table id="table_ysf_fpq_f987b"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td><td>

Hosted on::Hosts

</td><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td></tr><tr><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td><td>

Owns::Owned by

</td><td>

Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]

</td></tr><tr><td>

Resource Group \[cmdb\_ci\_resource\_group\]

</td><td>

Contains::Contained by

</td><td>

Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]

</td></tr></tbody>
</table>## Connections discovered by Service Mapping during the top-down discovery

Service Mapping performs the top-down discovery of the Azure Application Gateway in the context of application services. Service Mapping discovers the outgoing http connections from Azure Application Gateway service to pool members, such as virtual machines.

**Parent Topic:**[Available discovery patterns](available-patterns.md)

**Related topics**  


[Define a Cloud REST Query for cloud computing devices](../task/cloud-rest-query-pattern.md)

