---
title: Override Informer parameters from the Instance
description: Control Kubernetes Visibility Agent Informer execution parameters from the ServiceNow Instance to avoid dependence on your Kubernetes admin.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, Informer, settings, override, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\), Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Override Informer parameters from the Instance

Control Kubernetes Visibility Agent Informer execution parameters from the ServiceNow Instance to avoid dependence on your Kubernetes admin.

## Before you begin

Role required: discovery\_admin

## About this task

The Informer execution parameters are configured during deployment using the Kubernetes Yaml file or the Helm command. If you need to change these settings later, you can do so directly from the Instance without having to ask your Kubernetes team to update or reinstall the deployment.

When you add or modify a parameter, it is synchronized with the informer through the ECC Queue. Depending on the parameter, the Informer pod may need to restart. Parameters requiring a restart must have the SELF\_PATCHING\_ALLOWED environment variable set to true for changes to be effective upon restart. If this variable is set to false, the Informer is not restarted and continues to use the old values.

**Note:** Informer-specific parameters only affect a specific Informer. If you add a parameter without assigning it to an Informer, it defaults to a global parameter and affects all Informers in the system. When both global and Informer-specific parameters are present, Informer-specific parameters take precedence.

You can update the following parameters from the Instance:

|Parameter|Restart upon change|
|---------|-------------------|
|VERBOSE\_LOGGING|No|
|OPENSHIFT|Yes|
|CREATE\_SERVER\_CI|No|
|INCLUDE\_LABELS\_AND\_ANNOTATIONS|No|
|EXCLUDE\_LABELS\_AND\_ANNOTATIONS|No|
|FULL\_DISCOVERY\_MIN|Yes|
|SEND\_INTERVAL\_SEC|Yes|
|CONTINUOUS\_DISCOVERY|Yes|
|CLUSTER\_RESOURCE\_ID|No|
|CLUSTER\_NAME|No|

For information about the purpose of each parameter, see the [Kubernetes Visibility Agent \(formerly CNO for Visibility\) Advanced Configuration Options \[KB1648891\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1648891) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **Kubernetes Visibility Agent** &gt; **Configuration Parameters**.

2.  Select a parameter in the **Kubernetes Informer Parameters** list.

3.  Change the configured value as needed, and then select **Update**.


**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\)](cnov-deploy-install.md)

