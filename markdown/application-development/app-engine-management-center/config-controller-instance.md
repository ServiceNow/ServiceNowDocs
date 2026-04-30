---
title: Configure your controller instance
description: You must identify one of the instances in your app development pipeline as the controller instance. All communication between the instances in your pipeline, including the deployment order for applications in the pipeline, takes place in the controller instance.
locale: en-US
release: zurich
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure your controller instance

You must identify one of the instances in your app development pipeline as the controller instance. All communication between the instances in your pipeline, including the deployment order for applications in the pipeline, takes place in the controller instance.

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


