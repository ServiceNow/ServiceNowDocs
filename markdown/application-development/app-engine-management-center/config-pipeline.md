---
title: Configure your pipeline
description: Configure your app development pipeline so that your administrator can quickly move an application from one environment to another.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure your pipeline

Configure your app development pipeline so that your administrator can quickly move an application from one environment to another.

## Before you begin

You must create all of your pipeline environment records before completing these steps. For more information, see [Configure your pipeline environments](config-pipeline-environments.md).

Role required: admin or app\_engine\_admin

## Procedure

1.  In your production instance, navigate to **All** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Pipelines**.

2.  Select **New**.

    ![Creating a new pipeline record](../image/new-pipeline-purple.png "Pipeline - new record")

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the pipeline. Enter a name that distinguishes this pipeline from other pipelines.|
    |Pipeline Type|The type of pipeline you are defining. The most common use case for pipelines is to select Application Deployment; however, you can define other types as needed.|
    |Source Environment|The environment for this pipeline, usually the development environment.|
    |Application|Application scope of the pipeline.|
    |Active|Select the check box to activate this pipeline.|

4.  Select **Submit**.

5.  Reopen the pipeline record you just created.

6.  In the Pipeline Environments Order section, select the environments in the pipeline, excluding the **Source Environment**, and specify the order in which apps should be deployed through the pipeline.

7.  Select **Update**.


