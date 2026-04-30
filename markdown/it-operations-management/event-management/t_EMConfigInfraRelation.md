---
title: Create an infrastructure relationship for related CIs
description: Infrastructure relationships show CIs that are connected to a application service but are not necessary parts of the service. Infrastructure relationships are only available for application services.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create an infrastructure relationship for related CIs

Infrastructure relationships show CIs that are connected to a application service but are not necessary parts of the service. Infrastructure relationships are only available for application services.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

When you create a CI infrastructure relationship, the information is stored in the Infrastructure Relations \[em\_impact\_infra\_rel\_def\] table. When alerts generate, the related CI accompanies the application service information on the Event Management dashboard and in the impact tree. Additional information for the related CIs only appears on a related dependency view map for the application service. The following default infrastructure relationships are available.

|Infrastructure relationship|Impact rule|Description|
|---------------------------|-----------|-----------|
|cmdb\_ci\_appl|OS Cluster Member|Shows alert impact between hardware and software applications.|
|cmdb\_ci\_esx\_server|Infrastructure Dependencies|Shows alert impact between VCenter and ESX clusters.|
|cmdb\_ci\_kvm|Infrastructure Dependencies|Shows that alert impact on Linux Kernel-based Virtual Machine \(KVM\) connectivity.|
|cmdb\_ci\_vm\_zones|Infrastructure Dependencies|Shows alert impact on the Solaris VM zones.|

For example, based on of the cmdb\_ci\_vm\_zones Infrastructure relationship definition, Event Management adds ZoneServer@mmp1 to the application service. The Containment rule manages impact severity on alerts.

![Infrastructure relationships for a manual service](../image/EventManagementRelatedCI.png "Related CIs appear on the BSM")

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Infrastructure Relations**.

2.  Click **New**.

3.  Fill in the fields, as appropriate.

<table><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Child Type

</td><td>

The table that contains data about the child entity.

</td></tr><tr><td>

Parent Type

</td><td>

The table that contains data about the parent entity.

</td></tr><tr><td>

Relation Type

</td><td>

The relationship between the child and parent entities.

</td></tr><tr><td>

Impact Direction

</td><td>

The impacts direction to show on the application service map.-   **From Child to Parent**: When an alert is regarding a child, show the impact on the parent.
-   **From Parent to Child**: When an alert is regarding a parent, show the impact on the child entity.


</td></tr><tr><td>

Impact Rule

</td><td>

The impact rule to calculate infrastructure relationships:-   **OS Cluster Member** : Determines how host cluster members affect the overall cluster status based on a percentage or number of cluster members. For example, if a three-host cluster requires **60% Influence** to set the severity of **Major**, each member has **20% Influence** \(60% divided by 3\). The severity of the entire cluster can only change to **Major** when two or more cluster members have a severity of **Major**. The entire cluster is also considered to be down.
-   **Application Cluster Member** : Determines how application cluster members affect the overall impact of the cluster. For example, if a three-member cluster requires **90% Influence** to set the severity for the entire cluster to **Major**, each member has **30% Influence** \(90% divided by 3\). The severity of the entire cluster can only change to **Major** when all three members have a severity of **Major**.
-   **Infrastructure Dependencies** : Determines the definition of impact propagation for CIs in infrastructure relationships.
-   **CI Application Service**: Determines how impact applies to parent or child entities that are part of an application service.
-   **CI Parent in Application**: Sets impact only on the parent entity.
-   **Inclusion**: Determines the impact on entities with a Contains relationship. This rule is read-only.
-   **Network Path**: Determines how impact applies to parent or child entities that are part of a traditional network.
-   **Storage Path**: Determines how impact applies to parent or child entities that are part of a storage network.
-   **CI Impact** : Applies to application services. Determines the relationship between service members. The impact from child to parent CIs is always 100%. For example, the parent impact severity is derived from the child CI with the highest severity.


</td></tr></tbody>
</table>4.  Click **Submit**.


