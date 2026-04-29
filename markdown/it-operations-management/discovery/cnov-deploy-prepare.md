---
title: Prepare for Kubernetes Visibility Agent deployment
description: Prepare your ServiceNow instance and the Kubernetes cluster for Kubernetes Visibility Agent \(KVA\) deployment.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [OKE, Agent Client Collector, Kubernetes, Visibility, deployment, installation, prerequisites, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Prepare for Kubernetes Visibility Agent deployment

Prepare your ServiceNow instance and the Kubernetes cluster for Kubernetes Visibility Agent \(KVA\) deployment.

## Before you begin

-   Verify that the following applications are installed and activated:
    -   Discovery and Service Mapping Patterns
    -   Kubernetes Visibility Agent \(KVA\) application
-   Verify that the Kubernetes command line tool kubectl is installed and configured to communicate with your cluster. For more information, see the [kubectl](https://kubernetes.io/docs/tasks/tools/#kubectl) documentation.
-   If you plan to use a Helm chart for the installation, verify that the Helm tool is available. For more information, see the [Helm](https://helm.sh/) documentation.
-   If you plan to deploy KVA in the OKE \(Oracle Kubernetes Engine\) environment, you need to create a Kubernetes Cluster on Oracle Cloud Infrastructure. For more information, see the [Oracle](https://www.oracle.com/) documentation.

Role required: admin for steps performed on the ServiceNow instance.

## Procedure

1.  On the ServiceNow instance, navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Choose or create a user with at least the mid\_server role.

    For information about adding a new user to your instance, see [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US). For information about granting a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  In the Kubernetes cluster, choose or create a namespace in which you want to deploy KVA.

    To create a namespace:

    1.  Open the kubectl command line tool.
    2.  Run the following command, after replacing NAMESPACE with the relevant value:

        `kubectl create namespace NAMESPACE`

4.  Create a Kubernetes secret that contains the ServiceNow credentials for accessing your ServiceNow instance.

    **Note:** Ensure that the credentials correspond to the user you created or identified in the earlier step.

    1.  Open the kubectl command line tool.
    2.  Run the following command, after replacing INSTANCE\_NAME, USERNAME, PASSWORD and NAMESPACE with the relevant values:

        ```
        kubectl create secret generic k8s-informer-cred-INSTANCE_NAME --from-literal=.user=USERNAME --from-literal=.password=PASSWORD -n NAMESPACE
        ```

    **Note:**

    -   If the KVA Informer connects to the ServiceNow instance through a proxy server, you can provide the proxy user and password by adding the .proxyUser and .proxyPassword keys to the secret. For example:

        ```
        kubectl create secret generic k8s-informer-cred-INSTANCE_NAME --from-literal=.user=USERNAME --from-literal=.password=PASSWORD --from-literal=.proxyUser=PROXY_USER --from-literal=.proxyPassword=PROXY_PASSWORD -n NAMESPACE.
        ```

        If you don't provide .proxyUser, KVA assumes that authentication is not needed. If you provide .proxyUser but not .proxyPassword, the system returns an error in the logs and aborts the KVA Informer.

    -   If your organization uses Amazon Elastic Kubernetes Service \(EKS\), you can store the secret in AWS Secrets Manager. The KVA Informer then pulls the ServiceNow credentials for accessing your instance from the AWS Secrets Manager. For more information, see the [Kubernetes Visibility Agent \(formerly CNO for Visibility\): Storing the instance credentials in AWS Secrets Manager \[KB1581074\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1581074) article in the Now Support Knowledge Base.
    -   If your organization uses Azure Kubernetes Service \(AKS\), you can store the secret in the Microsoft Azure Key Vault. The KVA Informer then pulls the ServiceNow credentials for accessing your instance from the Azure Key Vault. For more information, see the [Storing the instance credentials in Microsoft Azure Key Vault \[KB1647736\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1647736) article in the Now Support Knowledge Base.
    -   If your organization uses Google Kubernetes Engine \(GKE\), you can store the secret in Google Cloud Secret Manager. The KVA Informer then pulls the ServiceNow credentials for accessing your instance from the Google Cloud Secret Manager. For more information, see the [Storing credentials in Google Cloud Secret Manager \[KB1709597\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1709597) article in the Now Support Knowledge Base.
    -   If your organization uses a custom root CA \(Certificate Authority\), you can mount a custom CA into the KVA Informer pod to enable the Informer to communicate with the ServiceNow instance. For more information, see the [Using a custom root certificate authority when connecting the Informer to the instance \[KB1710906\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1710906) article in the Now Support Knowledge Base.
    -   As an alternative to basic authentication, the KVA Informer can use OAuth 2.0 authorization to connect to the ServiceNow instance for enhanced security. When the Informer uses OAuth 2.0, the instance issues an access token with an expiry time rather than requiring login credentials with each resource request. For more information, see the [Connecting Kubernetes Visibility Agent \(formerly CNO for Visibility\) using the OAuth Protocol \[KB1648198\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1648198) article in the Now Support Knowledge Base.
5.  If your organization's policy requires it, place the KVA Informer docker image in your organization’s image repository.

    **Note:** Starting in KVA version 3.9.0 \(Informer version 2.3.0\), released in November 2024, the docker image supports both arm64 and amd64 architectures. Upgrading from the previous image to the new one will not cause any disruptions. However, the new image requires more storage space in your image repository than the previous one did.

    1.  Pull the image from Docker Hub and push it to your organization’s repository.

        Replace `VERSION` with the number of the most recent release, provided in the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Helm Chart and Kubernetes YAML file releases \[KB1564347\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1564347) article in the Now Support Knowledge Base.

        ```
        Docker pull docker.io/servicenowdocker/informer:VERSION
         Docker tag docker.io/servicenowdocker/informer:VERSION COMPANY_REPO:VERSION
         Docker push COMPANY_REPO:VERSION
        ```

    2.  If the image repository requires authentication, create a secret named k8s-informer-repo-cred in the designated namespace.

        For example:

        ```
        kubectl create secret docker-registry k8s-informer-repo-cred --docker-server https://index.docker.io/v2/ --docker-username DOCKER_USERNAME --docker-password DOCKER_TOKEN --docker-email=user@servicenow.com -n NAMESPACE
        ```

6.  If outgoing traffic from your cluster flows through a proxy, identify the proxy host name and port used in your cluster.

    **Note:** Ask your organization’s Kubernetes team for this information. You need to provide it in the installation process.

7.  Enable KVA to process more data simultaneously.

    By default, the Informer’s back-end side can handle data from around 300 clusters at the same time. If you have more clusters or your clusters undergo frequent changes, you can increase the number of concurrent worker threads used for processing the data. For more information, see the [Controlling the number of "Kubernetes Visibility Agent" \(formerly CNO for Visibility\) concurrent worker threads \[KB1580241\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1580241) article in the Now Support Knowledge Base.


## Result

Your ServiceNow instance and the Kubernetes cluster are ready for KVA deployment.

## What to do next

[Install Kubernetes Visibility Agent \(KVA\) Informer](cnov-deploy-install.md).

**Parent Topic:**[Configuring Kubernetes Visibility Agent](../concept/cnov-configuring.md)

