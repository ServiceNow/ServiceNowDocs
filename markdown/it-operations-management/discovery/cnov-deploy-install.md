---
title: Install Kubernetes Visibility Agent \(KVA\)
description: You can install Kubernetes Visibility Agent using either a Helm chart or the Kubernetes YAML file.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Agent Client Collector, Kubernetes, Visibility, installation, deployment, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Install Kubernetes Visibility Agent \(KVA\)

You can install Kubernetes Visibility Agent using either a Helm chart or the Kubernetes YAML file.

## Before you begin

Role required: none

## About this task

This procedure describes the standard Kubernetes Visibility Agent installation process. Typically, you would use a Helm chart to perform the installation, but you can also configure and run the Kubernetes YAML file provided by ServiceNow.

## Procedure

1.  Install Kubernetes Visibility Agent using either a Helm chart or the Kubernetes YAML file provided by ServiceNow.

    -   Install Kubernetes Visibility Agent using a Helm chart.

        1.  Edit the Helm install command.
            1.  In the following command, replace NAMESPACE, INSTANCE\_NAME, and CLUSTER\_NAME with the relevant values and replace the HELM\_URL with the URL of the most recent version, provided in the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Helm Chart and Kubernetes YAML file releases \[KB1564347\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1564347) article in the Now Support Knowledge Base.

                ```
                helm install -n NAMESPACE --set acceptEula=Y --set instance.name=INSTANCE_NAME --set clusterName="CLUSTER_NAME" {--set image.repository=COMPANY_REPO --set image.tag=COMPANY_TAG} {--set proxyUrl=http://proxy_host:proxy_port} k8s-informer HELM_URL
                ```

                **Note:**

                -   The curly brackets indicate that the code segments they surround are optional. Use these code segments if the image must be pulled from your organization’s image repository or if outgoing traffic from your cluster flows through a proxy.
                -   By passing `--set acceptEula=Y`, you agree to the End-User License Agreement. You can read the End-User License Agreement by extracting the EULA.pdf from informer-helm-&lt;VERSION\_NUMBER&gt;.tgz.
                -   If the Informer is installed in OpenShift, add the **openShift** parameter to the command and set it to `true`:

                    ```
                    helm install -n NAMESPACE --set acceptEula=Y --set instance.name=INSTANCE_NAME --set clusterName="CLUSTER_NAME" {--set image.repository=COMPANY_REPO --set image.tag=COMPANY_TAG} {--set proxyUrl=http://proxy_host:proxy_port} **\{--set openShift=true\}** k8s-informer HELM_URL
                    ```

                    **Note:** If the Informer is not installed in OpenShift, there is no need to set this parameter.

                -   If you use the Hybrid service maps to map resources both inside and outside the Kubernetes cluster, set the following parameters:

                    ```
                    --set bringIngressAddresses=true --set bringNodeExternalIPs=true --set discoverK8sServiceExternalIps=true --set openShift=true
                    ```

            2.  In the command, configure additional settings as needed:
                -   [Configure the memory limit of the Informer pod](cnov-config-informer-memory.md)
                -   [Change the full discovery frequency in Kubernetes Visibility Agent](cnov-config-full-discovery-frequency.md)
                -   [Deactivate continuous discovery in Kubernetes Visibility Agent](cnov-config-continuous-discovery-off.md)
                -   Suppress frequent changes in the Kubernetes cluster to reduce the load on your instance. When this feature is active, the Informer does not report changes above the configured threshold rate back to the instance. For more information, see the [Suppressing frequent changes in Kubernetes clusters reported by Kubernetes Visibility Agent \(formerly CNO for visibility\) \[KB1580745\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1580745) article in the Now Support Knowledge Base.
                -   Control the maximum number of full discoveries that informers can run on multiple clusters at the same time. For more information, see the [Scheduling Full Discoveries in Kubernetes Visibility Agent \(formerly CNO for Visibility\) \[KB1580250\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1580250) article in the Now Support Knowledge Base.
                -   [Enabling application service maps](../concept/enabling-application-service-maps.md)
        2.  Run the command.
    -   Install Kubernetes Visibility Agent using the Kubernetes YAML file.
        1.  Download the Kubernetes YAML zip file provided in the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Helm Chart and Kubernetes YAML file releases \[KB1564347\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1564347) article in the Now Support Knowledge Base.
        2.  Extract the k8s\_informer.yaml and EULA.pdf files from the zip file.
        3.  Edit the k8s\_informer.yaml file.
            -   Change the value of ACCEPT\_EULA to `"Y"`, as follows:

                ```
                - name: ACCEPT_EULA
                  value: "Y"
                ```

                **Note:** By changing the value to `"Y"`, you agree to the End-User License Agreement included in the EULA.pdf file.

            -   Replace all occurrences of &lt;NAMESPACE&gt; with the namespace in which you want to install the Informer.
            -   Replace all occurrences of &lt;INSTANCE\_NAME&gt; with the name of your instance, without the domain name.
            -   Replace &lt;CLUSTER\_NAME&gt; with the name of your cluster as it appears in the CMDB.
            -   If the Informer is installed in OpenShift, change the value of the OPENSHIFT environment variable to `true`.
            -   [Enabling application service maps](../concept/enabling-application-service-maps.md)
        4.  If you use the Hybrid service maps to map resources both inside and outside the Kubernetes cluster, set the following parameters:

            ```
            - name: BRING_INGRESS_ADDRESSES value: "true" - name: BRING_NODE_EXTERNAL_IPS value: "true" - name: DISCOVER_K8S_SERVICE_EXTERNAL_IP value: "true" - name: OPENSHIFT value: "true" 
            ```

        5.  Run the command:

            ```
            kubectl apply -f k8s_informer.yaml
            ```


## Result

Kubernetes Visibility Agent is deployed on the Kubernetes cluster and begins to stream data into your instance.

## What to do next

For information about Kubernetes Visibility Agent administration and troubleshooting, see the [Administrating and Troubleshooting Kubernetes Visibility Agent \(formerly CNO for Visibility\) \[KB1532614\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1532614) article in the Now Support Knowledge Base.

-   **[Configure the memory limit of the Informer pod](cnov-config-informer-memory.md)**  
Set the memory limit of the Kubernetes Visibility Agent Informer pod.
-   **[Change the full discovery frequency in Kubernetes Visibility Agent](cnov-config-full-discovery-frequency.md)**  
Customize how often you want the Kubernetes Visibility Agent Informer to run a full discovery.
-   **[Deactivate continuous discovery in Kubernetes Visibility Agent](cnov-config-continuous-discovery-off.md)**  
Switch off continuous discovery by Kubernetes Visibility Agent if all you need is periodic snapshots of your cluster resources. If you have multiple clusters with frequent changes, deactivating continuous discovery reduces the load on your instance.
-   **[Display the Kubernetes cluster version in the CMDB](cnov-config-see-cluster-version.md)**  
Make the Kubernetes Visibility Agent Informer populate the relevant field in the cmdb\_ci\_kubernetes\_cluster CI to display the Kubernetes cluster version.
-   **[Create a cmdb\_ci\_linux\_server CI for each Kubernetes node](cnov-config-linux-server-ci.md)**  
Configure if you want the Kubernetes Visibility Agent Informer to create a cmdb\_ci\_linux\_server CI for each Kubernetes node.
-   **[Retain inactive namespace CIs for audits](remove-inactive-cis.md)**  
If required by your corporate standards, retain inactive namespace configuration items \(CIs\) for reference and auditing purposes with the option to delete them manually later.
-   **[Define include and exclude lists of Labels and Annotations](cnov-config-annotations-allowed.md)**  
In Kubernetes Visibility Agent, define include and exclude lists of Labels and Annotations in Kubernetes resources that the Informer pulls into the Configuration Management Database \(CMDB\).
-   **[Add custom Labels and Annotations to Kubernetes resources](cnov-config-add-custom-labels.md)**  
Add custom Labels and Annotations to all resources deployed by Kubernetes Visibility Agent in the Kubernetes cluster.
-   **[Upgrade Kubernetes Visibility Agent Informers remotely](cnov-informer-upgrade-remote.md)**  
Upgrade Kubernetes Visibility Agent Informer pods in Kubernetes clusters remotely from the ServiceNow Instance to avoid dependence on your Kubernetes admin. You can upgrade a single Informer or multiple Informers together.
-   **[Override Informer parameters from the Instance](cnov-params-override.md)**  
Control Kubernetes Visibility Agent Informer execution parameters from the ServiceNow Instance to avoid dependence on your Kubernetes admin.

**Parent Topic:**[Configuring Kubernetes Visibility Agent](../concept/cnov-configuring.md)

