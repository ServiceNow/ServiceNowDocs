---
title: Load balancer discovery
description: Discovery can collect data about network routers, switches, and applications.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Load balancer discovery

Discovery can collect data about network routers, switches, and applications.

Discovery supports data collection from the following applications and hardware:

-   A10
-   Apache mod\_jk and Apache mod\_proxy
-   Big-IP F5 Traffic Manager
-   Cisco
-   Citrix NetScaler
-   HAProxy
-   NGINX
-   Alteon
-   ACE
-   Radware

**Important:** Discovery treats load balancers as licensable entities and attempts to discover them primarily using SNMP. If a load balancer in your system, running on a Linux host, has SNMP and SSH ports open, Discovery might classify it based on the SSH port. This classification has priority over SNMP. To ensure that Discovery properly classifies your hardware load balancers, create a Discovery behavior for load balancers that includes SNMP but not SSH. Software load balancers are treated as applications.

## Load balancer patterns

Starting with the Jakarta release, Discovery uses out-of-box patterns to find some types load balancers for new instances \(see table\).

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

<table id="table_gbc_kdq_fx"><thead><tr><th>

Load balancer

</th><th>

Pattern names and description

</th><th>

Main CI table populated

</th></tr></thead><tbody><tr><td>

[A10](../reference/r_DataCollDiscoA10LoadBalancers.md)

</td><td>

A10 LoadBalancer

</td><td>

A10 Load Balancer \[cmdb\_ci\_lb\_a10\]

</td></tr><tr><td>

[ACE](ace-load-balancer-discovery.md)

</td><td>

ACE Load Balancer by SSH \(formerly ACE Load Balancer\)

</td><td>

ACE \[cmdb\_ci\_lb\_ace\]

</td></tr><tr><td>

[Alteon](alteon-load-balancer-discovery.md)

</td><td>

Alteon Load Balancer

</td><td>

Alteon \[cmdb\_ci\_lb\_alteon\]

</td></tr><tr><td>

[F5 BIG-IP](c_LoadBalancerF5BIGIP.md)

</td><td>

F5 - HD, F5 Load Balancer

</td><td>

F5 BIG-IPs \[cmdb\_ci\_lb\_bigip\]

</td></tr><tr><td>

[NetScaler](c_LoadBalancerCitrixNetscaler.md)

</td><td>

Netscaler Load Balancer

</td><td>

Citrix NetScalers \[cmdb\_ci\_lb\_netscaler\]

</td></tr><tr><td>

[Radware - AppDirector](radware-appdirector.md)

</td><td>

AppDirector Load Balancer

</td><td>

Radware Load Balancer \[cmdb\_ci\_lb\_radware\]

</td></tr><tr><td>

[HAProxy load balancer discovery with patterns](../../service-mapping/reference/haproxy-lb-discovery-pattern.md)

</td><td>

HA Proxy

</td><td>

HAProxy Load Balancer \[cmdb\_ci\_lb\_haproxy\]

</td></tr></tbody>
</table>To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Load balancer discovery, Service Mapping, and customized CI fields

Discovery collects information about the install status and operational status of load balancers. If you are using Discovery with Service Mapping, do not customize the \[operational\_status\] or \[install\_status\] fields. By default, Service Mapping ignores all host CIs for which the value of the **\[operational\_status\]** field is not **1** \(Operational\) or the value of the status **\[install\_status\]** field is **100** \(absent\). For additional information, see [Preparing customized ServiceNow deployments to work with Service Mapping](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3D334cd265db4a4fc0d7e37aa31f9619f7%26sysparm_referring_url%3Dkb_view.do) \[KB0647574\] in the HI Knowledge Base.

-   **[A10 load balancer discovery](../reference/r_DataCollDiscoA10LoadBalancers.md)**  
Discovery and Service Mapping uses patterns to collect information about A10 load balancers.
-   **[Cisco ACE load balancer discovery](ace-load-balancer-discovery.md)**  
Discovery identifies and classifies information about ACE load balancers.
-   **[Cisco GSS load balancer discovery](c_LoadBalancerGSS.md)**  
Discovery of Cisco GSS load balancers is performed by both SNMP and SSH.
-   **[Cisco CSS load balancer](c_LoadBalancerCSS.md)**  
Discovery of Cisco CSS load balancers is performed by SNMP.
-   **[Citrix NetScaler load balancer discovery](c_LoadBalancerCitrixNetscaler.md)**  
Discovery and Service Mapping find Citrix NetScaler load balancers including Server Load Balancing \(GSLB\).
-   **[F5 BIG-IP load balancer discovery](c_LoadBalancerF5BIGIP.md)**  
Discovery and Service Mapping can find F5 BIG-IP load balancers via SNMP, SSH, and through the REST API.
-   **[HAProxy load balancer discovery using probes](c_LoadBalancerHAProxy.md)**  
Discovery of HAProxy Community edition load balancers is performed by SSH.
-   **[NGINX load balancer discovery](c_LoadBalancerNGINX.md)**  
Discovery of NGINX load balancers is performed by SSH.
-   **[Radware Alteon load balancer discovery](alteon-load-balancer-discovery.md)**  
Discovery identifies and classifies information about Alteon load balancers.
-   **[Radware-appDirector load balancer discovery](radware-appdirector.md)**  
Discovery of Radware load balancers is performed by SNMP.
-   **[Load balancer fields and probes](../reference/r_LoadBalancerFields.md)**  
Discovery stores load balancer information in several tables.

**Parent Topic:**[Network device discovery](c_NetworkDevices.md)

