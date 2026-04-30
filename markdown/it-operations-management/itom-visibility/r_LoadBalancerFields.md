---
title: Load balancer fields and probes
description: Discovery stores load balancer information in several tables.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Load balancer fields and probes

Discovery stores load balancer information in several tables.

The information in this topic pertains to discovery with probes and sensors only. If you are using patterns, such as to discover [F5 Big-IP load balancers](../concept/c_LoadBalancerF5BIGIP.md), see the relevant topic for that type of load balancer.

**Note:** By default, the system uses the discovered IP address of a load balancer for the CI record. This can be the management IP created for the device that is used in the Discovery schedule. For instructions on how to force Discovery to use the IP address of the load balancer's NIC rather than that of a management IP, see [IP address selection properties](discovery-ip-address-configuration.md#).

|Field label and name|Probes that gather data|
|--------------------|-----------------------|
|Serial Number \[serial\_number\]|SNMP - Netscaler - Identity - Serial|
|Asset tag \[asset\_tag\]|SNMP - Netscaler - Identity|
|Model ID \[model\_id\]|SNMP - Netscaler - Identity|

|Field label and name|Probes that gather data|
|--------------------|-----------------------|
|Serial Number \[serial\_number\]|Cisco GSS - Serial Number|
|Model ID \[model\_id\]|Cisco GSS - Identity|
|IP Address \[ip\_address\]|Cisco GSS - Network|
|Manufacturer \[manufacturer\]|Cisco GSS - Identity|

|Field label and name|Probes that gather data|
|--------------------|-----------------------|
|Serial Number \[serial\_number\]|SNMP - Load Balancer – Identity|
|Model ID \[model\_id\]|
|IP Address \[ip\_address\]|
|Manufacturer \[manufacturer\]|

|Field label and name|Probes that gather data|
|--------------------|-----------------------|
|Active modules \[active\_modules\]\*|SNMP - F5 BIG-IP - System|
|Asset tag \[asset\_tag\]|
|Model ID \[model\_id\]|
|Failover mode \[failover\_mode\]\*|
|Failover peer \[failover\_peer\]\*|
|Serial Number \[serial\_number\]|Cisco GSS - Serial Number|

\*not visible on the form by default. Customize the form to add this field.

<table id="table_ylt_w52_ct"><thead><tr><th>

Field label and name

</th><th>

Probes that gather data

</th></tr></thead><tbody><tr><td>

Operational status \[operational\_status\]

</td><td rowspan="2">

-   Apache - Get JK Module
-   Apache - Get Proxy Module
-   HAProxy - Get Configuration
-   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System
-   SNMP - Load Balancer - Identity

</td></tr><tr><td>

Name \[name\]

</td></tr></tbody>
</table><table id="table_bj4_p52_ct"><thead><tr><th>

Field label and name

</th><th>

Probes that gather data

</th></tr></thead><tbody><tr><td>

Configuration file \[config\_file\]\*

</td><td>

Nginx - Get Configuration

</td></tr><tr><td>

Name \[name\]

</td><td rowspan="3">

-   Apache - Get JK Module
-   Apache - Get Proxy Module
-   HAProxy - Get Configuration
-   Nginx - Get Configuration

</td></tr><tr><td>

IP Address \[ip\_address\]\*

</td></tr><tr><td>

Most recent discovery \[last\_discovered\]\*

</td></tr><tr><td>

Version \[version\]

</td><td>

-   Apache - Version
-   HAProxy - Version
-   Nginx - Version

</td></tr></tbody>
</table><table id="table_ang_kv2_ct"><thead><tr><th>

Field label and name

</th><th>

Probes that gather data

</th></tr></thead><tbody><tr><td>

Status \[install\_status\]\*

</td><td rowspan="3">

-   Apache - Get JK Module
-   Apache - Get Proxy Module
-   HAProxy - Get Configuration
-   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System

</td></tr><tr><td>

Load Balancer \[load\_balancer\]

</td></tr><tr><td>

