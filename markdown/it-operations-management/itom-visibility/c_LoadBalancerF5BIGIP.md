---
title: F5 BIG-IP load balancer discovery
description: Discovery and Service Mapping can find F5 BIG-IP load balancers via SNMP, SSH, and through the REST API.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# F5 BIG-IP load balancer discovery

Discovery and Service Mapping can find F5 BIG-IP load balancers via SNMP, SSH, and through the REST API.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

**Important:** Discovery treats load balancers as licensable entities and attempts to discover them primarily using SNMP. If a load balancer in your system, running on a Linux host, has SNMP and SSH ports open, Discovery might classify it based on the SSH port. This classification has priority over SNMP. To ensure that Discovery properly classifies your hardware load balancers, create a Discovery behavior for load balancers that includes SNMP but not SSH. Software load balancers are treated as applications.

You can download VMware images of BIG-IP with a free 90-day trial from [https://www.f5.com/trial](https://www.f5.com/trial).

For F5 Global Traffic Manager \(GTM\) BIG-IP load balancers, Discovery can resolve the DNS name of the F5 GTM hardware as well as the DNS names of all the servers associated with the load balancer that receive distributed traffic. To view this data, navigate to **All** &gt; **Configuration** &gt; **Load Balancers** &gt; **LB Hardware** and open the F5 load balancer record and then select the **DNS Names for CIs** related list. [Service Mapping](../../service-mapping/reference/c_ServiceMappingOverview.md) uses this information to map F5 relationships.

**Note:** If your F5 BIG-IP device is part of a failover cluster, it can be associated with two cluster nodes. In this case, one of the nodes appears as Operational in the **Operational Status** field, and the other appears as Non-Operational.

## Prerequisites

-   To successfully discover the load balancer pool members, set the **display service names** option \(**bigpipe.displayservicenames**\) of the load balancer to **false** on the F5 load balancer.
-   For F5 Load Balancer pattern:
    -   Configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) on the ServiceNow AI Platform.
    -   \(Optional\) If there are iRules or SNMP community credentials are not enough for discovering outgoing connections, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

        **Note:** If you do not want to use SSH credentials, you can use the REST API to create a connection to F5 BIG-IP devices.

        Service Mapping uses the SSH credentials to retrieve connections that are not from CMDB. Discovering connections using the SSH protocol is a failover mechanism for the SNMP-based discovery.

-   For F5 Load Balancer SSH pattern:
    -   Configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
    -   Verify permissions for the following SSH commands:
        -   `list auth partition all`
        -   `list sys global-settings`
        -   `show sys hardware`
        -   `list sys db failover.state`
        -   `list net self one-line`
        -   `show sys mac-address | grep interface`
        -   `show net interface field-fmt`
        -   `show net self | grep -e 'Mac Address' 'IP:'`
        -   `list ltm pool | grep -e 'pool' 'mode'`
        -   `list ltm pool /<partition_name>/* | grep -e 'pool' 'mode'`
        -   `show ltm pool | grep -e 'Ltm::' 'Total Connections'`
        -   `show ltm pool /<partition_name>/* |grep -e 'Ltm::' 'Total Connections'`
        -   `list sys db bigpipe.displayservicenames | grep value`
        -   `show /net vlan | grep -e 'Interface Name' 'Mac' 'Tag'`
        -   `show ltm virtual detail | grep -e 'Server:' 'State' 'Pool:' 'Destination' 'Total Connections'`
        -   `show ltm virtual detail /<partition_name>/* | grep -e 'Server:' 'State' 'Pool:' 'Destination' 'Total Connections'`
        -   `show gtm wideip | grep -e 'WideIp' 'State'`
        -   `list wideip a /<partition_name>/* | grep -e 'WideIp' 'State'`
        -   `show gtm wideip all | grep -e 'WideIp' 'State'`
        -   `list gtm wideip`
        -   `list gtm wideip all`
