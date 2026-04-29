---
title: Preconfigured CI relationships in tag-based discovery
description: Several preconfigured CI relationships participate in tag-based discovery, by default. The Traversal Rules for Application Services \[svc\_traversal\_rules\] table stores these relationships.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Preconfigured CI relationships in tag-based discovery

Several preconfigured CI relationships participate in tag-based discovery, by default. The Traversal Rules for Application Services \[svc\_traversal\_rules\] table stores these relationships.

**Important:** You cannot delete or modify preconfigured CI relationships used for tag-based discovery from the Traversal Rules for Application Services \[svc\_traversal\_rules\] table.

|CI|Relationship|CI|
|---|------------|---|
|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Virtualizes:: Virtualized by|Hardware \[cmdb\_ci\_hardware\]|
|Hardware \[cmdb\_ci\_hardware\]|Runs::Runs on|Application \[cmdb\_ci\_appl\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contains::Contained by|Operating-system-level Virtualization Container \[cmdb\_ci\_oslv\_container\]|

|CI|Relationship|CI|
|---|------------|---|
|Configuration Item \[cmdb\_ci\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|Contained By::Contains|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|OpenShift Project \[cmdb\_ci\_openshift\_project\]|Contained by::Contains|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Contained by::Contains|Kubernetes Cluster \[cmdb\_ci\_kubernetes\_cluster\]|
|Kubernetes Pod \[cmdb\_ci\_kubernetes\_pod\]|Cluster::Cluster of|Kubernetes Service \[cmdb\_ci\_kubernetes\_service\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]​|Contains::Contained By|OpenShift Deployed Config \[cmdb\_ci\_openshift\_dep\_conf​\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]​|Contains::Contained By|OpenShift Build Config \[cmdb\_ci\_openshift\_build\_conf\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]​|Contains::Contained By|OpenShift Route \[cmdb\_ci\_openshift\_route\]|
|Kubernetes Namespace \[cmdb\_ci\_kubernetes\_namespace\]​|Contains::Contained By|OpenShift Image Stream \[cmdb\_ci\_openshift\_images\_stream\]|

**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

