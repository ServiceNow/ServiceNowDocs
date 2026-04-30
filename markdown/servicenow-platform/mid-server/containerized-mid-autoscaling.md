---
title: Containerized MID Server Autoscaling
description: MID Servers can be deployed via StatefulSet with any number of replicas. They can scale automatically by leveraging Kubernetes Horizontal Pod Autoscaler \(HPA\). Horizontal Pod Autoscaler automatically updates a workload resource \(such as a Deployment or StatefulSet\) to match demand.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Containerized MID Server, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Containerized MID Server Autoscaling

MID Servers can be deployed via StatefulSet with any number of replicas. They can scale automatically by leveraging Kubernetes Horizontal Pod Autoscaler \(HPA\). Horizontal Pod Autoscaler automatically updates a workload resource \(such as a Deployment or StatefulSet\) to match demand.

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>Kubernetes can add or remove any numbers of stateful MID Server replicas as required by the workload. HPA only supports CPU and memory metrics. MID Servers can be deployed as a stateful application by providing the following information in the StatefulSet section of the deployment request form:

-   Name
-   Headless service name
-   Persistent volume claim \(PVC\)
-   Parameters, such as storage class, access modes, and storage request
-   The resource request/limit

The PVC declares the desired persistent volume where the MID Server stores config.xml, meta data files, and several of its sub-folders.

During workload fluctuations, a pod with a running MID Server container can be removed and replaced by a new one. StatefulSet ensures the same persistent volume is attached to the new pod, which allows the MID Server to resume its state.

The only sub-folders that can be mounted to the persistent volume are those that are initially empty with a new MID Server installation. The **config.xml** file and other meta data files must be backed up when the pod is shut down and restored during start-up.

Deployment requests exported as YAML files can be used to create a StatefulSet workload and new MID Server pods in the Kubernetes cluster.

When you make changes to the deployment YAML file and re-apply it, the existing pods of the deployment are recreated. With StatefulSet deployment, the configuration files are restored from the backup folder. The init script must detect the deployment environment changes and apply them to the configuration files before MID server is started.

## HPA Autoscaling activation

HPA Autoscaling can be activated for any existing StatefulSet workload by creating an HPA controller.

When you create a deployment request, you can choose either HPA version 1 or version 2.

When creating a deployment request on the instance with an HPA configuration, apply the exported YAML file and HPA autoscaling begins working immediately.

