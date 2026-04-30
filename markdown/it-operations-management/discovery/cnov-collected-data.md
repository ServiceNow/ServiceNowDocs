---
title: Data collected by Agent Client Collector for Kubernetes – Visibility
description: The Agent Client Collector for Kubernetes – Visibility Informer collects data on Kubernetes resources and populates various CMDB tables.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, data collected, reference, CMDB, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Agent Client Collector for Kubernetes – Visibility Reference, Kubernetes discovery using Agent Client Collector for Kubernetes – Visibility, Container discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Data collected by Agent Client Collector for Kubernetes – Visibility

The Agent Client Collector for Kubernetes – Visibility Informer collects data on Kubernetes resources and populates various CMDB tables.

The Agent Client Collector for Kubernetes – Visibility Informer collects data on the following Kubernetes resources:

-   Namespaces
-   Nodes
-   Deployments
-   Statefulsets
-   Daemonsets
-   Replicasets
-   Jobs
-   Cronjobs
-   Pods
-   Services
-   ReplicationController
-   Ingresses

The Informer collects data on the following OpenShift resources:

-   DeploymentConfig
-   BuildConfig
-   Routes
-   Groups
-   Users
-   Projects
-   Images
-   ImageStreams

The Informer populates the following CMDB tables:

-   cmdb\_ci\_kubernetes\_cluster
-   cmdb\_ci\_kubernetes\_namespace
-   cmdb\_ci\_kubernetes\_node
-   cmdb\_ci\_kubernetes\_deployment
-   cmdb\_ci\_kubernetes\_statefulset
-   cmdb\_ci\_kubernetes\_daemonset
-   cmdb\_ci\_kubernetes\_replicaset
-   cmdb\_ci\_kubernetes\_job
-   cmdb\_ci\_kubernetes\_cronjob
-   cmdb\_ci\_kubernetes\_pod
-   cmdb\_ci\_kubernetes\_service
-   cmdb\_ci\_kubernetes\_replicationcontroller
-   cmdb\_ci\_kubernetes\_ingress
-   cmdb\_ci\_docker\_container
-   cmdb\_ci\_docker\_image
-   cmdb\_ci\_container\_repository\_entry
-   cmdb\_ci\_container\_repository
-   cmdb\_ci\_linux\_server
-   cmdb\_ci\_openshift\_dep\_conf
-   cmdb\_ci\_openshift\_build\_conf
-   cmdb\_ci\_openshift\_route
-   cmdb\_ci\_openshift\_group
-   cmdb\_ci\_openshift\_user
-   cmdb\_ci\_openshift\_project
-   cmdb\_ci\_openshift\_images
-   cmdb\_ci\_openshift\_images\_stream

