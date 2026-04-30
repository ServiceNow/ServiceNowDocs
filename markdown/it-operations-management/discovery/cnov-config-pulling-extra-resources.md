---
title: Pulling additional resources from Kubernetes clusters into the CMDB
description: You can configure the Kubernetes Visibility Agent Informer to pull extra resources from Kubernetes clusters into the Configuration Management Database \(CMDB\), in addition to the resources it sends to the database by default. By pulling in additional resources beyond the default set, you can enhance visibility into your Kubernetes clusters.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, pull data, cluster, CMDB, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Pulling additional resources from Kubernetes clusters into the CMDB

You can configure the Kubernetes Visibility Agent Informer to pull extra resources from Kubernetes clusters into the Configuration Management Database \(CMDB\), in addition to the resources it sends to the database by default. By pulling in additional resources beyond the default set, you can enhance visibility into your Kubernetes clusters.

The Informer collects data on Kubernetes resources, sends the collected data to the instance, and updates the appropriate tables in the CMDB. For a list of the resources the Informer pulls into the CMDB by default, see [Data collected by CNO for Visibility](../reference/cnov-collected-data.md).

For every additional Kubernetes resource you want the Informer to pull into the CMDB, the system creates a Configuration Item \(CI\) in the cmdb\_ci\_kubernetes\_component target table. Alternatively, extra resources can be pulled to custom tables that extend the cmdb\_ci\_kubernetes\_component table. For example, you could create a u\_cmdb\_ci\_kubernetes\_configmap table for all ConfigMap resources in the cluster. The system creates a relation and a reference from the table to the cluster CI for every additional resource. If the resource is namespaced, a relation to the namespace CI is created.

By default, the Informer pulls the following information from the Kubernetes cluster for each additional resource:

-   Name
-   Namespace \(for namespaced resources\)
-   Kubernetes ID
-   API version
-   Kind
-   Labels and Annotations

Along with this default data, you can make the Informer pull further information on the additional resources into the CMDB. By default, the system stores this extra data in the attributes field of the cmdb\_ci\_kubernetes\_component table. You can also create a custom field per additional resource for storing the extra information.

Kubernetes Visibility Agent enables you to filter additional resources by defining filtering conditions. If a condition shows a match, the Informer sends the resource to the CMDB.

For more detailed information and procedures for pulling additional resources from Kubernetes clusters into the CMDB, see the [Discovering additional Kubernetes resources using CNO for Visibility \(Informer\) \[KB1638668\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1638668) article in the Now Support Knowledge Base.

**Parent Topic:**[Configuring Kubernetes Visibility Agent](cnov-configuring.md)

