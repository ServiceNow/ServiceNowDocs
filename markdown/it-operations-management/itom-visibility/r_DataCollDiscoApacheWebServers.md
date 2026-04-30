---
title: Apache web server discovery
description: Discovery identifies and classifies information about Apache web servers on both Windows and Linux computers.Discovery uses SSH to find Apache connectors mod\_jk and mod\_proxy.For an Apache web server the Unix - Active Processes probe requires sudo privileges.The Apache mod\_jk module forwards requests from the Apache web server to a Servlet container, such as Tomcat.The Apache mod\_proxy module implements a proxy, gateway, or cache for the Apache web server.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Apache web server discovery

Discovery identifies and classifies information about Apache web servers on both Windows and Linux computers.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Credentials

-   [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

## Classifier, patterns, and probes

<table id="table_qbq_2qh_lbb"><thead><tr><th>

Classifier

</th><th>

Trigger probes

</th><th>

Patterns

</th></tr></thead><tbody><tr><td>

Apache Server

</td><td>

-   Horizontal discovery probe: Launches patterns
-   Apache - Version\*
-   Apache - Get Configuration\*
-   Apache - Get JK ModuleApache - Get Proxy Module\*

</td><td>

-   Apache On Windows Pattern
-   Apache On Unix Pattern

</td></tr></tbody>
</table>\*For new instances, these probes are inactive on the classifier. Discovery uses patterns for discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected using probes

Discovery collects the following data on the Apache \[cmdb\_ci\_apache\_web\_server\] table for both Unix and Windows:

|Label|Field name|
|-----|----------|
|Name|name|
|Version|version|
|Description|description|
|TCP port\(s\)|tcp\_port|

## Connections found by Service Mapping during top-down discovery

Service Mapping uses discovery patterns to discover the following connections:

-   Any application using java
-   Any application using the LDAP port
-   Oracle WebLogic Module Oracle, and WebLogic Server \(version 10.3\)
-   \(On Windows only\) Jiva applications
-   \(On Windows only\) Tomcat server
-   \(On UNIX only\) Applications discovered using the mod\_jk process
-   \(On UNIX only\) Hosts to which the Apache web server is connecting in the load balancing mode
-   \(On UNIX only\) Epic application

**Parent Topic:**[Software discovery](../concept/c_Software.md)

## Apache mod\_jk and mod\_proxy discovery

Discovery uses SSH to find Apache connectors mod\_jk and mod\_proxy.

Discovery uses the **Unix - Active Processes** probe to identify an Apache web server process by matching one of the following criteria: the **name** of the process is:

-   httpd, or
-   apache, or
-   httpd2, or
-   httpd2-prefork
-   httpd.worker

If there is a match on one of these criteria, a record is created in the Web Server \[cmdb\_ci\_web\_server\] table if one does not already exist for that running process.

The following probes are triggered after classification:

|Probe|Description|Commands|
|-----|-----------|--------|
|Apache – Version|The sensor of this probe populates the Apache version information in the Web Server record.|httpd|
|Apache – Get Configuration|This probe contains a Bourne shell script and an argument that determines the path of the Apache configuration file. The sensor of this probe populates some additional information in the Web Server record.|echo, sed, httpd, cut, grep, egrep \(within the Borne shell script\)|

The sensor processing of the **Apache – Get Configuration** probe identifies whether either the mod\_jk or mod\_proxy modules are present and triggers the appropriate probe.

|Probe|Description|Commands|
|-----|-----------|--------|
|Apache – Get JK Module|If the mod\_jk module is running as a load balancer on the server, the sensor of this probe populates the information in the Load Balancer Service \[cmdb\_ci\_lb\_service\], Load Balancer Pool \[cmdb\_ci\_lb\_pool\] and Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\] tables.|echo, sed, httpd, cut, grep, egrep \(within the Borne shell script\)|
|Apache – Get Proxy Module|If the mod\_proxy module is running as a load balancer on the server, the sensor of this probe populates the information in the Load Balancer Service \[cmdb\_ci\_lb\_service\], Load Balancer Pool \[cmdb\_ci\_lb\_pool\] and Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\] tables.|grep, egrep \(within the Borne shell script\)|

In addition to data population, the following relationships are created in the CI Relationship \[cmdb\_rel\_ci\] table:

-   The records in the cmdb\_ci\_lb\_appl table run on the cmdb\_ci\_web\_server table records.
-   The records in the cmdb\_ci\_lb\_service table use the cmdb\_ci\_lb\_pool table records.
-   The records in the cmdb\_ci\_lb\_pool table are used by the cmdb\_ci\_service table record.
-   The records in the cmdb\_ci\_lb\_pool table are members of the cmdb\_ci\_lb\_pool\_member table.
-   The records in the cmdb\_ci\_lb\_pool\_member table are members of the cmdb\_ci\_lb\_pool table.

