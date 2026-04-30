---
title: NGINX load balancer discovery
description: Discovery of NGINX load balancers is performed by SSH.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# NGINX load balancer discovery

Discovery of NGINX load balancers is performed by SSH.

NGINX is an open source web server with a load balancer. Discovery identifies the web server and information related to the load balancer.

Consider the following requirements for discovering NGINIX servers:

-   Ensure that the NGINX software is installed and running on the server.
-   Grant the MID Server has access to the NGINX configuration file, which is `/etc/nginx/nginx.conf` by default.
-   Enable secure shell \(SSH\) commands.
-   The NGINX probes require credentials and execute privileges to run commands.

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

The Nginx Process Classifier detects a running process that matches the following criteria during the exploration of a UNIX server:

-   The name of the process starts with nginx.
-   The name of the process contains master.

Both of these conditions must match:

-   A record is created in the Web Server \[cmdb\_ci\_web\_server\] table.
-   A **Runs on** relationship is created in the CI Relationship \[cmdb\_rel\_ci\] table for the Linux Server \[cmdb\_ci\_linux\_server\] table and the Web Server \[cmdb\_ci\_web\_server\] table.

The following probes are triggered after classification:

|Probe|Description|Commands|
|-----|-----------|--------|
|Nginx – Version|This probe contains a Bourne shell script. It determines the version of NGINX and populates the Web Server \[cmdb\_ci\_web\_server\] table.|nginx|
|Nginx – Get Configuration|This probe contains a Bourne shell script and an argument that determines the path of the NGINX configuration file. The probe identifies configuration parameters based on keywords within the configuration file and returns them as a single payload result.|echo, sed, cut, grep, egrep \(within the Bourne shell script\)|

In addition to populating the data, the following relationships records are created in CI Relationships \[cmdb\_rel\_ci\] table:

-   The records in the cmdb\_ci\_web\_server table run on the cmdb\_ci\_linux\_server table records.
-   The records in the cmdb\_ci\_lb\_service table use the cmdb\_ci\_lb\_pool table records.
-   The records in the cmdb\_ci\_pool table are used by the cmdb\_ci\_service table records.
-   The records in the cmdb\_ci\_pool table are members of the cmdb\_ci\_pool\_member table records.
-   The records in the cmdb\_ci\_pool\_member table are members of the cmdb\_ci\_pool table records.

**Parent Topic:**[Load balancer discovery](c_LoadBalancers.md)

