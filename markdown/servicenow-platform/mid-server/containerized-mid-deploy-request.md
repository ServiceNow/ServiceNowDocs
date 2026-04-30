---
title: MID Server Deployment Request
description: After creating a MID server profile, the user can make a new deployment request to prepare the deployment process.​ A deployment request can be different for different container orchestrators.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Containerized MID Server Deployment and Auto-configuration, Containerized MID Server, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server Deployment Request

After creating a MID server profile, the user can make a new deployment request to prepare the deployment process.​ A deployment request can be different for different container orchestrators.

## Before you begin

Role required: agent\_admin

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>## About this task

The user can access MID Server deployment request from the app module **MID Deployment Requests**.​

Currently, only K8s deployment is supported. The K8s deployment request includes a reference to a MID Server profile, information about a MID Server docker image, K8s secrets, K8s deployment labels, and a list of MID Server names to assign to the new MID Servers.

## Procedure

1.  Enter information about the container image.

    In this section, you will specify which image is used with this deployment request and where it can be pulled from.

    -   **Image Registry Path and Repository**

        Enter a registry address and port, as well as a repository name where the image is stored. The syntax is `my.registry.address:port/repositoryname`.

    -   **Image Tag**

        Enter a tag that identifies the container image.

2.  Specify the MID Server names.

    A deployment request can be made to create multiple MID Servers. You can choose to enter the MID Server names manually, otherwise the system automatically generates them. If you enter the names manually, each MID Server name must be unique.

3.  Enter the Kubernetes cluster Information.

    -   **K8s Namespace**

        Enter a K8s namespace where the new MID servers are located. The default value is **default**.

    -   **K8s Service Account**

        Enter a K8s service account name that processes this deployment request. The default value is **default**.

    -   **MID Secrets Name**

        Enter the name of a K8s secrets object that holds MID Server secrets.

    -   **MID Secrets File Path**

        Enter the absolute path of the MID Server secrets file inside the container.

    -   **MID Mutual Auth PEM Secrets Name**

        Enter the name of a K8s secrets object that holds the MID Mutual Auth PEM certificate.

    -   **MID Mutual Auth PEM File Path**

        Enter the absolute path of the MID Mutual Auth PEM file inside container.

    -   **K8s Deployment Label**

        Enter a deployment label which is a list of key/value pairs. The label is attached to K8s deployment. A valid label must be 63 characters or less and can be empty. Unless the label is empty, it must begin and end with an alphanumeric character and contain only dashes, underscores, dots, and alphanumeric characters.


## What to do next

When a request is ready, the user can choose **Export to YAML file** to generate a K8s deployment YAML file and attach it to the same record.​ Once a request is processed, the entire record is set to read-only. There is a scheduled job that removes deployment requests older than 365 days.

