---
title: Configure a manual cluster
description: Provide redundancy capabilities of an entire cluster in case of failure of one or more CIs in that cluster. By viewing the relative impact of a cluster member on the cluster information, you can better understand the source of alerts and take remediation steps.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure CIs as manual cluster, Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure a manual cluster

Provide redundancy capabilities of an entire cluster in case of failure of one or more CIs in that cluster. By viewing the relative impact of a cluster member on the cluster information, you can better understand the source of alerts and take remediation steps.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

In a manual service that was not discovered automatically, you can manually group a specific CI or a generic CI class under a logical cluster. The relative impact of a cluster member on the cluster can be configured in the impact tree.

For more information, see [Alert impact calculation](../concept/c_EMImpactCalculation.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Manual Clusters**.

2.  Select **New**.

3.  In the **Select a Service containing this manual cluster** section, select an application service to contain the new manual cluster based on a specific CI or general CI class.

    The cluster number is automatically generated and appears in the **Number** field.

    1.  Select the Lookup using list icon \(![Lookup using list icon](../image/search-icon.png)\) in the **Service** field.

    2.  In the CMDB CI Service \[cmdb\_ci\_service\_discovered\] table, select a manually created service.

        To define a new application service, see [Manually create an application service in Event Management](create-an-application-service.md).

    3.  Preview the record by selecting the Preview this record icon \(![Preview this record icon](../image/info.png)\).

4.  In the **Select a Specific CI or generic CI class** section, in the **Defined As** field, select whether to define the manual cluster as a specific CI of a manual cluster or as a generic CI class of a manual cluster that will be applied to all CIs of this class.

    -   Specific CI - In the **Configuration item** field, select the Lookup using list icon \(![Lookup using list icon](../image/search-icon.png)\) and select the configuration item.
    -   Generic CI class – In the **Configuration item class** field, select the configuration item class.
5.  In the **Provide a Description** section, either provide a description in the **Description** field or leave it blank to contain an automatically generated description when you select **Save** or **Submit**.

    The **Description** field is automatically updated when you select **Save** or **Submit**. The automatically generated description consists of the configuration item name and the service name. For example: `CI <Alert Processing> in service <linuxApplService> (*** auto generated ***)`.

    To prevent an automatic update of the Description field and retain your changes, delete the \(\*\*\* auto generated \*\*\*\) suffix that appears as part of the description.

6.  Activate the cluster by selecting the **Activate** check box.

7.  Select **Submit**.


## Result

The manual cluster is saved in the EM Impact Manual Cluster \[em\_impact\_manual\_cluster\] table. The impact calculation is recalculated automatically.

**Parent Topic:**[Configuring CIs in a manual service as a manual cluster](../concept/manual-cluster-in-a-manual-service.md)

**Related topics**  


[Configuring CIs in a manual service as a manual cluster](../concept/manual-cluster-in-a-manual-service.md)

