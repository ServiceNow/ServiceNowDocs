---
title: Data collection and discovery using Netflow
description: Service Mapping can perform discovery based on data collected using the Netflow protocol. Netflow is a protocol that Service Mapping can use to collect data about CIs and their connections along with Netstat and lsof commands.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Data collection and discovery using Netflow

Service Mapping can perform discovery based on data collected using the Netflow protocol. Netflow is a protocol that Service Mapping can use to collect data about CIs and their connections along with Netstat and lsof commands.

Using the Netflow protocol for collecting data is one of the traffic-based discovery methods. Other methods deployed by Service Mapping are using netstat and lsof commands and the VPC Flow Logs. For more information, refer to [Traffic-based discovery in Service Mapping](traffic-based-discovery.md).

In base systems, which are the default or standard configurations, traffic-based discovery relies solely on TCP-related data collected using the **netstat**, **ss**, and **lsof** commands. Discovery based on Netflow and VPC logs requires additional configuration. You can enrich your traffic-based discovery by configuring Service Mapping to use the Netflow protocol.

The component, which receives data in the Netflow format is the Netflow Collector. Its location depends on whether you configure data collection for testing purposes or standard operation:

-   **For the test purposes**

    This setup results in half automated data collection flow, where Service Mapping imports data only if you manually copy it from the Netflow Collector. You place the Netflow Collector on a server inside your organization network. This must be a server different from the server hosting the MID Server. You configure and test this setup as described in [Configure onetime data import using Netflow for testing purposes](../task/test-netflow-service-mapping.md).

-   **For standard operation**

    This setup results in fully automated data collection flow, where all involved components send, collect and analyze data automatically. You place the Netflow Collector on the same server as the MID Server inside your organization network. For instructions, see [Configure data collection using Netflow](../task/configure-netflow-service-mapping.md).


Netflow-based discovery has the following flow:

1.  The Netflow daemon runs and receives data from switches communicating with servers in the organization. The Netflow Collector writes received data from the Netflow daemon.
2.  The server, hosting the Netflow collector, uses the Netflow nfdump utility to write the data into the nfdump output file. This file summarizes the raw data on all switches used for server communication.

    ![Standard Netflow configuration: collecting data and writing it into the nfdump output file](../image/NetflowStandardSetup1.png "Collecting data and writing it into the nfdump output file")

3.  In testing setups, where the Netflow Collector is located not on the same server as the MID Server, you may need to convert the nfdump into the gzip format. Then you must manually copy the raw data in the nfdump output file onto the MID Server.

    ![Standard Netflow configuration: copying the nfdump output file onto the MID Server](../image/NetflowTestSetup.png "Copying the nfdump output file onto the MID Server")

4.  The MID Server processes the raw data in the nfdump output file and places the processed information onto the ECC queue.

    ![Standard Netflow configuration: analyzing the raw data and placing it at the ECC Queue](../image/NetflowStandardSetup2.png "Analyzing the raw data and placing it at the ECC Queue")

5.  A sensor retrieves the processes data from the ECC queue and writes it into the Flow Connection \[sa\_flow\_connection\] table.
6.  Whenever Service Mapping checks the ECC queue and receives information on a discovered CI, it checks these tables for any data on outbound connections related to the CI: the cmdb\_tcp and sa\_flow\_connection tables. If these two tables contain unique data that patterns did not discover, Service Mapping enriches the information about the CI connections and adds them to the map.

    ![Standard configuration: Service Mapping retrieves data from the sa_flow_connection table](../image/NetflowStandardSetup3.png "Service Mapping retrieves data from the sa_flow_connection table")


**Parent Topic:**[Advanced Service Mapping configuration](c_ConfigureSM.md)

**Related topics**  


[https://support.servicenow.com/kb\_view.do?sysparm\_article=KB0597467](https://support.servicenow.com/kb_view.do?sysparm_article=KB0597467)

