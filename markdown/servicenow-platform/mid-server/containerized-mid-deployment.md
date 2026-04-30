---
title: Containerized MID Server Deployment and Auto-configuration
description: An agent admin can enter a MID Server Profile and create a deployment request on the instance. She/he can then export the deployment request to a YAML file and use it to deploy MID Servers to Kubernetes or OpenShift cluster.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Containerized MID Server, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Containerized MID Server Deployment and Auto-configuration

An agent admin can enter a MID Server Profile and create a deployment request on the instance. She/he can then export the deployment request to a YAML file and use it to deploy MID Servers to Kubernetes or OpenShift cluster.

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>Containerized MID Servers use a Docker image of the MID Server that allows you to quickly deploy MID Servers. The documentation for [Build MID Server Docker Image for Linux](../task/mid-build-docker-linux.md#) provides steps for manually preparation and deployment. The following Containerized MID Server auto-configuration simplifies the process and makes it scalable.

## MID Server profile

A MID Server profile contains all the settings required to configure a new MID Server, excluding sensitive data such as passwords and certificates. Sensitive data should be passed through Secrets created on the K8s cluster. The user only enters secret names and locations in the deployment request. An **agent\_admin** role is required to create or change profiles. MID Server profiles are stored in the following tables:

-   mid\_server\_profile
-   mid\_profile\_config
-   mid\_profile\_wrapper\_config
-   mid\_profile\_property
-   mid\_profile\_application\_m2m
-   mid\_profile\_capability\_m2m
-   mid\_profile\_ip\_range\_m2m
-   mid\_profile\_cluster\_m2m

During deployment, the **mid\_profile\_config** and **mid\_profile\_wrapper\_config** parameters are sent to the K8s cluster. These parameters populate the `config.xml` and `wrapper-override.conf` of the new MID Server. The other parameters are used by the auto-configuration on the instance. The user can access the MID Server profile from the module **MID Server Profiles** on the instance.

The MID Server name is not required in a profile because a profile can be used to deploy multiple MID Servers. Instead, the user is asked to enter MID Server names as part of a new deployment request. For the **mid\_profile\_wrapper\_config**, the user can enter any parameters that they want to see in `wrapper-override.conf`. For example:

<table id="table_jv2_nk3_fsb"><tbody><tr><td>

**Name**

</td><td>

**Value**

</td></tr><tr><td>

wrapper.java.maxmemory

</td><td>

2048

</td></tr><tr><td>

wrapper.java.additional.3

</td><td>

-Djavax.net.debug=ssl:handshake

</td></tr></tbody>
</table>Other profile settings can be entered the same way as on a MID Server record.

## MID Server Deployment Request

After creating a MID server profile, the user can make a new deployment request to prepare the deployment process.​ A deployment request can be different for different container orchestrators. See [MID Server Deployment Request](../task/containerized-mid-deploy-request.md) for more information.

## Export MID Deployment Request for Manual Deployment

The user can export it to a K8s deployment YAML file. The user can download the YAML file to the K8s cluster and deploy new MID Servers with the following command: `kubectl apply –f <yaml_file>`

## Docker image preparation

To prepare a Docker image, first build a MID Server image on a K8s cluster as explained in [Build MID Server Docker Image](../task/mid-build-docker-linux.md#). Upload the built image to an image registry and pull the image to a local image with the command: `docker pull registry/mid:<tag>`. Refer to [Docker Registry Setup for Containerized MID Server II: Auto Configuration \[KB1001380\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1001380) for information on limitations on pulling an image directly from a remote registry.

## Kubernetes preparation

See also [How to build and deploy Containerized MID Servers in Kubernetes using StatefulSets \[KB1325173\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1325173).

**Kubernetes service account setup**

Ensure the service account has the proper RBAC set up to create, delete, and list permission for resources. The following example YAML file uses the default service account:

```
apiVersion: rbac.authorization.k8s.io/v1 
 kind: ClusterRoleBinding 
 metadata:   
    name: default-service-acccount-as-cluster-admin 
 subjects:   

  - kind: ServiceAccount 
    # Reference to upper's `metadata.name`     
    name: default 
    # Reference to upper's `metadata.namespace`     
    namespace: default 
 roleRef:   
    kind: ClusterRole 
    name: cluster-admin 
    apiGroup: rbac.authorization.k8s.io
```

You may choose a custom service account and assign a **ClusterRole** to that service account and name space. The default name space is **default**. The following example YAML file uses a custom name space, **mynamespace**.

```
apiVersion: rbac.authorization.k8s.io/v1 
 kind: ClusterRoleBinding 
 metadata:   
    name: custom-serviceacccount-as-cluster-admin 
 subjects:   

  - kind: ServiceAccount 
    # Reference to upper's `metadata.name`     
    name: mycustomserviceaccount 
    # Reference to upper's `metadata.namespace`     
    namespace: mynamespace 
 roleRef:   
    kind: ClusterRole 
    name: cluster-admin 
    apiGroup: rbac.authorization.k8s.io
```

**Kubernetes Secret setup**

Secrets are created for **mid-secrets.properties** or PEM files for mutual authentication. For more information about how to create a Secret, see the section in [Containerized MID Server](containerized-mid.md).

## Auto-configure new Containerized MID Servers

When a MID server is connected to the instance for the first time, a MID Server record is created. The MID Server record is populated with the container ID, profile ID and deployment name. The **Auto-Configure MID from profile** business rule is triggered when the new MID Server record is updated with a profile ID in the **profile\_id** field. The business rule looks up the profile settings associated with that profile ID and configures the new MID server accordingly.

## Sync MID Server Profile to existing MID Servers

The MID Server profile can be out-of-sync with the settings of existing MID Servers if the user updates the profile long after the related MID Servers were auto-configured. The user can synchronize the profile settings to the existing MID Server by selecting **Sync to MID Servers** on the instance.

**Note:** When applying cluster settings from MID Server profile to a MID Server, the cluster assignment will fail if the MID Server doesn't have any capability assigned. It is controlled by the "validate MID server capability" business rule on the ecc\_agent\_cluster\_member\_m2m table. If you want to assign a MID server to a cluster, please make sure it has some capabilities.

