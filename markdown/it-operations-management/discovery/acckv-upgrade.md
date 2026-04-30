---
title: Upgrade Kubernetes Visibility Agent
description: You can upgrade Kubernetes Visibility Agent using either a Helm chart or the Kubernetes YAML file.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Agent Client Collector, Kubernetes, Visibility, upgrading, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Upgrade Kubernetes Visibility Agent

You can upgrade Kubernetes Visibility Agent using either a Helm chart or the Kubernetes YAML file.

## Before you begin

Role required: none

## About this task

This procedure describes the standard Kubernetes Visibility Agent upgrade process. Typically, you would use a Helm chart to perform the upgrade. Alternatively, you can upgrade Kubernetes Visibility Agent by configuring and running the Kubernetes YAML file provided by ServiceNow. In both cases, there is no need to uninstall before upgrading.

You can also upgrade Kubernetes Visibility Agent Informer pods in Kubernetes clusters remotely from the ServiceNow Instance. For more information, see [Upgrade Kubernetes Visibility Agent Informers remotely](cnov-informer-upgrade-remote.md).

## Procedure

1.  Upgrade Kubernetes Visibility Agent using either a Helm chart or the Kubernetes YAML file provided by ServiceNow.

    -   Upgrade Kubernetes Visibility Agent using a Helm chart.

        1.  Edit the Helm upgrade command.
            1.  In the following command, replace NAMESPACE, INSTANCE\_NAME, and CLUSTER\_NAME with the relevant values and replace the HELM\_URL with the URL of the most recent version, provided in the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Helm Chart and Kubernetes YAML file releases \[KB1564347\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1564347) article in the Now Support Knowledge Base.

                ```
                helm upgrade -n NAMESPACE --set acceptEula=Y --set instance.name=INSTANCE_NAME --set clusterName="CLUSTER_NAME" {--set image.repository=COMPANY_REPO --set image.tag=COMPANY_TAG} {--set proxyUrl=http://proxy_host:proxy_port} k8s-informer HELM_URL
                ```

                **Note:**

                -   The curly brackets indicate that the code segments they surround are optional. Use these code segments if the image must be pulled from your organization’s image repository or if outgoing traffic from your cluster flows through a proxy.
                -   By passing `--set acceptEula=Y`, you agree to the End-User License Agreement. You can read the End-User License Agreement by extracting the EULA.pdf from informer-helm-&lt;VERSION\_NUMBER&gt;.tgz.
                -   If the Informer is installed in OpenShift, add the **openShift** parameter to the command and set it to `true`:

                    ```
                    helm upgrade -n NAMESPACE --set acceptEula=Y --set instance.name=INSTANCE_NAME --set clusterName="CLUSTER_NAME" {--set image.repository=COMPANY_REPO --set image.tag=COMPANY_TAG} {--set proxyUrl=http://proxy_host:proxy_port} **\{--set openShift=true\}** k8s-informer HELM_URL
                    ```

                    **Note:** If the Informer is not installed in OpenShift, there is no need to set this parameter.

            2.  In the command, configure additional settings as needed:
                -   [Configure the memory limit of the Informer pod](cnov-config-informer-memory.md)
                -   [Change the full discovery frequency in Kubernetes Visibility Agent](cnov-config-full-discovery-frequency.md)
                -   [Deactivate continuous discovery in Kubernetes Visibility Agent](cnov-config-continuous-discovery-off.md)
                -   Suppress frequent changes in the Kubernetes cluster to reduce the load on your instance. When this feature is active, the Informer does not report changes above the configured threshold rate back to the instance. For more information, see the [Suppressing frequent changes in Kubernetes clusters reported by Kubernetes Visibility Agent \(formerly CNO for visibility\) \[KB1580745\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1580745) article in the Now Support Knowledge Base.
                -   Control the maximum number of full discoveries that Informers can run on multiple clusters at the same time. For more information, see the [Scheduling Full Discoveries in Kubernetes Visibility Agent \(formerly CNO for Visibility\) \[KB1580250\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1580250) article in the Now Support Knowledge Base.
        2.  Run the command.
    -   Upgrade Kubernetes Visibility Agent using the Kubernetes YAML file.
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
        4.  Run the command:

            ```
            kubectl apply -f k8s_informer.yaml
            ```


## What to do next

For information about Kubernetes Visibility Agent administration and troubleshooting, see the [Administrating and Troubleshooting Kubernetes Visibility Agent \(formerly CNO for Visibility\) \[KB1532614\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1532614) article in the Now Support Knowledge Base.

**Parent Topic:**[Configuring Kubernetes Visibility Agent](../concept/cnov-configuring.md)

