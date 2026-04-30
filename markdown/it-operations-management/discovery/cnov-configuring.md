---
title: Configuring Kubernetes Visibility Agent
description: Set up Kubernetes Visibility Agent by performing the described procedures.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, configuration, settings, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Configuring Kubernetes Visibility Agent

Set up Kubernetes Visibility Agent by performing the described procedures.

For information about advanced configuration options, see the [Administrating and Troubleshooting Kubernetes Visibility Agent \(formerly CNO for Visibility\) \[KB1532614\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1532614) article in the Now Support Knowledge Base.

-   **[Prepare for Kubernetes Visibility Agent deployment](../task/cnov-deploy-prepare.md)**  
Prepare your ServiceNow instance and the Kubernetes cluster for Kubernetes Visibility Agent deployment.
-   **[Install Kubernetes Visibility Agent \(KVA\)](../task/cnov-deploy-install.md)**  
You can install Kubernetes Visibility Agent using either a Helm chart or the Kubernetes YAML file.
-   **[Enabling application service maps](enabling-application-service-maps.md)**  
Service maps map application services based on traffic between the workloads in Kubernetes using Istio or Linkerd service meshes or a ServiceNow DaemonSet, and sends that information to the ServiceNow instance.
-   **[Pulling additional resources from Kubernetes clusters into the CMDB](cnov-config-pulling-extra-resources.md)**  
You can configure the Kubernetes Visibility Agent Informer to pull extra resources from Kubernetes clusters into the Configuration Management Database \(CMDB\), in addition to the resources it sends to the database by default. By pulling in additional resources beyond the default set, you can enhance visibility into your Kubernetes clusters.
-   **[Upgrade Kubernetes Visibility Agent](../task/acckv-upgrade.md)**  
You can upgrade Kubernetes Visibility Agent using either a Helm chart or the Kubernetes YAML file.

**Parent Topic:**[Kubernetes Visibility Agent](../../agent-client-collector/concept/acc-kubernetes-visibility-landing-page.md)

