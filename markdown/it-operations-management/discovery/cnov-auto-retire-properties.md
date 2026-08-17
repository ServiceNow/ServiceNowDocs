---
title: Kubernetes cluster auto-retirement properties
description: Configure system properties to control the automatic retirement of inactive Kubernetes cluster configuration items \(CIs\) and their associated resources, so your CMDB reflects only active infrastructure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/cnov-auto-retire-properties.html
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-07-27"
reading_time_minutes: 1
keywords: [Kubernetes, auto-retirement, system properties, configuration, cluster management]
breadcrumb: [Reference, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Kubernetes cluster auto-retirement properties

Configure system properties to control the automatic retirement of inactive Kubernetes cluster configuration items \(CIs\) and their associated resources, so your CMDB reflects only active infrastructure.

The auto-retirement feature updates the *install\_status* field to retired on inactive Kubernetes cluster CIs and all associated CIs \(pods, namespaces, deployments, containers, and other resources\). A cluster is inactive when its associated Informer is in the Down state and the cluster CI has not been updated for a configured period.

The system checks these conditions during each full discovery cycle. When the time comes to run full discovery and the Informer is in the Down state, the system evaluates the conditions and updates the status accordingly.

## Configuration properties

The following system properties control the auto-retirement behavior. Properties are located in the sys\_properties table.

<table id="table_auto_retire_properties"><thead><tr><th>

Property name

</th><th>

Type

</th><th>

Default value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_visibility.auto\_retire\_k8s\_clusters**

</td><td>

Boolean

</td><td>

false

</td><td>

Determines whether the system retires inactive Kubernetes cluster CIs handled by Kubernetes Visibility Agent \(KVA\). Set to true to enable auto-retirement.

</td></tr><tr><td>

**sn\_acc\_visibility.auto\_retire\_period\_days**

</td><td>

Integer

</td><td>

60

</td><td>

Number of days of inactivity after which the system retires a stale Kubernetes cluster. The system uses the *sys\_updated\_on* field to determine when the cluster CI was last updated.

</td></tr><tr><td>

**sn\_acc\_visibility.auto\_retire\_install\_status**

</td><td>

String

</td><td>

7

</td><td>

The numerical value the system writes to the *install\_status* field of the Kubernetes cluster CI and its associated CIs. Valid values include:-   7 \(Retired\)
-   100 \(Absent\)

**Warning:** If you set the value to 100 \(Absent\), the cluster CI and all associated CIs are deleted by a table cleanup job. This action is irreversible.

</td></tr><tr><td>

**sn\_acc\_visibility.node\_deletion\_set\_server\_install\_status**

</td><td>

String

</td><td>

No value \(empty\)

</td><td>

The numerical value the system writes to the *install\_status* field of cmdb\_ci\_linux\_server CIs associated with Kubernetes nodes. The system applies this value when nodes are deleted from the cluster or when the cluster is retired. If the property doesn't exist or is empty, the system takes no action on Linux server CIs.

</td></tr></tbody>
</table>**Parent Topic:**[Kubernetes Visibility Agent Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/cnov-reference.md)

