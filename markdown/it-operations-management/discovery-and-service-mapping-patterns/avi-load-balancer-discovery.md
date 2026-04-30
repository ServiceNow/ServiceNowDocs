---
title: Avi Vantage load balancer discovery
description: The ServiceNow Discovery and Service Mapping applications use the Avi load balancer discovery patterns to find Avi Vantage load balancer components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Avi Vantage load balancer discovery

The ServiceNow Discovery and Service Mapping applications use the Avi load balancer discovery patterns to find Avi Vantage load balancer components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses the Avi Load Balancer Controller pattern and the Avi Load Balancer Controller - Session-based pattern to run horizontal discovery. Both patterns use set of REST APIs to find the load balancers. They differ only in the type of authentication used when running the API queries.

For top-down discovery, Service Mapping uses the Avi Load Balancer VIP pattern.

The patterns support Avi infrastructure residing on AWS and VMware. They relate the discovered CIs to the infrastructure only when run on VMware . The patterns also support Global Server Load Balancing \(GSLB\).

You can use these patterns on the ServiceNow AI Platform® using the release Madrid patch 5, New York or later.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Ensure that your instance supports the Avi Load Balancer CI class models by deploying the latest version of the CMDB CI Class Models store app. Install the application from the ServiceNow Store.
-   For the Avi Load Balancer Controller pattern:
    -   In the Avi Controller, ensure that Basic Authentication is allowed.
    -   Configure the following credentials:
        1.  Navigate to **Discovery** &gt; **Credentials**
        2.  Click **New**.
        3.  Click **Basic Auth Credentials**, fill out the form, and then click **Submit**.

            |Field|Description|
            |-----|-----------|
            |Name|Credential name.|
            |Active|Option for enabling this credential for discovery. Select this check box to enable discovery.|
            |Applies to|Select **All MID servers**.|
            |Order|Order in which the platform tries this credential as it attempts to log on to devices. A smaller number indicates that the credential appears higher in the list. Establish the credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number, or none, the instance tries the credentials in a random order. The default value is 100.|
            |User name|Name of the user for performing Avi Load Balancer discovery.|
            |Password|Password for this user.|

        4.  [Run a Quick Discovery](../../discovery/task/t_DiscoverNow.md) on the IP address of the Avi Controller Cluster.
-   For the Avi Load Balancer Controller - Session-based pattern:
    -   Create a Basic Authentication credential with an alias:
        1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.
        2.  Click **New**.
        3.  Enter a unique name for the alias and select **Credential** for the alias type.
        4.  Click **Submit**.
        5.  Open the new alias.
        6.  On the Credentials tab, click **New**.
        7.  Select **Basic Auth Credentials** for the credential type and fill out the form.

            |Field|Description|
            |-----|-----------|
            |Name|Credential name.|
            |User name|Name of the user for performing Avi Load Balancer discovery.|
            |Password|Password for this user.|

        8.  Click **Update**.
    -   Create a [serverless discovery](../../discovery/concept/serverless-discovery.md) schedule.

        Then do the following:

        1.  In the scheduler, click the **Serverless Execution Patterns** tab.
        2.  Click **New**.
        3.  Fill out the form and then click **Submit**.

            |Field|Description|
            |-----|-----------|
            |Name|Provide a descriptive name.|
            |Pattern|Select the Avi Load Balancer Controller - Session-based pattern.|

        4.  Open the record created in the previous steps, and configure these parameters:

            |Parameter|Description|
            |---------|-----------|
            |IP address|The Avi IP address.|
            |Credential alias|The name of the credential alias created above.|

-   For the Avi Load Balancer Controller pattern and the Avi Load Balancer Controller - Session-based pattern, provide a user with permissions to send the following API queries.
    -   /api/cluster
    -   /api/serviceengine
    -   /api/pool
    -   /api/vimgrvmruntime?controller\_vm=true
    -   /api/cloud
    -   /api/virtualservice
    -   /api/serviceenginegroup
    -   /api/gslbservice
    -   /api/tenant
