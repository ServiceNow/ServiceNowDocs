---
title: HAProxy load balancer discovery with patterns
description: The Discovery and Service Mapping Patterns application uses the HA Proxy pattern to find HAProxy Community load balancers running on a Linux server. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2024-09-12"
reading_time_minutes: 3
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# HAProxy load balancer discovery with patterns

The Discovery and Service Mapping Patterns application uses the HA Proxy pattern to find HAProxy Community load balancers running on a Linux server. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

HAProxy Community edition is an open-source load balancer that can run in either TCP or HTTP mode. Note that although Discovery supports HAProxy for HTTP load balancing, TCP load balancing isn’t supported.

Starting with Discovery and Service Mapping Patterns 1.15.0 version, pattern-based discovery is the default method for discovering HAProxy load balancers. For information on probe-based HAProxy discovery, see [HAProxy load balancer discovery using probes](../../discovery/concept/c_LoadBalancerHAProxy.md).

**Note:** HAProxy discovery supports one-to-one relationship mapping between a front-end port and a back-end port. If multiple front-ends are connected to the same back-end, the discovery process will only map the relationship from the lowest front-end port number in a defined range to the back-end port.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To learn about HAProxy load balancers and their versions that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Verify HAProxy is installed on the Linux server**

    Verify the HAProxy software is installed and running on a Linux server.

-   **Verify permission to run HAProxy command**

    Verify you have permission to run the following command: `<HAproxy Installation Path>/haproxy -v`.

-   **Verify read access to HAProxy configuration file**

    Verify you have read access to the `haproxy.cfg` file.

-   **Create SSH credentials**

    For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the HA Proxy Pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the HAProxy load balancer.|
|Version \[version\]|Version of the HAProxy load balancer.|
|Description \[short\_description\]|Description of the HAProxy process, which is obtained by running the command: `haproxy -version`.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer in the following format: `<LB name>:<LB port>`.|
|Port \[port\]|Port on which the load balancer is listening.|
|IP Address \[ip\_address\]|IP address of the load balancer service.|
|Last port \[last\_port\]|Highest port number used by the load balancer service.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer pool.|
|Load balancer \[load\_balancer\]|HAProxy containing the load balancer pool.|
|Load balancing method \[load\_balancing\_method\]|Method used to load balance the pool, for example: Round Robin.|
|Most recent discovery \[last\_discovered\]|Timestamp of the most recent discovery.|
|Install Status \[install\_status\]|Install status of the load balancer pool, for example: Installed.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the load balancer pool member.|
|Service port \[service\_port\]|Port used by the pool member.|
|IP Address \[ip\_address\]|IP address of the pool member host.|
|Pool \[pool\]|Load balancer pool containing the pool member.|

## CI relationships

Discovery creates these relationships to support the HAProxy load balancer discovery.

|CI|Relationship|CI|
|---|------------|---|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|References|HAProxy Load Balancer \[cmdb\_ci\_lb\_haproxy\]|
|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|References|HAProxy Load Balancer \[cmdb\_ci\_lb\_haproxy\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|References|HAProxy Load Balancer \[cmdb\_ci\_lb\_haproxy\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Allocated to::Allocated from|Load Balancer Service \[cmdb\_ci\_lb\_service\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Owns::Owned by|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|References|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

