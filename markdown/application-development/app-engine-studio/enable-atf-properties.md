---
title: Enable Automated Test Framework \(ATF\) properties
description: The App Engine Studio \(AES\) Pipelines and Deployments app includes an Application Test Framework \(ATF\) suite called the Application Deployment Test Suite. Two system properties control whether the test runs automatically whenever an app is deployed to a Test environment.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Pipelines and Deployments configuration tasks, Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Enable Automated Test Framework \(ATF\) properties

The App Engine Studio \(AES\) Pipelines and Deployments app includes an Application Test Framework \(ATF\) suite called the Application Deployment Test Suite. Two system properties control whether the test runs automatically whenever an app is deployed to a Test environment.

## Before you begin

Role required: admin

## About this task

The tests in the Application Deployment Test Suite can be run on production instances; however, the flows included in the base system run only on non-production \(Test\) instances. Additionally, the tests should run only on an instance defined with an **Instance Type** of **Testing**. For more information, see [Configure your pipeline environments](config-pipeline-environments.md).

**Note:** If you plan on cloning your production instance to one or more non-production instances, you should either create a data preserver for these settings or enable these settings on your production instance. For more information, see [System clone](https://www.servicenow.com/docs/access?context=c_SystemClone&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to the System Properties table by typing `sys_properties.list` in the navigation filter and pressing **Enter**.

2.  Locate the following two properties:

    -   sn\_atf.runner.enabled
    -   sn\_atf.schedule.enabled
3.  If you want these tests to run automatically on non-production instances whenever an app is deployed to a Test instance, open each property record, change the **Value** field to true, and select **Update**.


**Parent Topic:**[Pipelines and Deployments configuration tasks](../reference/p-and-d-config-tasks.md)

