---
title: IBM licensing in IBM LPAR infrastructures
description: When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, the Software Asset Management application supports IBM licensing rules for IBM logical partitions.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Virtualization technologies and cloud platforms supported by ASP integrations, Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# IBM licensing in IBM LPAR infrastructures

When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, the Software Asset Management application supports IBM licensing rules for IBM logical partitions.

A logical partition \(LPAR\) is a defined subset of processor hardware that supports the operating system. An LPAR contains resources, such as processors, memory, and input or output devices, that operate as an independent system. You can have multiple LPARs within each mainframe hardware system.

Discovering the LPARs and LPAR resources within your IBM LPAR infrastructure requires ServiceNow Discovery patterns for the IBM Hardware Management Console \(HMC\), which is the hardware appliance that enables you to manage and configure your LPARs. To access these discovery patterns, you must request and install the Discovery and Service Mapping Patterns application from the ServiceNow Store. For more information on how to configure a discovery on your LPARs, see [IBM Virtualization and Hardware Management Console discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/ibm-hmc-discovery.md).

**Note:** The `lparstat` command pulls a report of LPAR-related information and usage. For more information, see the [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/).

When you run a discovery, your discovered LPAR data is populated and stored in the following Configuration Management Database \(CMDB\) tables on your ServiceNow instance:

-   cmdb\_ci\_ibm\_frame
-   cmdb\_ci\_aix\_server
-   cmdb\_ci\_lpar\_instance
-   cmdb\_ci\_lpar\_resource
-   cmdb\_rel\_ci
-   cmdb\_sam\_sw\_install

To populate and store this data, you must request and install the CMDB CI Class Models application from the ServiceNow Store. This application adds or updates CMDB classes for the IBM HMC. For more information on IBM HMC CMDB classes, see [IBM Hardware Management Console \(HMC\) extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-ibm-hmc.md).

The Software Asset Management application supports both full capacity and sub-capacity processor value unit \(PVU\), resource value unit \(RVU\), and virtual processor core \(VPC\) licensing for IBM software products in IBM LPAR infrastructures.

## IBM licensing rules in IBM LPAR infrastructures

-   **Full capacity licensing**

    When you use full capacity licensing, you must license each processor core on the underlying hardware system that is running the LPARs on which you have installed and run an IBM software product.

    Using the total number of processor cores on the underlying hardware system, you can determine the number of rights that are required for your license based on the license type. To determine the number of rights that are required for a PVU or RVU license, see [IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses](ibm-pvu-rvu-licensing.md). To determine the number of rights that are required for a VPC license, see [IBM virtual processor core \(VPC\) licenses](ibm-virtual-processor-core-licensing.md).

-   **Sub-capacity licensing**

    When you use sub-capacity licensing, you must license only the processor cores that are assigned to the LPARs on which you install and run an IBM software product.

    You can determine the number of rights that are required for a sub-capacity license based on the type of processor pool and license that you are using for your IBM software product.

    IBM LPARs support both dedicated and shared processor pools. If you are using a dedicated processor pool, in which processor cores are assigned to only one dedicated LPAR, you must license each dedicated processor core that is assigned to the LPAR on which you install or run an IBM software product. If you are using a shared processor pool, in which processor cores are shared across micro-partitions, you must license the processor cores that are shared across the micro-partitions on which you install or run an IBM software product. You can determine the number of processor cores that must be licensed across your micro-partitions based on the LPAR type:

    -   **Capped LPAR**: A capped LPAR is a logical partition that is assigned a maximum entitled capacity, which is the number of CPU resources that the LPAR is entitled to receive. Capped LPARs cannot use more processor power than the assigned entitled capacity.
    -   **Uncapped LPAR**: An uncapped LPAR is a logical partition that can use more processor power than the assigned entitled capacity. Processor power usage is limited by the number of virtual processor cores that are assigned to the LPAR or by the maximum number of processor cores that are available to the shared processor pool.
    For more details, see [Sub-capacity \(Virtualization\) License Counting Rules](https://public.dhe.ibm.com/software/passportadvantage/SubCapacity/Scenarios_Power_Systems.pdf).

    Using the sum of processor cores that must be licensed across your processor pools, you can determine the number of rights that are required for your license based on the license type. To determine the number of rights that are required for a PVU or RVU license, see [IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses](ibm-pvu-rvu-licensing.md). To determine the number of rights that are required for a VPC license, see [IBM virtual processor core \(VPC\) licenses](ibm-virtual-processor-core-licensing.md).


**Parent Topic:**[Virtualization technologies and public cloud platforms supported by IBM Authorized SAM Provider \(ASP\) integrations](supported-virtualization-technologies-iasp-integrations.md)

