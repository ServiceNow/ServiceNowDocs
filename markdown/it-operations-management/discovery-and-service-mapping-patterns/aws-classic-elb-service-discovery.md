---
title: AWS classic ELB Service discovery with Patterns
description: Discovery uses the Amazon AWS classic ELB Service discovery pattern to find all load balancers that use HTTP and HTTPS traffic.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS classic ELB Service discovery with Patterns

Discovery uses the Amazon AWS classic ELB Service discovery pattern to find all load balancers that use HTTP and HTTPS traffic.

Elastic Load Balancing \(ELB\) automatically distributes incoming application traffic across multiple targets.

The Amazon AWS classic ELB Service discovery pattern supports top-down discovery. The two possible entry points for top-down discovery are the HTTP\(s\) Endpoint and TCP Endpoint. Outgoing relations are to Amazon EC2 instances.

The ServiceNow AI Platform supports Amazon Commercial Cloud Services \(C2S\) for discovery and cloud governance. C2S is the government program that brings AWS into the Intelligence Community.

You can use this pattern on the ServiceNow platform using Jakarta or later releases.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Run a horizontal discovery, using [Cloud API \(CAPI\)](../../cloud-management-v2/concept/cloud-management-api.md). This is necessary because this discovery pattern supports top-down discovery only. For cloud discovery, you can run the horizontal discovery as usual.
-   When the load balancers data has been stored in the Configuration Management Database \(CMDB\), create an application service for each load balancer.
-   Set read-only permissions for these REST APIs:
    -   https://elasticloadbalancing.&lt;REGION&gt;.amazonaws.com/?Action=DescribeLoadBalancers&amp;Version=2012-06-01&amp;LoadBalancerNames.member.1=&lt;LB\_NAME&gt;
    -   https://ec2.&lt;REGION&gt;.amazonaws.com/?Action=DescribeInstances&amp;Version=2016-11-15&amp;Filter.1.Name=instance-state-name&amp;Filter.1.Value=running&amp;Filter.2.Name=instance-id&amp;Filter.2.Value=&lt;INSTANCE\_ID&gt; \(to create relation between LB and EC2 instance\)
-   For Cloud Discovery, download the Discovery and Service Mapping Patterns from the ServiceNow Store.
-   When installing the MID Server, ensure that the host machine meets or exceeds the [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) published on the ServiceNow documentation site.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

The discovered data includes the following tables and fields.

|Table and field|Description|
|---------------|-----------|
|Load Balancer Services \[cmdb\_ci\_lb\_service\]|
|Fully qualified domain name \[fqdn\]|Fully Qualified Domain Name \(FQDN\) of the load balancer. The DNS name.|
|Name \[name\]|Name of the load balancer, in the following format: &lt;LB name&gt;:&lt;LB port&gt;.|
|Back End Port \[back\_end\_port\]|Port of the instance.|
|Server Port \[server\_port\]|Port of the instance.|
|Port \[port\]|Port of the load balancer.|
|Front End Port \[front\_end\_port\]|Port of the load balancer.|
|Object ID \[object\_id\]|LB port.|
|IP Address \[ip\_address\]|IP address of the FQDN.|
|Server Protocol \[server\_protocol\]|Protocol of the instance.|
|IP Address \[cmdb\_ci\_ip\_address\]|
|IP Address \[ip\_address\]|IP address of the load balancer FQDN.|
|Name \[name\]|Name of the load balancer, in the following format: &lt;LB name&gt;:&lt;LB port&gt;.|
|Netmask \[netmask\]|0.0.0.0|

**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