## Legacy: Add sudo access for the Unix - Active Processes probe

For an Apache web server the Unix - Active Processes probe requires sudo privileges.

### Before you begin

Role required: admin

### About this task

You can configure the Unix - Active Processes probe to elevate privileges.

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Probes**.

2.  In the **Search** field, search for Unix - Active Processes.

3.  Click field, search for Unix - Active Processes probe.

4.  In the **Probe Parameters** related list, click**New**.

5.  Click **New**

6.  Use the following information to fill out the form:

    |Probe|Commands|
    |-----|--------|
    |Name|must\_sudo|
    |Value|true|

7.  Click **Submit**


## Data collected by Mod\_jk module

The Apache mod\_jk module forwards requests from the Apache web server to a Servlet container, such as Tomcat.

Additional mod\_jk directives can also manage load balancing. Discovery populates the CMDB when it detects an Apache Server. When the Apache Web Server process is detected, if the mod\_jk module is running on the web server as a load balancer, the related information populates to the CMDB.

-   The MID Server user account to explore the target server must have access to the httpd.conf configuration file in the /etc/httpd/conf/ folder.
-   Discovery uses secure shell \(SSH\) commands to identify the following associated elements:
    -   Apache Get Configuration
    -   Apache Version
    -   Apache Get JK Module
-   The following probes require execute privileges to run commands:

    |Probe|Command|
    |-----|-------|
    |Apache – Get Configuration|echo, sed, httpd, cut, grep, egrep \(within the Borne shell script\)|
    |Apache – Version|httpd|
    |Apache – Get JK Module|echo, sed, httpd, cut, grep, egrep \(within the Borne shell script\)|


### Probes and sensors

Discovery uses the Unix - Active Processes probe to identify an Apache server that contains the mod\_jk module:

1.  The Unix - Active Processes probe detects a running process that matches one of the following criteria:
    -   The name of the process is httpd.
    -   The name of the process is apache.
2.  If there is a match on one of these criteria, a record is created in the Web Server table \[cmdb\_ci\_web\_server\] if one does not already exist for that running process. The following probes are also triggered:
    -   Apache – Version: the sensor of this probe populates the Apache version information in the Web Server record.
    -   Apache – Get Configuration: this probe contains a Bourne shell script and an argument that determines the path of the Apache configuration file. The sensor of this probe populates some additional information in the Web Server record.
3.  The sensor processing of Apache – Get configuration probe results triggers the following probes if the mod\_jk module is running on the web server:

    Apache – JK Module: if the mod\_jk module is running as a load balancer on the server, the sensor of this probe populates the information in the Load Balancer Service \[cmdb\_ci\_lb\_service\], Load Balancer Pool \[cmdb\_ci\_lb\_pool\] and Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\] tables.


### Data Collected

For the mod\_jk module with no load balancer, the following data is collected by default:

|Table Name|Field and Label Name|Probe|
|----------|--------------------|-----|
|cmdb\_ci\_web\_server|Name \[name\]|Apache – Get Configuration|
|cmdb\_ci\_web\_server|Version \[version\]|Apache – Version|
|cmdb\_ci\_web\_server|Description \[short\_description\]|Apache – Version|

If the mod\_jk module is enabled for load balancing, Discovery connects the following data:

