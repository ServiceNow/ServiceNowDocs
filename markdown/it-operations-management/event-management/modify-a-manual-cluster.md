---
title: Modify a manual cluster
description: Modify an existing manual cluster by changing the service, the specific CI, the generic CI class, or the description in case of an incorrect initial configuration, changes in the network, or other issues.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring CIs in a manual service as a manual cluster, Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Modify a manual cluster

Modify an existing manual cluster by changing the service, the specific CI, the generic CI class, or the description in case of an incorrect initial configuration, changes in the network, or other issues.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Manual Clusters**.

2.  From the list, select a manual cluster.

3.  Change the service containing the manual cluster by selecting a different one in the **Select a Service containing this manual cluster** section.

    The cluster number appears in the **Number** field.

    1.  Select the Lookup using list icon \(![Lookup using list icon](../image/search-icon.png)\) in the **Service** field.

    2.  In the CMDB CI Service \[cmdb\_ci\_service\_discovered\] table, select a manually created service.

    3.  Preview the record by selecting the Preview this record icon \(![Preview this record icon](../image/info.png)\).

4.  In the **Select a Specific CI or generic CI class** section in the **Defined As** field, modify the manual cluster either as a specific CI of a manual cluster or as a generic CI class of a manual cluster that will be applied to all CIs of this class.

    -   Specific CI - In the **Configuration item** field, select the Lookup using list icon \(![Lookup using list icon](../image/search-icon.png)\) and select the configuration item.
    -   Generic CI class – In the **Configuration item class** field, select the configuration item class.
5.  In the **Provide a Description** section, modify the description in the **Description** field.

    The **Description** field is automatically updated when you select **Save** or **Submit**. The automatically generated description consists of the configuration item name and the service name. For example: `CI <Alert Processing> in service <linuxApplService> (*** auto generated ***)`.

    To prevent an automatic update of the Description field and retain your changes, delete the \(\*\*\* auto generated \*\*\*\) suffix that appears as part of the description.

6.  Activate or deactivate the cluster by selecting or clearing the **Activate** check box.

7.  Select **Update** to save your changes.


## Result

The manual cluster is saved in the EM Impact Manual Cluster \[em\_impact\_manual\_cluster\] table. The impact calculation is recalculated automatically.

**Parent Topic:**[Configuring CIs in a manual service as a manual cluster](../concept/manual-cluster-in-a-manual-service.md)

**Related topics**  


[Configuring CIs in a manual service as a manual cluster](../concept/manual-cluster-in-a-manual-service.md)