Name \[name\]

</td></tr></tbody>
</table>\*not visible on the form by default. Customize the form to add this field.

<table id="table_ccn_rv2_ct"><thead><tr><th>

Field label and name

</th><th>

Probes that gather data

</th></tr></thead><tbody><tr><td>

Load Balancing Method \[load\_balance\_method\]

</td><td rowspan="4">

-   Apache - Get JK Module
-   Apache - Get Proxy Module
-   HAProxy - Get Configuration
-   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System

</td></tr><tr><td>

Load Balancer \[load\_balancer\]

</td></tr><tr><td>

Most recent discovery \[last\_discovered\]\*

</td></tr><tr><td>

Name \[name\]

</td></tr></tbody>
</table>\*not visible on the form by default. Customize the form to add this field.

<table id="table_xgv_cw2_ct"><thead><tr><th>

Field label and name

</th><th>

Probes that gather data

</th></tr></thead><tbody><tr><td>

Fully qualified domain name \[fqdn\]\*

</td><td>

-   HAProxy - Get Configuration
-   Nginx - Get Configuration
-   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td rowspan="6">

-   Apache - Get JK Module
-   Apache - Get Proxy Module
-   HAProxy - Get Configuration
-   Nginx- Get Configuration
-   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System

</td></tr><tr><td>

Load balancer \[load\_balancer\]

</td></tr><tr><td>

Most recent discovery \[last\_discovery\]\*

</td></tr><tr><td>

Name \[name\]

</td></tr><tr><td>

Pool \[pool\]\*

</td></tr><tr><td>

Service Port \[service\_port\]

</td></tr></tbody>
</table>\*not visible on the form by default. Customize the form to add this field.

<table id="table_t44_3w2_ct"><thead><tr><th>

Field label and name

</th><th>

Probes that gather data

</th></tr></thead><tbody><tr><td>

Input URL \[input\_url\]

</td><td>

-   Apache - Get JK Module
-   Apache - Get Proxy Module
-   Nginx - Get Configuration

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

-   Apache - Get JK Module
-   Apache - Get Proxy Module
-   Cisco GSS - Identity
-   HAProxy - Get Configuration
-   Nginx - Get Configuration
-   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System

</td></tr><tr><td>

Last port \[last\_port\]\*

</td><td>

HAProxy - Get Configuration

</td></tr><tr><td>

Load Balancer \[load\_balancer\]

</td><td rowspan="3">

-   Apache - Get JK Module
-   Apache - Get Proxy Module
-   Cisco GSS - Identity
-   HAProxy - Get Configuration
-   Nginx - Get Configuration
-   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System

</td></tr><tr><td>

Most recent discovery \[last\_discovery\]\*

</td></tr><tr><td>

Service Port \[service\_port\]\*

</td></tr></tbody>
</table>\*not visible on the form by default. Customize the form to add this field.

<table id="table_e3z_nw2_ct"><thead><tr><th>

Field label and name

</th><th>

Probes that gather data

</th></tr></thead><tbody><tr><td>

Load Balancer \[load\_balancer\]

</td><td rowspan="2">

-   Apache - Get JK Module
-   Apache - Get Proxy Module
-   HAProxy - Get Configuration
-   Nginx - Get Configuration
-   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System

</td></tr><tr><td>

Name \[name\]

</td></tr><tr><td>

Tag \[tag\]

</td><td>

-   SNMP - F5 BIG-IP - System
-   SNMP - Netscaler - System

</td></tr></tbody>
</table>## Apache web server data

Discovery also collects data on Apache web serer load balancing modules using SSH. See [Apache mod\_jk and mod\_proxy discovery](r_DataCollDiscoApacheWebServers.md#) for more information on probes for Apache web server data. For information on the tables, fields, and data sources that discovery populates for Apache web servers, see [Apache web server discovery](r_DataCollDiscoApacheWebServers.md#).

**Parent Topic:**[Load balancer discovery](../concept/c_LoadBalancers.md)