|Table Name|Field and Label Name|Probe|
|----------|--------------------|-----|
|cmdb\_ci\_lb\_appl|Name \[name\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_appl|IP Address \[ip\_address\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_appl|Last Discovered \[last\_discovered\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_pool\_member|Name \[name\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_pool\_member|Last Discovered \[last\_discovered\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_pool\_member|IP Address \[ip\_address\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_pool\_member|Load Balancer \[load\_balancer\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_pool\_member|Port \[port\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_service|Input URL \[Input\_url\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_service|Last Discovered \[last\_discovered\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_service|IP Address \[ip\_address\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_service|Name \[name\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_service|Load Balancer \[load\_balancer\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_service|Port \[port\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_pool|Last Discovered \[last\_discovered\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_pool|Load balancing Method \[load\_balancing\_method\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_pool|Load Balancer \[load\_balancer\]|Apache – Apache - Get JK Module|
|cmdb\_ci\_lb\_pool|Name \[name\]|Apache – Apache - Get JK Module|

### Relationships

In addition to data population, the following relationships are created in the CI Relationship \[cmdb\_rel\_ci\] table:

-   The records in the cmdb\_ci\_lb\_appl table run on the cmdb\_ci\_web\_server table records.
-   The records in the cmdb\_ci\_lb\_service table use the cmdb\_ci\_lb\_pool table records.
-   The records in the cmdb\_ci\_lb\_pool table are used by the cmdb\_ci\_service table record.
-   The records in the cmdb\_ci\_lb\_pool table are members of the cmdb\_ci\_lb\_pool\_member table.
-   The records in the cmdb\_ci\_lb\_pool\_member table are members of the cmdb\_ci\_lb\_ pool table.

## Data collected by Mod\_proxy module

The Apache mod\_proxy module implements a proxy, gateway, or cache for the Apache web server.

An additional mod\_proxy\_balancer can also manage load balancing. Discovery populates the CMDB when it detects an Apache server. When the Apache Web Server process is detected, if the mod\_proxy module is running on the web server as a load balancer the related information populates to the CMDB.

Consider the following requirements for discovering an Apache server that contains the mod\_proxy module:

-   The MID Server user account to explore the target server must have access to the \[httpd.conf\] configuration file in the /etc/httpd/conf/ folder.
-   Discovery uses secure shell \(SSH\) commands to identify the following associated elements:
    -   Apache Get Configuration
    -   Apache Version
    -   Apache Get Proxy Module
-   The following probes require execute privileges to run commands:

    |Probe|Commands|
    |-----|--------|
    |Apache – Get Configuration|echo, sed, httpd, cut, grep, egrep \(within the Borne shell script\)|
    |Apache – Get Proxy Module|grep, egrep \(within the Borne shell script\)|
    |Apache – Version|httpd|


### Probes and sensors

Discovery uses the Unix - Active Processes probe to identify an Apache server that contains the mod\_proxy module. The probes and sensors operate in the following manner:

1.  The Unix - Active Processes probe detects a running process that matches one of the following criteria:
    -   The name of the process is httpd.
    -   The name of the process is apache2.
2.  If there is a match on one of these criteria, a record is created in the Web Server table \[cmdb\_ci\_web\_server\] if one does not already exist for that running process. The following probes are also triggered:
    -   Apache – Version: the sensor of this probe populates the Apache version information in the Web server \[cmdb\_ci\_web\_server\] record.
    -   Apache – Get Configuration: this probe contains a Bourne shell script and an argument that determines the path of the Apache configuration file. The sensor of this probe populates some additional information in the Web server \[cmdb\_ci\_web\_server\] record.
3.  The sensor processing of the Apache – Get configuration probe results triggers the following probes if the mod\_proxy module is running on the web server:

    Apache - Get Proxy Module: if the mod\_proxy module is running as a load balancer on the server, the sensor of this probe populates the information in the Load Balancer Service \[cmdb\_ci\_lb\_service\], Load Balancer Pool \[cmdb\_ci\_lb\_pool\] and Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\] tables.


### Data Collected

For the mod\_proxy module with no load balancer, the following data is collected by default:

|Table Name|Field and Label Name|Probe|
|----------|--------------------|-----|
|cmdb\_ci\_web\_server|Name \[name\]|Apache – Get Configuration|
|cmdb\_ci\_web\_server|Version \[version\]|Apache – Version|
|cmdb\_ci\_web\_server|Description \[short\_description\]|Apache – Version|

If the mod\_proxy module is enabled for load balancing, Discovery connects the following data:

|Table Name|Field and Label Name|Probe|
|----------|--------------------|-----|
|cmdb\_ci\_lb\_appl|IP Address \[ip\_address\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_appl|Last Discovered \[last\_discovered\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_pool\_member|Name \[name\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_pool\_member|Last Discovered \[last\_discovered\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_pool\_member|IP Address \[ip\_address\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_pool\_member|Load Balancer \[load\_balancer\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_pool\_member|Port \[port\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_service|Input URL \[Input\_url\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_service|Last Discovered \[last\_discovered\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_service|IP Address \[ip\_address\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_service|Name \[name\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_service|Load Balancer \[load\_balancer\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_service|Port \[port\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_pool|Last Discovered \[last\_discovered\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_pool|Load balancing Method \[load\_balancing\_method\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_pool|Load Balancer \[load\_balancer\]|Apache - Get Proxy Module|
|cmdb\_ci\_lb\_pool|Name \[name\]|Apache - Get Proxy Module|

### Relationships

In addition to data population, the following relationships are created in the CI Relationship \[cmdb\_rel\_ci\] table:

-   The records in the cmdb\_ci\_lb\_appl table run on the cmdb\_ci\_web\_server table records.
-   The records in the cmdb\_ci\_lb\_service table use the cmdb\_ci\_lb\_pool table records.
-   The records in the cmdb\_ci\_lb\_pool table are used by the cmdb\_ci\_service table records.
-   The records in the cmdb\_ci\_lb\_pool are members of the cmdb\_ci\_lb\_pool\_member table records.
-   The records in the cmdb\_ci\_lb\_pool\_member is a member of the cmdb\_ci\_lb\_pool table records.

