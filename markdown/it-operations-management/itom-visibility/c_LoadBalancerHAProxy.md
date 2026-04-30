---
title: HAProxy load balancer discovery using probes
description: Discovery of HAProxy Community edition load balancers is performed by SSH.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# HAProxy load balancer discovery using probes

Discovery of HAProxy Community edition load balancers is performed by SSH.

**Note:** Starting with Discovery and Service Mapping Patterns 1.15.0 version, pattern-based discovery is the default method for discovering HAProxy load balancers.

-   For information about enabling probe-based discovery, see [Enable HAProxy load balancer discovery with probes](../task/enable-haproxy-lb-discovery-probe.md).
-   For information about the HA Proxy pattern, see [HAProxy load balancer discovery with patterns](../../service-mapping/reference/haproxy-lb-discovery-pattern.md).
-   For information about Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

HAProxy is an open-source load balancer that can manage any TCP service. It is particularly suited for HTTP load balancing because it supports session persistence and Layer 7 processing. Discovery supports HAProxy for HTTP load balancing. TCP load-balancing is not supported.

Consider the following requirements for discovering the HAProxy:

-   The HAProxy software is installed and running on a Linux server.
-   The MID Server is deployed to explore the server and the MID Server has access to the server HAProxy configuration file.
-   The configuration probe checks for the `haproxy.cfg` file using one of the following methods:
    -   Using the **f** parameter for the HAProxy process output.
    -   Using the default `/etc/haproxy/haproxy.cfg` path.
-   The HAProxy probes require credentials and execute privileges to run commands.

Discovery uses the **Unix - Active Processes** probe to identify an HAProxy load balancer when the name of the process is haproxy. If this criterion matches, a record is created in the HAProxy Load Balancers \[cmdb\_ci\_lb\_haproxy\] table if one does not already exist for that running process.

The following probes are triggered after classification:

|Probe|Description|Commands|
|-----|-----------|--------|
|HAProxy – Version|The sensor of this probe populates the HAProxy version in the HAProxy Load Balancers \[cmdb\_ci\_lb\_haproxy\] table.|haproxy|
|HAProxy – Get Configuration|The sensor of this probe populates additional information in the HAProxy Load Balancers \[cmdb\_ci\_lb\_haproxy\] table. The probe also populates information in the Load Balancer Service \[cmdb\_ci\_lb\_service\], Load Balancer Pool \[cmdb\_ci\_lb\_pool\], Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\], Load Balancer Interface \[cmdb\_ci\_lb\_interface\], and Load Balancer Application \[cmdb\_ci\_lb\_appl\] tables.|echo, sed, cut, grep, egrep \(within the Borne shell script\)|

In addition to populating the data, the following relationships records are created in CI Relationships \[cmdb\_rel\_ci\] table:

-   The records in the cmdb\_ci\_lb\_appl table run on the cmdb\_ci\_web\_server table records.
-   The records in the cmdb\_ci\_lb\_service table use the cmdb\_ci\_lb\_pool table records.
-   The records in the cmdb\_ci\_pool table are used by the cmdb\_ci\_service table records.
-   The records in the cmdb\_ci\_pool table are members of the cmdb\_ci\_pool\_member table records.
-   The records in the cmdb\_ci\_pool\_member table are members of the cmdb\_ci\_pool table records.

