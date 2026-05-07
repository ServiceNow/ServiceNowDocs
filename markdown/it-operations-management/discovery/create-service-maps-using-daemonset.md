---
title: Enable service maps using DaemonSet
description: Enable application service maps based on the traffic between the workloads in Kubernetes by using a ServiceNow DaemonSet as part of Kubernetes Visibility Agent \(KVA\) installation.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enabling application service maps, Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Enable service maps using DaemonSet

Enable application service maps based on the traffic between the workloads in Kubernetes by using a ServiceNow DaemonSet as part of Kubernetes Visibility Agent \(KVA\) installation.

## Before you begin

Role required: discovery\_admin.

## About this task

If you use a ServiceNow DaemonSet, a pod is running on each Kubernetes node and reports to the main Informer pod every 60 seconds on new connections detected. For more information, see [Install Kubernetes Visibility Agent \(KVA\) Informer](cnov-deploy-install.md)

## Procedure

-   Set parameters either during Helm chart archive installation or by modifying the Kubernetes YAML file provided by ServiceNow.

<table id="choicetable_ucg_fpk_bgc"><thead><tr><th align="left" id="d152425e92">

Method

</th><th align="left" id="d152425e95">

Actions

</th></tr></thead><tbody><tr><td id="d152425e101">

**During Helm chart archive installation**

</td><td>

1.  In the Helm `install` command, add the following parameter:

    ```
--set connectionsDiscovery.method=servicenow 
    ```

2.  If your organization's policy requires it, pull the DaemonSet image from Docker hub and place it in your organization’s image repository.

Replace the placeholder X characters with the number of the most recent release provided in the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Helm Chart and Kubernetes YAML file releases \[KB1564347\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1564347) article in the Now Support Knowledge Base.

    ```
Docker pull servicenowdocker/informer_ds:X.X.X
Docker tagservicenowdocker/informer_ds:X.X.X COMPANY_REPO:X.X.X
    ```

3.  In the `Helm install` command, add the following parameters:

`--set image.dsRepository=COMPANY_REPO –set image.dsTag=X.X.X`

</td></tr><tr><td id="d152425e144">

**Modifying the `k8s_informer.yaml` file**

</td><td>

1.  In the `k8s_informer.yaml` file, uncomment the DaemonSet, ServiceAccount \(used by the DaemonSet\), and Service.Deployment resources according to the instructions in the file.
2.  Uncomment the lines containing environment variables.
3.  If your Prometheus server URL isn't the default one, uncomment the lines containing the environment variable *PROMETHEUS\_URL* and change the value.
4.  Run the following command:

    ```
kubectl apply -f k8s_informer.yaml
    ```

</td></tr></tbody>
</table>
## What to do next

[Create application service maps](create-an-app-service-map-kva.md)

**Parent Topic:**[Enabling application service maps](../concept/enabling-application-service-maps.md)

