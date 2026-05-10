---
title: Instances in ReleaseOps configuration
description: Learn about the different types of instances in ReleaseOps configuration.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ReleaseOps, Deploying applications, Building applications]
---

# Instances in ReleaseOps configuration

Learn about the different types of instances in ReleaseOps configuration.

## Controller instance and managed instances

The terms controller instance and managed instances are specific to multi-instance management. ReleaseOps uses multi-instance management to handle trust configurations across instances and orchestrate deployments from a single instance. The instance that manages the other instances and orchestrates deployments is the controller instance. The other instances that the controller instance manages are the managed instances. During ReleaseOps configuration, you must add managed instances and authorize your controller instance to manage those instances.

For more information about multi-instance management, see [Cross-instance application trust configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/grant-access-v2.md). To see a complete list of managed instances, you can navigate to **All** &gt; **Multi-instance management** &gt; **Managed instances**.

## Deployment instances and pipeline instances

A deployment instance defines the environment of the instance, such as development, test, or production. During ReleaseOps configuration, deployment instances are created for each instance in your pipeline. You must define the environment type for each deployment instance.

You can view a complete list of deployment instances and their environment types by navigating to **All** &gt; **ReleaseOps** &gt; **Deployment instances**.

A pipeline instance maps a deployment instance to the pipeline that it participates in. Only intermediate instances are mapped using pipeline instances, because the source and destination instances are specified in the deployment request record and the release record respectively. For example, in a three instance \(development, test, production\) pipeline, the test instance is the only instance that must be defined with a pipeline instance.

To view a list of pipeline instances for a given pipeline, navigate to **All** &gt; **ReleaseOps** &gt; **Pipelines** and select the pipeline from the list. On the pipeline record page, select **Pipeline instances** to view the pipeline instances for the selected pipeline.

![View pipeline instances for a selected pipeline on the pipeline record page.](../image/releaseops-pipeline-instances-view.png)

## Remote instances

ReleaseOps uses update sources to move update sets between instances. A remote instance is the source instance, or update source, where an update set originates. For more information about update sources, see [Set up the source instance for an update set](../../system-update-sets/task/setting-source-for-update-set.md).

If you previously worked with update sets and have remote instances already defined, ReleaseOps can use those instances when defining remote instances during guided setup. Otherwise, you can create remote instances during the guided setup process.

