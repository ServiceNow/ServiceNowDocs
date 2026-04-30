---
title: NGINX web server discovery
description: NGINX is an open source web server with a load balancer. Discovery identifies the web server and information related to the load balancer.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# NGINX web server discovery

NGINX is an open source web server with a load balancer. Discovery identifies the web server and information related to the load balancer.

Discovery identifies NGINX server software using the following process:

1.  The NGINX Process Classifier detects a running process that matches the following criteria during the exploration of a Linux server:
    -   Name starts with nginx
    -   Name contains master
2.  If there is a match:
    -   A record is created in the NGINX Web Server \[cmdb\_ci\_nginx\_web\_server\] table.
    -   A Runs on relationship is created in the CI Relationship \[cmdb\_rel\_ci\] table for a Linux server \(Linux Server \[cmdb\_ci\_linux\_server\]\) and for an NGINX web server \(NGINX Web Server \[cmdb\_ci\_nginx\_web\_server\]\).

        The following two probes are triggered:

        -   NGINX – Version: This probe contains a Bourne shell script. It determines the version of NGINX and populates the NGINX Web Server \[cmdb\_ci\_nginx\_web\_server\] table.
        -   NGINX – Get Configuration: This probe contains a Bourne shell script and an argument that determines the path of the NGINX configuration file. The probe identifies configuration parameters based on keywords within the configuration file and returns them as a single payload result.
        The sensor on the ServiceNow instance parses the payload result and populates the CMDB.


You must have the following requirements to discover an NGINX webserver:

-   NGINX is installed and running on the server.
-   The MID Server has access to the NGINX configuration file, which is /`etc/nginx/nginx.conf` by default.

## Requirements

For NGINIX servers:

-   Ensure that the NGINX software is installed and running on the server.
-   Grant the MID Server has access to the NGINX configuration file, which is `/etc/nginx/nginx.conf` by default.
-   Enable secure shell \(SSH\) commands to identify the following associated elements:
    -   NGINX Version
    -   NGINX Get Configuration

The following probes require execute privileges to run commands:

|Probe|Commands|
|-----|--------|
|Nginx – Version|nginx|
|Nginx – Get Configuration|echo, sed, httpd, cut, grep, egrep \(within the Bourne shell script\)|

**Note:** The Nginx pattern performs top-down discovery on both Windows and Linux servers. For information on prerequisites for top-down discovery for NGINX web servers, see [Prerequisites for performing top-down discovery using Service Mapping](../../service-mapping/reference/prerequisites-service-mapping.md).

## Probes and Sensors

Discovery identifies NGINX server software using the following process:

1.  The Nginx Process Classifier detects a running process that matches the following criteria during the exploration of a UNIX server:
    -   The name of the process starts with `nginx`.
    -   The name of the process contains `master`.
2.  If there is a match:
    -   A record is created in the Web Server \[cmdb\_ci\_web\_server\] table.
    -   A Runs on relationship is created in the CI Relationship \[cmdb\_rel\_ci\] table for the Linux Server \[cmdb\_ci\_linux\_server\] table and the Web Server \[cmdb\_ci\_web\_server\] table.
3.  The following two probes are triggered:
    -   Nginx – Version: this probe contains a Bourne shell script. It determines the version of NGINX and populates the Web Server \[cmdb\_ci\_web\_server\] table.
    -   Nginx – Get Configuration: this probe contains a Bourne shell script and an argument that determines the path of the NGINX configuration file. The probe identifies configuration parameters based on keywords within the configuration file and returns them as a single payload result.
4.  The sensor on the ServiceNow instance processes the payload and populates the CMDB.

## Data Collected

Discovery creates or updates CMDB records when it detects a running NGINX process. The following data is collected.

|Table Name|Field and Label Name|Probe|
|----------|--------------------|-----|
|Name|cmdb\_ci\_lb\_appl \[name\]|Nginx– Get Configuration|
|IP Address|cmdb\_ci\_lb\_appl \[ip\_address\]|Nginx– Get Configuration|
|Last Discovered|cmdb\_ci\_lb\_appl \[last\_discovered\]|Nginx– Get Configuration|
|Version|cmdb\_ci\_lb\_appl \[version\]|Nginx– Version|
|Name|cmdb\_ci\_lb\_pool\_member \[name\]|Nginx– Get Configuration|
|Last Discovered|cmdb\_ci\_lb\_pool\_member \[last\_discovered\]|Nginx– Get Configuration|
|IP Address|cmdb\_ci\_lb\_pool\_member \[ip\_address\]|Nginx– Get Configuration|
|Load Balancer|cmdb\_ci\_lb\_pool\_member \[load\_balancer\]|Nginx– Get Configuration|
|Fully Qualified Domain Name|cmdb\_ci\_lb\_pool\_member \[fqdn\]|Nginx– Get Configuration|
|Port|cmdb\_ci\_lb\_pool\_member \[port\]|Nginx– Get Configuration|
|Last Discovered|cmdb\_ci\_lb\_service \[last\_discovered\]|Nginx– Get Configuration|
|IP Address|cmdb\_ci\_lb\_service \[ip\_address\]|Nginx– Get Configuration|
|Name|cmdb\_ci\_lb\_service \[name\]|Nginx– Get Configuration|
|Load Balancer|cmdb\_ci\_lb\_service \[load\_balancer\]|Nginx– Get Configuration|
|Input URL|cmdb\_ci\_lb\_service \[input\_url\]|NGINX – Get Configuration|

## Relationships

In the table \[cmdb\_rel\_ci\] the following relationships are populated:

-   The records in the cmdb\_ci\_lb\_appl table run on the cmdb\_ci\_web\_server table records.
-   The records in the cmdb\_ci\_lb\_service table use the cmdb\_ci\_lb\_pool table records.
-   The records in the cmdb\_ci\_pool table are used by the cmdb\_ci\_service table records.
-   The records in the cmdb\_ci\_pool table are members of the cmdb\_ci\_pool\_member table.
-   The records in the cmdb\_ci\_pool\_member table are members of cmdb\_ci\_pool table.

**Parent Topic:**[Software discovery](c_Software.md)

