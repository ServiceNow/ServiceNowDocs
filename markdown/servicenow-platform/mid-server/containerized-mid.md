---
title: Containerized MID Server
description: Containerized MID Server uses a Docker image of the MID Server that allows you to quickly deploy MID Servers at scale. MID Servers are deployed using orchestration tools like OpenShift or Kubernetes. Orchestration tools can automate their deployment and maintenance and add new containers on demand or replace failed containers automatically.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Containerized MID Server

Containerized MID Server uses a Docker image of the MID Server that allows you to quickly deploy MID Servers at scale. MID Servers are deployed using orchestration tools like OpenShift or Kubernetes. Orchestration tools can automate their deployment and maintenance and add new containers on demand or replace failed containers automatically.

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>To use Containerized MID Servers, you can download Docker recipes for Linux from the MID Server download page. Use the recipes to build the Docker images for the current release. The recipes are zipped and signed. Some features have been deprecated for the Washington DC family release. See [\[KB1559617\] Deprecated Containerized MID Server Features in Washington DC](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1559617) for more information.

Containerized MID Server system requirements:

-   AlmaLinux is supported.

-   The recipes cannot be used to build images for previous MID Server versions.

-   Discovery of NMAP and CyberArk are not supported.

-   Other applications such as Orchestration and Integration Hub are not certified.


Once the Docker images are available, you can create new MID Server containers and configure them with configuration parameters passed through environment variables or secret files. Docker, Openshift, and Kubernetes secrets are supported. The MID Server application inside the container is run as a process by a non-admin user.

When a containerized MID Server record is first created on the instance, a random UUID is created and set to the **container\_id** column. During the start-up sequence, this value is replaced by the actual container ID. The container ID can be used to differentiate between containerized and regular MID Servers. Non-containerized MID Servers' container ID have a null or empty value.

In order to automatically clean up the down MID Servers on Instance, a scheduled job called Purge Orphaned Containerized MID Servers is scheduled to run daily. This job removes orphaned containerized MID Servers if they are down longer than the value set by the **max\_retention\_days** property. The job also creates a warning MID Server issue each day before the removal day, if there are equal to or less than the value of **warn\_days** remaining. The default values for **max\_retention\_days** and **warn\_days** are 30 and 7, respectively.

## Auto-upgrade

Auto-upgrade works the same way for containerized MID Servers as it does for regular MID Servers. However, it is recommended to disable the auto-upgrade for containerized MID Servers. Whenever a new image is needed, build a new image and deploy it by updating the deployment YAML file then re-apply it.

Containerized MID Server auto-upgrade is controlled by the **mid.container.autoupgrade.enabled** config parameter and is set to true by default. The config parameter is read-only, therefore it can not be synced down from the instance.

Add the config parameter to a MID Server profile and use it with new deployment requests. The settings are then included in deployment YAML file when the deployment request is exported, or when it is manually added to an existing deployment YAML file and re-applied.

## HealthCheck

A HEALTHCHECK rule is implemented to check MID Server health status based on heartbeat every 5 minutes. If there was no heartbeat activity in last 30 minutes, it is considered a failure. After 3 consecutive failures, it becomes unhealthy in the docker ps command output.

To see more HealthCheck details, run the following [docker inspection command](https://docs.docker.com/engine/reference/commandline/inspect/): `docker inspect --format='{{json .State.Health}}' <container-id>`

## Basic Container Operations

Basic operations are supported on container side. For example, you can stop, start, or restart a running container using Docker commands.

-   **docker stop &lt;container\_id&gt;**

    This command shuts down the containerized MID Server.

-   **docker start &lt;container\_id&gt;**

    This command starts a containerized MID Server if it is stopped.

-   **docker restart &lt;container\_id&gt;**

    This command shuts down a MID Server and restarts it.


## Build MID Server Docker Image

[Build a MID Server Docker Image](../task/mid-build-docker-linux.md#) with the provided recipes to deploy a Containerized MID Server. Containerized MID Server uses a Docker image of the MID Server that allows you to quickly deploy MID Servers at scale.

## Containerized MID Server Deployment and Auto-configuration

With the [deployment and auto-configuration feature](containerized-mid-deployment.md), an agent admin can enter all required MID Server  settings in a MID Server Profile on the instance and then submit a deployment request to K8s cluster. After the request is  processed, the new MID servers are automatically created and auto-configured. They are ready  to use in seconds.  If the MID Server profile is changed, the related Containerized MID Servers can also be updated on demand.

