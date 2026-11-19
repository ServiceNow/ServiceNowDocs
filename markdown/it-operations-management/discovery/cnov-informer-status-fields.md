---
title: Kubernetes Visibility Agent Informer status fields
description: The fields in the Kubernetes Visibility Agent Informers table sn\_acc\_visibility\_kubernetes\_informer describe the status of the Informer pods deployed in your Kubernetes clusters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery/cnov-informer-status-fields.html
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Agent Client Collector, Kubernetes, Visibility, Informer, status, fields, reference, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Kubernetes Visibility Agent Reference, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Kubernetes Visibility Agent Informer status fields

The fields in the Kubernetes Visibility Agent Informers table `sn_acc_visibility_kubernetes_informer` describe the status of the Informer pods deployed in your Kubernetes clusters.

<table id="table_vql_dsh_tyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Informer name

</td><td>

System-generated name of the Informer, based on the unique ID of the cluster. When a new cluster CI is created, the Informer name is identical to the name you configured for the cluster.

 Select this field to view the available actions on the selected Informer.

</td></tr><tr><td>

Kubernetes cluster

</td><td>

Reference to the cluster CI.

 Select this field to view details of the cluster.

</td></tr><tr><td>

Full discovery status

</td><td>

Status of the current full discovery. Possible values are: Empty, In Progress, Queued, Completed, Failed, Skipped, and Timed out.

 **Note:** Full discovery is performed either periodically or on demand. By default, it is run once a day. Full discovery status is considered Skipped if, when the time came to run full discovery by a given informer, the informer was in the Down state and was not able to communicate with the instance. The full discovery status is considered Timed Out if the instance doesn't receive confirmation that the full discovery is completed within the expected time window.

</td></tr><tr><td>

Last full discovery

</td><td>

The time that the last full discovery was completed.

</td></tr><tr><td>

Informer version

</td><td>

The version of the Informer pod that is running in the cluster.

</td></tr><tr><td>

Status

</td><td>

The status of the Informer. Possible values are: Up, Down, Paused.

 **Note:** The status of an Informer is considered Down when no message has been received in the last 15 minutes.

 When the auto-retirement feature is enabled, clusters with Informers in the Down state for an extended period may be automatically retired during full discovery cycles. For more information, see [Enable automatic retirement for inactive Kubernetes cluster CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/remove-inactive-cis.md).

</td></tr><tr><td>

Continuous Discovery Status

</td><td>

The status of continuous discovery. Possible values are: On or Off.

</td></tr><tr><td>

Upgrade Status

</td><td>

The upgrade status of Informers in the cluster. Possible values are: Upgrade Pending, Upgrading, Desired image in use, Upgrade using kubectl/Helm.**Note:** When the upgrade status of an Informer is Upgrade using kubectl/Helm, contact your Kubernetes admin to upgrade the informer manually.

</td></tr></tbody>
</table>**Parent Topic:**[Kubernetes Visibility Agent Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/cnov-reference.md)

