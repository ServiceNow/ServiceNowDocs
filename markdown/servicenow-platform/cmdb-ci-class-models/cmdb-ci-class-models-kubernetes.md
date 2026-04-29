---
title: Kubernetes extension classes
description: The Discovery and Service Mapping app adds or updates classes for the Kubernetes pattern.
locale: en-US
release: australia
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB CI class models, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Kubernetes extension classes

The Discovery and Service Mapping app adds or updates classes for the Kubernetes pattern.

CMDB CI Class Models is a ServiceNow Store app that adds class models that extend the CMDB class hierarchy. The new or updated classes include class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Kubernetes pattern

The Kubernetes pattern main flow helps with discovering Kubernetes core elements. The classes in this release, extend the support to discover Kubernetes workload controller components like deployments, daemonsets, and statefulsets. The Workload Share library captures information about deployments, daemonsets, and statefulsets and stores them in the respective tables. Other extensions include a YAML and service mesh extension that generates a YAML file to track configuration files and creating service to service relations by discovering service mesh information.

![Kubernetes extension class integrated with the CMDB hierarchy.](../image/cmdb-kubernetes-model-pattern-diagram.png "Kubernetes extension class integrated with the CMDB hierarchy")

![Kubernetes workload.](../image/cmdb_kubernetes_workload.png "Kubernetes workload")

## Classes

This section lists the classes that the CMDB CI Class Models app adds or updates.

CMDB CI Class Models: Release 1.12.0 adds the following classes for Kubernetes pattern. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

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

