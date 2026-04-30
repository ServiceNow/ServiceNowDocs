---
title: IBM WebSEAL discovery
description: The Discovery application uses the IBM WebSEAL patterns to find WebSEAL applications, web application servers, and junctions on your infrastructure. Discovering some of these resources requires installing the Discovery and Service Mapping Patterns application from the Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [WebSEAL, IBM, Security Access Manager, ISAM]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM WebSEAL discovery

The ® Discovery application uses the IBM WebSEAL patterns to find WebSEAL applications, web application servers, and junctions on your infrastructure. Discovering some of these resources requires installing the Discovery and Service Mapping Patterns application from the ® Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Detailed information on IBM WebSEAL**

    For information, see [Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md)

-   **Authentication**

    The WebSEAL authentication process includes HTTP header authentication with basic credentials [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

    If you’re running discovery for the first time, configure Credential affinity for Discovery and Orchestration [Credential affinity for Discovery and Orchestration](https://www.servicenow.com/docs/access?context=c_CredentialAffinity&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

    **Note:** Credential affinity isn’t available In debug mode.

-   **Configured MID Server**

    Ensure the MID Server has access and permissions to send HTTPS requests to the WebSEAL application.

-   **Configured user permissions to execute API calls**

    Ensure that the user has the permission to run the following API:

    -   /net/general

    -   /net/dns

    -   /wga/reverseproxy

    -   /wga/reverseproxy/&lt;reverse\_proxy\_id&gt;/configuration/stanza/junction/entry\_name/match-vhj-first

    -   /wga/reverseproxy/&lt;reverse\_proxy\_id&gt;/junctions
    -   /wga/reverseproxy/"&lt;reverse\_proxy\_id&gt;/junctions?junctions\_id=&lt;junction\_id&gt;

    -   /wga/widgets/health.json

-   **HTTP Classification enabled**

    The IBM WebSEAL Pattern is triggered when you run the discovery on the server that the WebSEAL is on. Ensure that the HTTP Classification is present in the instance. For more information, see [Create an HTTP classification](../../discovery/task/create-an-http-classifier.md) and [Run discovery through an HTTP or HTTPS REST call](../../discovery/task/run-http-discovery.md)


## Data collected during horizontal discovery

<table id="table_olj_wwb_x5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

ISAM Server \[cmdb\_ci\_isam\_server\] 

</td></tr><tr><td>

name

</td><td>

The name of the server as returned by the `/net/general` API call. If the field is empty, `nslookup` on the IP address would be attempted to populate this field.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

The IP address according to the discovery schedule/configuration.

</td></tr><tr><td>

fqdn

</td><td>

The `search_domain` returned by the`/net/dns` API call.

</td></tr><tr><td class="sub-head" colspan="2">

WebSEAL \[cmdb\_ci\_app\_server\_webseal\]

</td></tr><tr><td>

name

</td><td>

The name of the WebSEAL server as returned by the API.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

The IP address according to the discovery schedule/configuration.

</td></tr><tr><td>

fqdn

</td><td>

The `search_domain` returned by the`/net/dns` API call.

</td></tr><tr><td>

install\_status

</td><td>

The status is set to **installed** by default.

</td></tr><tr><td>

operation\_status

</td><td>

The status is set to **operational** by default.

</td></tr><tr><td>

install\_directory

</td><td>

According to the identification requirement, this field is populated with the FQDN of the server.

</td></tr><tr><td class="sub-head" colspan="2">

WebSEAL Reverse Proxies \[cmdb\_ci\_webseal\_reverse\_proxy\]

</td></tr><tr><td>

name

</td><td>

The name of the resource according to the API response.

</td></tr><tr><td>

object\_id

</td><td>

The ID of the resource, of the API response.

</td></tr><tr><td>

install\_status

</td><td>

Indicates if the installation is enabled.

</td></tr><tr><td>

operational\_status

</td><td>

Indicates if the operation has started.

</td></tr><tr><td>

service\_type – hard-coded

</td><td>

The status is set to `Webseal Reverse Proxy`by default.

</td></tr><tr><td>

webseal\_health\_status

</td><td>

The WebSEAL reported health status regarding the `/wga/widgets/health.json` API call

</td></tr><tr><td class="sub-head" colspan="2">

WebSEAL Junctions \[cmdb\_ci\_webseal\_junction\]

</td></tr><tr><td>

name

</td><td>

The name of the resource according to the API response.

</td></tr><tr><td>

object\_id

</td><td>

The id of the resource, created as a unique hash number corresponding to the case-sensitive name of the resource.

**Note:** The case insensitivity of the queries may create duplicate fields when the **name** value is identical to the **Object ID** value. One of the identification attributes must be changed to have a unique value.

</td></tr><tr><td>

install\_status

</td><td>

Hard-coded to installed status

</td></tr><tr><td>

operational\_status

</td><td>

Hard-coded to operational status

</td></tr><tr><td>

stateful\_junction

</td><td>

Boolean value indicating whether it’s a stateful Junction

</td></tr><tr><td>

transparent\_path\_junction

</td><td>

Boolean value indicating whether it’s a transparent path Junction

</td></tr><tr><td>

junction\_type

</td><td>

List for the type of the Junction

</td></tr><tr><td class="sub-head" colspan="2">

WebSEAL Backend Servers \[cmdb\_ci\_webseal\_backend\_server\]

</td></tr><tr><td>

name

</td><td>

the name of the resource, as per API response

</td></tr><tr><td>

object\_id

</td><td>

the id of the resource, as per API response

</td></tr><tr><td>

install\_status

</td><td>

the status of the resource as per the “enabled” value in the API response

</td></tr><tr><td>

operational\_status

</td><td>

the status of the resource as per the “operation state” value

</td></tr><tr><td>

server\_id

</td><td>

The UUID used to identify the junction web server

</td></tr><tr><td>

http\_port

</td><td>

HTTP port of the back-end third-party server. Applicable when the junction type is tcp.

</td></tr><tr><td>

service\_port

</td><td>

TCP port of the back-end third-party server. Default is 80 for TCP junctions and 443 for SSL junctions

</td></tr><tr><td>

Priority

</td><td>

The priority of the server \(1-9\). Default is 9.

</td></tr></tbody>
</table><table id="table_nxq_dcc_x5b"><thead><tr><th>

CI

</th><th>

Relationship Type

</th><th>

CI

</th></tr></thead><tbody><tr><td>

Webseal \[cmdb\_ci\_app\_server\_webseal\]

</td><td>

Runs on::Runs

</td><td>

ISAM Server \[cmdb\_ci\_isam\_server\]

</td></tr><tr><td>

Webseal Reverse Proxy \[cmdb\_ci\_webseal\_reverse\_proxy\]

</td><td>

Hosted on::Hosts

 Reference\[load\_balancer\]

</td><td>

Webseal \[cmdb\_ci\_app\_server\_webseal\]

</td></tr><tr><td>

Webseal Reverse Proxy \[cmdb\_ci\_webseal\_reverse\_proxy\]

</td><td>

Runs on::Runs

 Reference\[isam\_server\]

</td><td>

ISAM Server

 \[cmdb\_ci\_isam\_server\]

</td></tr><tr><td>

Webseal Junction \[cmdb\_ci\_webseal\_junction\]

</td><td>

Allocated to::Allocates

 Reference \[service\]

</td><td>

Webseal Reverse Proxy \[cmdb\_ci\_webseal\_reverse\_proxy\]

</td></tr><tr><td>

Webseal Junction \[cmdb\_ci\_webseal\_junction\]

</td><td>

Owns::Owned by

 Reference \[pool\]

</td><td>

Load Balancer Pool Member \[cmdb\_ci\_webseal\_backend\_server\]

</td></tr><tr><td>

Webseal Junction \[cmdb\_ci\_webseal\_junction\]

</td><td>

Reference only \[load\_balancer\]

</td><td>

Webseal \[cmdb\_ci\_app\_server\_webseal\]

</td></tr></tbody>
</table>**Note:** Currently, the relation between the back-end servers and actual server CIs in the CMDB isn’t possible for HD.

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

