---
title: VMware NSX Advanced load balancer discovery
description: The ServiceNow Discovery application uses the VMware NSX Advanced load balancer discovery pattern to find VMware NSX load balancers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# VMware NSX Advanced load balancer discovery

The ServiceNow Discovery application uses the VMware NSX Advanced load balancer discovery pattern to find VMware NSX load balancers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The pattern uses a set of REST APIs to find the load balancers. It is triggered by the NSX HTTP classifier that responds to the **HTTP - Classify** probe. For more information, see [HTTP device discovery](../../discovery/concept/http-discovery.md).

**Note:** There are two patterns available. The legacy VMware NSX Load Balancer pattern is for the S series. The new VMware NSX-T Load Balancer pattern is for the T series. The functionality and collected information remain the same.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Enable NSX Basic Authentication**

    In VMware NSX, enable NSX Basic Authentication.

-   **Verify that the applications are up to date**
    -   CMDB CI Class Models
    -   Visibility Content
    -   Discovery and Service Mapping Patterns
-   **Configure basic authentication credentials**

    On the ServiceNow AI Platform, configure basic authentication credentials. The credentials must have the following API permissions:

    -   NSX:
        -   /api/4.0/edges
        -   /api/4.0/edges/&lt;edge\_id&gt;loadbalancer/config
    -   NSX-T: /api/v1/edge-clusters
    For more information about basic authentication credentials, see [Basic authentication credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_BasicAuthCredentialsForm.md).

-   **Verify HTTP discovery is triggered against the NSX Main Controller IP**

    The HTTP discovery is triggered only if SSH or SNMP discovery is unsuccessful.

-   **Create a discovery schedule**

    Create the discovery schedule for VMware NSX load balancer discovery or run a quick discovery on the IP address of the NSX Main Controller. For more information about running a quick discovery, see [Run a Quick Discovery](../../discovery/task/t_CreateADiscoverySchedule.md#).


## Data collected by Discovery for VMware NSX Advanced load balancer

Discovery populates the data in the CMDB when running the VMware NSX Advanced load balancer patterns.

|Field|Description|
|-----|-----------|
|Name \[name\]|Edge name.|
|Object ID \[object\_id\]|Edge ID.|
|IP Address \[ip\_address\]|IP address of the NSX Main Controller.|
|Operational status \[operational\_status\]|Load balancer status: Active or inactive.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Virtual server name.|
|IP Address \[ip\_address\]|Virtual server IP address.|
|Object ID \[object\_id\]|Virtual server object ID.|
|Port \[port\]|Virtual server port with which to communicate.|
|Listener Protocol \[listener\_protocol\]|Listener protocol. For example: HTTP, HTTPS.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Pool name.|
|Object ID \[object\_id\]|Pool object ID.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Pool member name.|
|IP Address \[ip\_address\]|Pool member IP address.|
|Object ID \[object\_id\]|Pool member object ID.|
|Service port \[service\_port\]|Pool member port with which to communicate.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Monitor name.|
|Object ID \[object\_id\]|Monitor object ID.|
|Timeout in seconds \[timeout\_sec\]|Time in seconds to wait for a response.|
|Interval in seconds \[check\_interval\_sec\]|Interval in seconds after which the monitor sends the request again.|
|Monitor type protocol \[monitor\_type\]|Monitor type. For example: HTTP, HTTPS, TCP.|
|Request path \[request\_path\]|Path where the monitor sends the request.|
|Max retries \[max\_retries\]|The maximum number of times the resource is tested before it is declared "Down".|

The Dependency Views map shows all discovered load balancer CIs and the relationships between them.

![CIs and connections on a Dependency Views map](../image/dependency-nsx.png)

## CI relationships

Discovery creates these relationships to support the VMware NSX load balancer discovery.

|CI|Relationship|CI|
|---|------------|---|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Runs on::Runs|NSX Load Balancer \[cmdb\_ci\_nsx\_lb\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Uses::Used by|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|NSX Load Balancer \[cmdb\_ci\_nsx\_lb\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Owns::Owned by|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|Hosted on::Hosts|NSX Load Balancer \[cmdb\_ci\_nsx\_lb\]|
|Cloud Load Balancer Health Service \[cmdb\_ci\_lb\_health\_service\]|Used by::Uses|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|

## Troubleshooting

If the mapping process does not proceed as you expected, follow the following suggestions.

<table id="table_ggn_ypj_yhb"><thead><tr><th>

Symptom

</th><th>

Cause

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Discovery fails. The discovery message contains the information about an error caused by the REST timeout.

</td><td>

There are many CIs sending the REST call response in the deployment. The MID Server cannot process the REST call response without exceeding the time limit controlled by the **mid.sa.cloud.request\_timeout** parameter.

</td><td>

By default, the **mid.sa.cloud.request\_timeout** parameter is set to 30000 milliseconds. Increase the value of this parameter on the relevant MID Server and run discovery again.

**Note:** If the **Configuration Parameters** related list for the relevant MID Server does not show this parameter, you may need to add it.

</td></tr><tr><td>

Pattern Designer fails during a debug session. The Pattern Designer message contains information about an error caused by a timeout.

</td><td>

The Pattern Designer fails because of a timeout during pattern debugging \(and not during discovery\).

</td><td>

By default, the **sa.debugger.max\_timeout**parameter is set to 240 seconds.Increase the value of this parameter on the relevant MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