-   For the Avi Load Balancer VIP pattern:
    -   [Create an service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
    -   Before using the Avi Load Balancer VIP pattern, use one of the horizontal Avi load balancer discovery patterns to find the Avi infrastructure.

## Data collected by Discovery during horizontal discovery

The discovered data includes the following tables and fields.

<table id="table_mqj_dh3_vjb"><thead><tr><th>

Table and field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Avi Controller \[cmdb\_ci\_avi\_controller\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the Avi Controller.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

Hostname of the Virtual Machine \(VM\).

</td></tr><tr><td>

IP address \[ip\_address\]

</td><td>

IP address of the FQDN.

</td></tr><tr><td colspan="2">

Avi Service Engine \[cmdb\_ci\_avi\_service\_engine\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the Avi Service Engine.

</td></tr><tr><td>

IP address \[ip\_address\]

</td><td>

IP address of the Avi Service Engine.

</td></tr><tr><td>

Version \[version\]

</td><td>

Version of the Avi Service Engine.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier of the Avi Service Engine.

</td></tr><tr><td colspan="2">

Avi Controller Cluster \[cmdb\_ci\_avi\_controller\_cluster\]

</td></tr><tr><td>

Cluster ID \[cluster\_id\]

</td><td>

Unique identifier of the Avi Controller Cluster.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the Avi Controller Cluster.

</td></tr><tr><td>

IP address \[ip\_address\]

</td><td>

IP address of the Avi Controller Cluster host.

</td></tr><tr><td colspan="2">

Load Balancer Pool \[cmdb\_ci\_lb\_pool\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the Load Balancer Pool.

</td></tr><tr><td>

Server ID \[server\_id\]

</td><td>

Unique identifier of the Load Balancer Pool.

</td></tr><tr><td>

Load Balancing Method \[load\_balancing\_method\]

</td><td>

Method that Avi Vantage uses to make its load balancing decision. The pattern translates the algorithms as follows:-   "LB\_ALGORITHM\_LEAST\_CONNECTIONS": "least-connections"
-   "LB\_ALGORITHM\_ROUND\_ROBIN": "round-robin"
-   "LB\_ALGORITHM\_FASTEST\_RESPONSE": "fastest-response"
-   "LB\_ALGORITHM\_CONSISTENT\_HASH": "consistent-hash"
-   "LB\_ALGORITHM\_LEAST\_LOAD": "least-load"
-   "LB\_ALGORITHM\_FEWEST\_SERVERS": "fewest-servers"
-   "LB\_ALGORITHM\_RANDOM": "random"
-   "LB\_ALGORITHM\_FEWEST\_TASKS": "fewest-tasks"
-   "LB\_ALGORITHM\_NEAREST\_SERVER": "nearest-server"

</td></tr><tr><td colspan="2">

Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the Pool Member @ name of the Pool.

</td></tr><tr><td>

IP address \[ip\_address\]

</td><td>

IP address of the Pool Member host.

</td></tr><tr><td colspan="2">

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the Virtual IP \(VIP\).

</td></tr><tr><td>

IP address \[ip\_address\]

</td><td>

IP address of the VIP.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier of the VIP.

</td></tr><tr><td>

Port \[port\]

</td><td>

Port of the host VM.

</td></tr><tr><td colspan="2">

Avi Tenant \[cmdb\_ci\_avi\_tenant\]

</td></tr><tr><td>

name

</td><td>

Name of the Tenant​.

</td></tr><tr><td>

object\_id

</td><td>

The object\_id of the Tenant​.

</td></tr><tr><td>

tenant\_url

</td><td>

URL to the Tenant​.

</td></tr></tbody>
</table>The Dependency Views map shows discovered load balancer CIs and the relationships between them.

![CIs and connections on a Dependency Views map.](../image/avi-lb-dependency-views-map1.png)

The following image shows the results of top-down discovery using the Avi Load Balancer VIP pattern.

![This image shows top-down discovery using the Avi Load Balancer VIP pattern.](../image/avi-lb-top-down-discovery.png "Top-down discovery using the Avi Load Balancer VIP pattern")

## CI relationships

These relationships are created to support Avi Load Balancer discovery:

|CI|Relationship|CI|
|---|------------|---|
|Avi Controller Cluster \[cmdb\_ci\_avi\_controller\_cluster\]|Cluster of::Cluster|Avi Controller \[cmdb\_ci\_avi\_controller\]|
|Avi Tenant \[cmdb\_ci\_avi\_tenant​\]|Hosted on::Hosts|Avi Controller Cluster \[cmdb\_ci\_avi\_controller\_cluster\]|
|Contains::Contained by|Load Balancer Service \[cmdb\_ci\_lb\_service\]|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Used by::Uses|Load Balancer Service \[cmdb\_ci\_lb\_service\]|
|Hosted on::Hosts|Avi Controller Cluster \[cmdb\_ci\_avi\_controller\_cluster\]|
|Owns::Owned by|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|
|Avi Service Engine \[cmdb\_ci\_avi\_service\_engine\]|Hosted on::Hosts|Avi Controller Cluster \[cmdb\_ci\_avi\_controller\_cluster\]|
|Avi Controller \[cmdb\_ci\_avi\_controller\]|Contains::Contained by|Avi Service Engine \[cmdb\_ci\_avi\_service\_engine\]|
|Load Balancer Service \[cmdb\_ci\_lb\_service\]|Used by::Uses|Avi Service Engine \[cmdb\_ci\_avi\_service\_engine\]|
|Runs on::Runs|Avi Controller Cluster \[cmdb\_ci\_avi\_controller\_cluster\]|
|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|Reference only|Avi Controller Cluster \[cmdb\_ci\_avi\_controller\_cluster\]|

## Troubleshooting

If Avi load balancer top-down discovery fails, see KB article [KB0824019](https://support.servicenow.com/kb_view.do?sysparm_article=KB0824019) for a workaround.

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
</table>**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

