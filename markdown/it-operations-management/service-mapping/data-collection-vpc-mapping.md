---
title: Data collection and discovery using VPC Flow Logs
description: Service Mapping can perform discovery based on data collected using VPC Flow Logs. Amazon VPC hosts Amazon Elastic Compute Cloud \(EC2\) instances that provide Amazon Web Services. VPC Flow Logs collect data on IP traffic going to and from network interfaces in the VPC.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Data collection and discovery using VPC Flow Logs

Service Mapping can perform discovery based on data collected using VPC Flow Logs. Amazon VPC hosts Amazon Elastic Compute Cloud \(EC2\) instances that provide Amazon Web Services. VPC Flow Logs collect data on IP traffic going to and from network interfaces in the VPC.

In base systems, which are the default or standard configurations, traffic-based discovery relies solely on TCP-related data collected using the **netstat**, **ss**, and **lsof** commands. Discovery based on Netflow and VPC logs requires additional configuration. You can enrich your traffic-based discovery by configuring Service Mapping to use VPC Flow Logs.

Service Mapping discovery based on VPC Flow logs has the following flow:

1.  Amazon EC2 instances collect their individual logs into log streams and forward them to the central flow log group.

    ![Amazon EC2 instances collect their individual logs](../image/VPCFlowSetup1.png "Amazon EC2 instances collect their individual logs")

2.  The ServiceNow connector triggers MID Server to collect the data from the flow log and processes it.
3.  The MID Server places the processed information onto the ECC queue.

    ![MID Server collects the data from the flow log and places it onto the ECC queue.](../image/VPCFlowSetup2.png "MID Server collects the data from the flow log and places it onto the ECC queue")

4.  A sensor retrieves the processes data from the ECC queue and writes it into the Flow Connection \[sa\_flow\_connection\] table.
5.  Whenever Service Mapping checks the ECC queue and receives information on a discovered CI, it checks these tables for any data on outbound connections related to the CI: the cmdb\_tcp and sa\_flow\_connection tables. If these two tables contain unique data that patterns did not discover, Service Mapping enriches the information about the CI connections and adds them to the map.

    ![The collected data is written into the sa_flow_connection table from which Service Mapping collects the data.](../image/VPCFlowSetup3.png "Collected data is written into the sa_flow_connection table from which Service Mapping collects the data")


In deployments with multiple flow log groups, configure a dedicated connector that works with one MID Server for every flow log group. Multiple flow log groups my use the same AWS credentials.

**Related topics**  


[https://support.servicenow.com/kb\_view.do?sysparm\_article=KB0597467](https://support.servicenow.com/kb_view.do?sysparm_article=KB0597467)

[Traffic-based discovery in Service Mapping](traffic-based-discovery.md)

