---
title: Test App Engine Management Center functionality on a non-production instance
description: Test App Engine Management Center \(AEMC\) on a non-production instance to confirm that everything is working as expected before moving to production.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the App Engine Management Center, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Test App Engine Management Center functionality on a non-production instance

Test App Engine Management Center \(AEMC\) on a non-production instance to confirm that everything is working as expected before moving to production.

## Before you begin

Role required: admin

## About this task

To test AEMC and pipelines before you proceed to a production environment, pick two non-production instances for testing purposes. Follow the Pipelines and Deployments guided setup as if one of those non-production instances is a production instance. Because the system doesn't verify that the instance type on the environment record is actually a production instance, you can set the instance type to **Production** for the second non-production instance.

## Procedure

1.  Begin the Pipelines and Deployments Guided setup tasks as detailed in [Pipelines and Deployments configuration tasks](../../pipelines-and-deployments/reference/p-and-d-config-tasks.md).

2.  When you begin the tasks to configure your pipeline environments, select one of your non-production instances and designate it as a production instance in the pipeline environment record.

    For more information on the usual process, see [Configure your pipeline environments](../../pipelines-and-deployments/task/config-pipeline-environments.md).

3.  Test AEMC and your pipeline functionality.

4.  When you're done testing, change the **Instance type** of the non-production pipeline environment record to the correct type of instance.


**Parent Topic:**[Configure the App Engine Management Center](configure-aemc.md)

