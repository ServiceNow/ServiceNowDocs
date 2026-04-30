---
title: Oracle Database and WebLogic Server licensing in hard-partitioned environments
description: The Software Asset Management application supports Oracle hard-partitioning licensing rules for IBM AIX Logical Partition \(LPAR\), Solaris Logical Domain \(LDOM\), and Solaris Zone.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Oracle licensing in partitioned environments, Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle Database and WebLogic Server licensing in hard-partitioned environments

The Software Asset Management application supports Oracle hard-partitioning licensing rules for IBM AIX Logical Partition \(LPAR\), Solaris Logical Domain \(LDOM\), and Solaris Zone.

When you hard partition a server, the server is divided into smaller systems that run independently from each other. Each system contains its own processors, network resources, operating system, memory, and more. For more information on Oracle licensing and hard partitioning, refer to [Oracle Partitioning Policy](https://www.oracle.com/assets/partitioning-070609.pdf).

## IBM LPAR

LPAR is a defined subset of processor hardware that supports the operating system. An LPAR contains resources, such as processors, memory, and input or output devices, that operate as an independent system. You can have multiple LPARs within each mainframe hardware system.

Discovering the LPARs and LPAR resources within your IBM LPAR infrastructure requires ServiceNow Discovery patterns for the IBM Hardware Management Console \(HMC\), which is the hardware appliance that enables you to manage and configure your LPARs. To access these discovery patterns, you must request and install the Discovery and Service Mapping Patterns application from the ServiceNow Store. For more information on how to configure a discovery on your LPARs, see [IBM Virtualization and Hardware Management Console discovery](https://www.servicenow.com/docs/access?context=ibm-hmc-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

**Note:** The `lparstat` command pulls a report of LPAR-related information and usage. For more information, see the [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/).

When you run a discovery, your discovered LPAR data is populated and stored in the following Configuration Management Database \(CMDB\) tables on your ServiceNow instance:

-   cmdb\_ci\_ibm\_frame
-   cmdb\_ci\_aix\_server
-   cmdb\_ci\_lpar\_instance
-   cmdb\_ci\_lpar\_resource
-   cmdb\_rel\_ci
-   cmdb\_sam\_sw\_install

To populate and store this data, you must request and install the CMDB CI Class Models application from the ServiceNow Store. This application adds or updates CMDB classes for the IBM HMC. For more information on IBM HMC CMDB classes, see [IBM Hardware Management Console \(HMC\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-ibm-hmc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

After your discovered LPAR data is populated in the appropriate CMDB tables, you can use the **samp\_frame\_to\_lpar\_resource** database view to join the tables together and consolidate all LPAR data into a single view. Based on this database view and the Oracle Database and WebLogic Server licensing rules for IBM LPAR, you can identify and determine the license compliance of all Oracle Database and WebLogic server installations across your IBM LPAR infrastructure.

<table id="table_asg_dzj_rrb"><thead><tr><th>

Processor pool

</th><th>

Description

</th><th>

Licensing rule

</th></tr></thead><tbody><tr><td>

Dedicated

</td><td>

Processors are assigned to only one dedicated LPAR, which is an LPAR that is built on dedicated CPU resources.

</td><td>

You must license the dedicated processors on which you install or run an Oracle database or WebLogic server.To determine the number of rights that are required for a dedicated LPAR, multiply the total number of processor cores that are running an Oracle Database or WebLogic server on the LPAR by a core processor licensing factor, as specified on the [Oracle Processor Core Factor Table](http://www.oracle.com/us/corporate/contracts/processor-core-factor-table-070634.pdf).

</td></tr><tr><td>

Shared

</td><td>

Processors are shared across micro-partitions, which are LPARs that are built on shared CPU resources.

</td><td>

You must license the shared processors on which you install or run an Oracle Database or WebLogic server.You can determine the number of rights that are required across your micro-partitions based on the LPAR type:

-   **Capped LPAR**: A capped LPAR is a logical partition that is assigned a maximum entitled capacity, which is the number of CPU resources that the LPAR is entitled to receive. Capped LPARs can’t use more processor power than the assigned entitled capacity.

To determine the number of rights that are required across your capped micro-partitions, multiply the sum of all assigned entitled capacities by a core processor licensing factor, as specified on the [Oracle Processor Core Factor Table](http://www.oracle.com/us/corporate/contracts/processor-core-factor-table-070634.pdf).

-   **Uncapped LPAR**: An uncapped LPAR is a logical partition that can use more processor power than the assigned entitled capacity. Processor power usage is limited by the number of virtual processors that are assigned to the LPAR or by the maximum number of physical processor cores that are available to the shared processor pool.

To determine the number of rights that are required across your uncapped micro-partitions, add the sum of all assigned virtual processors with the sum of all assigned entitled capacities.

    -   If the resulting value is lower than the number of physical processor cores that are available to the shared processor pool, multiply the value by a core processor licensing factor, as specified on the [Oracle Processor Core Factor Table](http://www.oracle.com/us/corporate/contracts/processor-core-factor-table-070634.pdf).
    -   If the resulting value is greater than the number of physical processor cores that are available to the shared processor pool, multiply the number of physical processor cores by a core processor licensing factor, as specified on the [Oracle Processor Core Factor Table](http://www.oracle.com/us/corporate/contracts/processor-core-factor-table-070634.pdf).

</td></tr></tbody>
</table>For more information on database views, see [Working with database views for reporting](https://www.servicenow.com/docs/access?context=c_DatabaseViews&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Solaris LDOM or Oracle VM Server for SPARC

A logical domain \(LDOM\) is a distinct logical unit within a single computer system, complete with its own operating system, resources, and identity. You can run different applications in separate logical domains and maintain their independence for performance and security reasons. Solaris LDOM is a virtualization technology that enables creating multiple virtual machines \(VMs\) on a single physical server.

The ServiceNow Discovery application uses the Solaris LDOM infrastructure pattern and Solaris LDOM shared library pattern to find all LDOM data. For information on Solaris LDOM discovery, see [Oracle Solaris LDOM discovery](https://www.servicenow.com/docs/access?context=solaris-ldom-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

The Software Asset Management application supports licensing of Oracle Database Server and WebLogic Server installed on the Solaris LDOM, version 2.0 and above, for Per Processor and Named User Plus \(NUP\) license metrics. To license your Oracle Database or WebLogic server installations, rights should be allocated to the physical server that runs the Solaris LDOM configuration. For details on the licensing of Oracle products, see [Software model metric attributes](../reference/sw-metric-attributes.md).

## Solaris zones

You can set up a global zone on a Solaris server and hard partition it with multiple local zones. You can then run an Oracle Database or WebLogic server on one or more local zones. To license your Oracle Database or WebLogic server installations, rights should be allocated to the physical host that runs the entire Solaris zone configuration. For the Per Processor license metric, rights must cover the cores for all local zones up to the maximum capacity of the physical host. For the NUP license metric, rights must cover the clients that access the Database or WebLogic server on the local zones. For information on Solaris zone discovery, see [Solaris discovery](https://www.servicenow.com/docs/access?context=r_DataCollDiscoSolarisComputers&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

**Parent Topic:**[Oracle Database and WebLogic Server licensing in partitioned environments](oracle-licensing-partitioned-environments.md)

