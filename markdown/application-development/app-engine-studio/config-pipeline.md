---
title: Configure your pipeline
description: Configure your App Engine Studio \(AES\) pipeline so that your administrator can quickly move an application from one environment to another.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Pipelines and Deployments configuration tasks, Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure your pipeline

Configure your App Engine Studio \(AES\) pipeline so that your administrator can quickly move an application from one environment to another.

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


**Parent Topic:**[Pipelines and Deployments configuration tasks](../reference/p-and-d-config-tasks.md)

