---
title: Configure your controller instance
description: You must identify one of the instances in your App Engine Studio \(AES\) pipeline as the controller instance. All communication between the instances in your pipeline, including the deployment order for applications in the pipeline, takes place in the controller instance.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Pipelines and Deployments configuration tasks, Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure your controller instance

You must identify one of the instances in your App Engine Studio \(AES\) pipeline as the controller instance. All communication between the instances in your pipeline, including the deployment order for applications in the pipeline, takes place in the controller instance.

## Before you begin

Role required: admin

## About this task

Typically, your production instance should be identified as the controller instance. All request and approval records are stored on your controller instance.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Environments**.

2.  When you are [configuring your pipeline environments](config-pipeline-environments.md), decide which instance you want to use as the controller, and select the **Is Controller?** check box for that instance.

    ![Is Controller? field](../image/controller-instance-purple.png)

3.  Select **Save**.

    When the workflow for the pipeline runs, the non-production instances communicate with the controller instance to determine to which instance the app should next be deployed.


**Parent Topic:**[Pipelines and Deployments configuration tasks](../reference/p-and-d-config-tasks.md)

