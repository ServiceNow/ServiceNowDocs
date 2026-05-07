---
title: Enable service maps using service meshes
description: Enable application service maps based on the traffic between the workloads in Kubernetes by using Istio or Linkerd or service meshes as part of Kubernetes Visibility Agent \(KVA\) installation.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enabling application service maps, Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Enable service maps using service meshes

Enable application service maps based on the traffic between the workloads in Kubernetes by using Istio or Linkerd or service meshes as part of Kubernetes Visibility Agent \(KVA\) installation.

## Before you begin

You must have a Prometheus server and provide the Prometheus URL.

Role required: discovery\_admin.

## About this task

If you use a service mesh, a pod running on every node \(Informer\) communicates with a Prometheus server to get the traffic information. For more information, see [Install Kubernetes Visibility Agent \(KVA\) Informer](cnov-deploy-install.md)

## Procedure

-   Set parameters either during Helm chart archive installation or by modifying the Kubernetes YAML file provided by ServiceNow.

<table id="choicetable_cc2_2vk_bgc"><thead><tr><th align="left" id="d478358e89">

Method

</th><th align="left" id="d478358e92">

Actions

</th></tr></thead><tbody><tr><td id="d478358e98">

**During Helm installation**

</td><td>

In the `Helm install` command, add the following parameter:

```
--set connectionsDiscovery.method=<METHOD>
```

where &lt;METHOD&gt; is the URL for either Istio \(http://prometheus.istio-system:9090\) or Linkerd \(http://prometheus.linkerd-viz:9090\).

 **Note:**

If your Prometheus server URL is not the default one, use the following parameter:

```
--set connectionsDiscovery.prometheusUrl
```

</td></tr><tr><td id="d478358e124">

**Modify the `k8s_informer.yaml` script**

</td><td>

1.  Access the `k8s_informer.yaml` script.
2.  Set the environment variable *k8s\_informer.yaml* by entering either Istio or Linkerd in quotation marks:

    ```
-- name: GET_CONNECTIONS_METHOD value: "" 
    ```

3.  Run the following command:

    ```
kubectl apply -f k8s_informer.yaml
    ```

</td></tr></tbody>
</table>
## What to do next

[Create application service maps](create-an-app-service-map-kva.md)

**Parent Topic:**[Enabling application service maps](../concept/enabling-application-service-maps.md)

