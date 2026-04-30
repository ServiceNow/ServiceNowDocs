---
title: Kubernetes extension classes
description: The Discovery and Service Mapping app adds or updates classes for the Kubernetes pattern.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Kubernetes extension classes

The Discovery and Service Mapping app adds or updates classes for the Kubernetes pattern.

The app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. You can use the added classes as any other CMDB class. Applications such as Discovery and Service Mapping patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Kubernetes pattern

The Kubernetes pattern main flow helps with discovering Kubernetes core elements. The classes in this release, extend the support to discover Kubernetes workload controller components like deployments, daemonsets, and statefulsets. The Workload Share library captures information about deployments, daemonsets, and statefulsets and stores them in the respective tables. Other extensions include a YAML and service mesh extension that generates a YAML file to track configuration files and creating service to service relations by discovering service mesh information.

![Kubernetes extension class integrated with the CMDB hierarchy.](../image/cmdb-kubernetes-model-pattern-diagram.png "Kubernetes extension class integrated with the CMDB hierarchy")

![Kubernetes workload.](../image/cmdb_kubernetes_workload.png "Kubernetes workload")

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates.

CMDB CI Class Models: Release 1.12.0 adds the following classes for Kubernetes pattern. For the list of CMDB classes in a base system, including ones that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_uwm_1zl_vlb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Fields

</th><th>

Relation

</th></tr></thead><tbody><tr><td>

cmdb\_ci\_kubernetes\_workload

</td><td>

cmdb\_ci\_kubernetes\_components

</td><td>

 

</td><td>

Provides from cmdb\_ci\_kubernetes\_service

</td></tr><tr><td>

cmdb\_ci\_kubernetes\_deployment

</td><td>

cmdb\_ci\_kubernetes\_workload

</td><td>

-   Replicas Desired
-   Replicas Updated
-   Replicas Total
-   Replicas Available
-   Replicas Unavailable

</td><td>

Hosted on Cluster

</td></tr><tr><td>

cmdb\_ci\_kubernetes\_daemonset

</td><td>

cmdb\_ci\_kubernetes\_workload

</td><td>

-   Pods running
-   Pods Waiting
-   Pods Succeeded
-   Pods Failed
-   Pods Available

</td><td>

Hosted on Cluster

</td></tr><tr><td>

cmdb\_ci\_kubernetes\_statefulset

</td><td>

cmdb\_ci\_kubernetes\_workload

</td><td>

-   Pods running
-   Pods Waiting
-   Pods Succeeded
-   Pods Failed
-   Pods Available

</td><td>

Hosted on Cluster

</td></tr></tbody>
</table>**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

