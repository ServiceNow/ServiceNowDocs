---
title: Enable Change Management integration
description: Enable Change Management integration with AEMC so that deployments through the pipeline to the production environment are automatically scheduled based on the Change request state and planned change window.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Pipelines and Deployments configuration tasks, Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Enable Change Management integration

Enable Change Management integration with AEMC so that deployments through the pipeline to the production environment are automatically scheduled based on the Change request state and planned change window.

## Before you begin

Role required: admin

## About this task

This task can be completed within the Guided Setup system. This task opens within Guided Setup when you select **Configure**. If you prefer, you can follow the instructions below to access the same configuration task outside of the Guided Setup.

## Procedure

1.  Navigate to the System Properties table by typing `sys_properties.list` in the navigation filter and pressing **Enter**.

2.  Locate the following property: sn\_deploy\_pipeline.change\_management.enabled.

3.  Connect your existing Change Management processes to AEMC by changing the **Value** field to `true`.

4.  Select **Update**.

5.  In the Pipelines and Deployments Guided Setup, select **Mark Complete**.

    Marking the enablement step complete enables you to configure properties related to Change Management integration including the change model, change template, and CI creation subflow. For more information, see [Configure properties to integrate Change Management](../concept/configure-properties-integrate-cm.md#).


**Parent Topic:**[Pipelines and Deployments configuration tasks](../reference/p-and-d-config-tasks.md)

