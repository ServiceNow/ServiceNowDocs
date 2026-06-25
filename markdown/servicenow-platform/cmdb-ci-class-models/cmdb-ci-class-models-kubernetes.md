---
title: Kubernetes extension classes
description: The Discovery and Service Mapping app adds or updates classes for the Kubernetes pattern.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-kubernetes.html
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

See the release notes for all CMDB CI class models.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Kubernetes pattern

The Kubernetes pattern main flow helps with discovering Kubernetes core elements. The classes in this release, extend the support to discover Kubernetes workload controller components like deployments, daemonsets, and statefulsets. The Workload Share library captures information about deployments, daemonsets, and statefulsets and stores them in the respective tables. Other extensions include a YAML and service mesh extension that generates a YAML file to track configuration files and creating service to service relations by discovering service mesh information.

\[Omitted image "cmdb-kubernetes-model-pattern-diagram.png"\] Alt text: Kubernetes extension class integrated with the CMDB hierarchy.

\[Omitted image "cmdb\_kubernetes\_workload.png"\] Alt text: Kubernetes workload.

## Classes

This section lists the classes that the CMDB CI Class Models app adds or updates.

CMDB CI Class Models: Release 1.12.0 adds the following classes for Kubernetes pattern. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-tables-details.md).

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


[CMDB schema model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_ConfigurationManagementDatabase.md)

