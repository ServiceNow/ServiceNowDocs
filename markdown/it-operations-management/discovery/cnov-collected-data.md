---
title: Data collected by Kubernetes Visibility Agent
description: The Kubernetes Visibility Agent Informer collects data on Kubernetes resources and populates various CMDB tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/cnov-collected-data.html
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Agent Client Collector, Kubernetes, Visibility, data collected, reference, CMDB, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Reference, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Data collected by Kubernetes Visibility Agent

The Kubernetes Visibility Agent Informer collects data on Kubernetes resources and populates various CMDB tables.

For the information about the data Kubernetes Visibility Agent Informer collects on the Kubernetes resources and OpenShift resources, and about the CMDB tables it populates, see the KB article [KB2669848](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=5883b26493ca3a10d9743f986cba1060)

\[Omitted image "kva-ci-relationships.png"\] Alt text: Relationships between CIs created by Kubernetes Visibility Agent \(KVA\)

## CI relationships created by Kubernetes Visibility Agent \(KVA\)

The following tables list the CMDB CI relationships that Kubernetes Visibility Agent \(KVA\) creates. The relationship type names match the values written to the cmdb\_rel\_type table.

Relationships created by default:

|Source CI|Relationship type|Target CI|
|---------|-----------------|---------|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Cluster of::Cluster|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|Kubernetes Component \[cmdb\_ci\_kubernetes\_component\] — Gateway API / Traefik IngressRoute, watched out of the box \(Gateway API resources require informer version 2.7.x or later, per KB2669848\)|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Members::Member of|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Deployment / StatefulSet / DaemonSet / Job / CronJob / ReplicaSet / ReplicationController \[cmdb\_ci\_kubernetes\_deployment / \_statefulset / \_daemonset / \_job / \_cronjob / \_replicaset / \_replicationcontroller\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Component \[cmdb\_ci\_kubernetes\_component\] — default-watched types, namespaced|
|Linux/Windows Server \[cmdb\_ci\_linux\_server / cmdb\_ci\_win\_server\]|Contains::Contained by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes Deployment / CronJob / DeploymentConfig \[cmdb\_ci\_kubernetes\_deployment / \_cronjob / cmdb\_ci\_openshift\_dep\_conf\]|Owns::Owned by|Kubernetes ReplicaSet / Job / ReplicationController \[cmdb\_ci\_kubernetes\_replicaset / \_job / \_replicationcontroller\]|
|Kubernetes ReplicaSet / Job / CronJob / etc. \[cmdb\_ci\_kubernetes\_replicaset / \_job / \_cronjob\]|Instantiates::Instantiated by|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|
|Kubernetes workload — Deployment / StatefulSet / DaemonSet / Job / CronJob / ReplicaSet / ReplicationController \[cmdb\_ci\_kubernetes\_deployment / \_statefulset / \_daemonset / \_job / \_cronjob / \_replicaset / \_replicationcontroller\]|Hosted on::Hosts|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Hosted on::Hosts|Linux/Windows Server \[cmdb\_ci\_linux\_server / cmdb\_ci\_win\_server\]|
|Linux/Windows Server \[cmdb\_ci\_linux\_server / cmdb\_ci\_win\_server\]|Managed by::Manages|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Provided By::Provides|Kubernetes workload it serves \[cmdb\_ci\_kubernetes\_deployment / \_statefulset / \_daemonset / \_replicaset\]|
|Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]|Provided By::Provides|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Gateway API HTTPRoute \[cmdb\_ci\_kubernetes\_component\]|Used by::Uses|Gateway \[cmdb\_ci\_kubernetes\_component\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Container \[cmdb\_ci\_docker\_container\] — non-init containers, default setting|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Docker Image \[cmdb\_ci\_docker\_image\]|
|Docker Image \[cmdb\_ci\_docker\_image\]|Instantiates::Instantiated by|Docker Container \[cmdb\_ci\_docker\_container\]|
|Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|Hosted on::Hosts|Container Repository \[cmdb\_ci\_container\_repository\]|
|Docker Image \[cmdb\_ci\_docker\_image\]|Provisioned From::Provisioned|Container Repository Entry \[cmdb\_ci\_container\_repository\_entry\]|
|Linux/Windows Server \[cmdb\_ci\_linux\_server / cmdb\_ci\_win\_server\]|Virtualized by::Virtualizes|VM Instance \[cmdb\_ci\_vm\_instance\] \(only if this CI already exists, via VMware/cloud discovery\)|
|Linux/Windows Server \[cmdb\_ci\_linux\_server / cmdb\_ci\_win\_server\]|Instantiates::Instantiated by|VMware Instance \[cmdb\_ci\_vmware\_instance\] \(only if this CI already exists, via VMware discovery\)|

Relationships created only with additional configuration. For exact Helm parameter paths, environment variable names, and system property names for each configurable relationship, see the KB article [KB1648891](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=KB1648891):

|Source CI|Relationship type|Target CI|Configuration required \(default\)|
|---------|-----------------|---------|----------------------------------|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Runs on::Runs|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|**createPodNodeRelation.enable** \(default `false`\)|
|Linux/Windows Server \[cmdb\_ci\_linux\_server / cmdb\_ci\_win\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|**createServerIpAddresses** \(default `false`\)|
|Kubernetes Node \[cmdb\_ci\_kubernetes\_node\]|Owns::Owned by|IP Address — node ExternalIP \[cmdb\_ci\_ip\_address\]|**bringNodeExternalIPs** \(default `false`\)|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Owns::Owned by|IP Address — ExternalIP / LB ingress IP \[cmdb\_ci\_ip\_address\]|**discoverK8sServiceExternalIps** \(default `false`\)|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Owns::Owned by|DNS Name — LB hostname \[cmdb\_ci\_dns\_name\]|**discoverK8sServiceExternalIps** \(default `false`\)|
|Kubernetes Ingress \[cmdb\_ci\_kubernetes\_ingress\]|Owns::Owned by|IP Address — LB address \[cmdb\_ci\_ip\_address\]|**bringIngressAddresses** \(default `false`\)|
|Kubernetes Cluster / Namespace \[cmdb\_ci\_kubernetes\_cluster / cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|Kubernetes Component — your custom resource types \[cmdb\_ci\_kubernetes\_component\]|**additionalResources.resources** \(default empty\)|
|OpenShift Route \[cmdb\_ci\_openshift\_route\]|Provided By::Provides|Target resource, for example Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|**openShift** \(default `false`\)|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]|Contains::Contained by|OpenShift DeploymentConfig / BuildConfig / Route / ImageStream \[cmdb\_ci\_openshift\_dep\_conf / cmdb\_ci\_openshift\_build\_conf / cmdb\_ci\_openshift\_route / cmdb\_ci\_openshift\_images\]|**openShift** \(default `false`\)|
|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|Contains::Contained by|OpenShift Group / User / Project / Image \[cmdb\_ci\_openshift\_group / cmdb\_ci\_openshift\_user / cmdb\_ci\_openshift\_project / cmdb\_ci\_openshift\_images\]|**openShift** \(default `false`\)|
|VM Instance — KubeVirt \[cmdb\_ci\_vm\_instance\]|Managed by::Manages|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|**sn\_acc\_visibility.kubevirt.create\_cmdb\_ci\_vm\_instance** \(default `false`\)|
|VM Instance — KubeVirt \[cmdb\_ci\_vm\_instance\]|Instantiates::Instantiated by|Raw KubeVirt VM/VMI component \[cmdb\_ci\_kubernetes\_component\]|**sn\_acc\_visibility.kubevirt.create\_cmdb\_ci\_vm\_instance** \(default `false`\)|
|Server — KubeVirt-backed \[cmdb\_ci\_server\]|Instantiates::Instantiated by|VM Instance — KubeVirt \[cmdb\_ci\_vm\_instance\]|**sn\_acc\_visibility.kubevirt.create\_server** \(default `false`\)|
|Kubernetes Pod / Service / workload \[cmdb\_ci\_kubernetes\_pod / \_service / workload tables\]|Connects to::Connected by|Kubernetes Pod / Service / TCP Endpoint \[cmdb\_ci\_kubernetes\_pod / \_service / cmdb\_ci\_endpoint\_tcp\]|**connectionsDiscovery.method** \(default empty — disabled; set to `servicenow` or `cilium` to enable\)|

**Parent Topic:**[Kubernetes Visibility Agent Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/cnov-reference.md)