-   For F5REST pattern:
    -   For horizontal discovery using Discovery, provide read-only permissions to run the following APIs:

        -   `"https://" + $ipAddress + "/mgmt/tm/ltm/pool"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/global-settings"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/hardware"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/failover"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/self"`
        -   `"https://" + $ipAddress + "/mgmt/tm/ltm/virtual?$select=destination,mask,vlans"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/interface"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/interface/stats"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/trunk"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/vlan"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/vlan/"+<vlan id>+"/interfaces"`
        -   `"https://" + $ipAddress + "/mgmt/tm/gtm/wideip"`
        -   `"https://" + $ipAddress + "/mgmt/tm/cm/traffic-group/"`
        -   `"https://" + $ipAddress + "/mgmt/tm/cm/device"`
    -   Create [basic authentication](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) credentials.
-   For F5 REST OAuth 2.0 authentication pattern:
    -   Verify read-only permission for the following APIs:
        -   `"https://" + $ipAddress + "/mgmt/shared/authn/login"`
        -   `"https://" + $ipAddress + "/mgmt/tm/ltm/pool"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/global-settings"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/hardware"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/failover"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/self"`
        -   `"https://" + $ipAddress + "/mgmt/tm/ltm/virtual?$select=destination,mask,vlans"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/interface"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/interface/stats"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/trunk"`
        -   `"https://" + $ip_address + "/mgmt/tm/net/vlan"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/vlan/"+<vlan id>+"/interfaces"`
        -   `"https://" + $ipAddress + "/mgmt/tm/gtm/wideip"`
        -   `"https://" + $ipAddress + "/mgmt/tm/cm/traffic-group/"`
        -   `"https://" + $ipAddress + "/mgmt/tm/cm/device"`
    -   Create [basic authentication](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) credentials.
    -   Create [a credential alias](https://www.servicenow.com/docs/access?context=discovery-credential-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for the basic authentication credential.
    -   Create a [serverless discovery schedule](../../service-mapping/task/create-serverless-sched-f5-rest-oauth.md).
-   For top-down discovery using Service Mapping, provide permissions to run the following APIs:

    -   `https://" get_attr {"managementIP"}"/mgmt/tm/ltm/"get_attr {"irule"}`
    -   `https://" get_attr {"managementIP"}"/mgmt/tm/ltm/virtual/~Common~"get_attr {"vip_name"}`
    -   `https://" get_attr {"computer_system.managementIP"}"/mgmt/tm/ltm/pool/"get_attr {"pool_name"}"/members?`
-   \(Optional\) For top-down discovery with Service Mapping, configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   \(Optional\) For top-down discovery with Service Mapping, provide a user with permissions to run the following commands:
    -   bigpipe commands \(for BIG-IP LTM F5 or BIG-IP GTM F5 version 9\)
    -   bigpipe and Traffic Management Shell \(TMSH\) commands \(for BIG-IP LTM F5 or BIG-IP GTM F5 version 10\)
    -   Traffic Management Shell \(TMSH\) commands \(for BIG-IP LTM F5 or BIG-IP GTM F5 version 11\)
    -   Traffic Management Shell \(TMSH\) advanced commands \(for BIG-IP LTM F5 or BIG-IP GTM F5 version 10, 11, and 12\)
    -   The **show cm traffic-group – get command** for discovering F5 BIG-IP Device Service Clustering
-   \(Optional\) For top-down discovery with Service Mapping, give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md).

## F5 cluster discovery

The horizontal discovery process can find F5 clusters. To discover clusters, the credentials must have read permission to traffic groups. For SNMP, this is the regular read permission. For SSH, you need to have **Traffic Management Shell \(TMSH shell\)** enabled and accessible.

**Note:** Because F5 clusters share the same virtual IPs and addresses for all devices, the horizontal discovery process cannot find specific IP addresses for each device.

## Classifier, patterns, and probes

Discovery uses these classifiers, probes, and pattern for F5 discovery:

<table id="table_fzd_2yv_jz"><thead><tr><th>

Classifiers

</th><th>

Trigger probes

</th><th>

Patterns

</th></tr></thead><tbody><tr><td>

F5 BIG-IP Load Balancer

</td><td>

Horizontal discovery probe: launches patterns

</td><td>

These patterns are used for standard horizontal discovery including identifying clusters:

-   F5 Load Balancer
-   F5 Load Balancer SSH
-   F5REST
-   F5 REST OAuth 2.0 authentication

 **Note:** The F5 Load Balancer and F5 Load Balancer SSH patterns include the extension section that discovers [F5 certificates.](../../service-mapping/reference/f5-certificate-discovery.md)

</td></tr><tr><td>

F5 HTTP

</td><td>

The F5 HTTP classifier does not use a trigger probe. It triggers the F5 Load Balancer REST pattern to perform data collection via REST.

</td><td>

These patterns use iRules to get information via REST. Service Mapping uses these patterns for top-down discovery:

-   F5 Load Balancer REST
-   F5 BigIP GTM
-   F5 BigIP LTM

</td></tr></tbody>
</table>To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Connections discovered by Service Mapping during the top-down discovery

Service Mapping performs the top-down discovery of the GTM BIG-IP load balancer in the context of application services. It discovers configured URLs of the GTM BIG-IP load balancers.

## Data collected by Discovery during horizontal discovery

The following data is collected on the F5 Big-IP `[cmdb_ci_lb_bigip]` table.

|Table and field|Description|
|---------------|-----------|
|F5 Big-IP \[cmdb\_ci\_lb\_bigip\]|
|Name \[name\]|Details about the load balancer. View a record in this table to see the upstream and downstream relationships with the load balancer.|
|Serial Number \[serial\_number\]|
|Operational Status \[operational\_status\]|
|Load Balancer Interface \[cmdb\_ci\_lb\_interface\]|
|Name \[name\]|Details about each interface for the load balancer.|
|MAC Address \[mac\_address\]|
|Operational Status \[operational\_status\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|
|Name \[name\]|The name of the pool and the method of load balancing it enables.|
|Load balancing method \[load\_balancing\_method\]|
|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|
|Name \[name\]|The name, IP address, and service port that each pool member uses.|
|IP Address \[ip\_address\]|
|Service Port \[service\_port\]|
|Pool \[pool\]|
|Load Balancer VLAN \[cmdb\_ci\_lb\_vlan\]|
|Name \[name\]|The name of the VLAN and the tag that is associated with this VLAN to identify it.|
|Tag \[tag\]|
|MAC Address \[mac\_address\]|
|Load Balancer Services \[cmdb\_ci\_lb\_service\]|
|Name \[name\]|Details about the load balancer service that distributes the workload to other servers, such as web servers.|
|IP Address \[ip\_address\]|
|Port \[port\]|
|Operational Status \[operational\_status\]|
|Hit count \[hit\_count\]|
|DNS \[cmdb\_ci\_dns\_name\]|
|Name \[name\]|The name and IP address of the Domain Name Server for the network adapters.|
|IP Address \[ip\_address\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Name \[name\]|Details about the network adapters on the load balancer.|
|IP Address \[ip\_address\]|
|Netmask \[netmask\]|
|Mac address \[mac\_address\]|
|Cluster \[cmdb\_ci\_cluster\]|
|Name \[name\]|Details about the load balancer cluster.|
|Cluster status \[cluster\_status\]|
|Cluster ID \[cluster\_id\]|
|IP address \[ip\_address\]|
|Cluster Node \[cmdb\_ci\_cluster\_node\]|
|Name \[name\]|Details about each node in a cluster.|
|Cluster ID \[cluster\_id\]|
|Cluster status \[cluster\_status\]|

## Configuration item \(CI\) relationships for clusters

These relationships are created for clusters:

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_cluster|Hosts::Hosted on|cmdb\_ci\_lb\_bigip|
|cmdb\_ci\_cluster\_node|Hosted on::Hosts|cmdb\_ci\_lb\_bigip|
|cmdb\_ci\_cluster\_node|Cluster of::Cluster|cmdb\_ci\_cluster|

**Parent Topic:**[Load balancer discovery](c_LoadBalancers.md)

