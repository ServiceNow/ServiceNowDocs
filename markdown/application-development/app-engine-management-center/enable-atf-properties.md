---
title: Enable Automated Test Framework \(ATF\) properties
description: Pipelines and Deployments includes an Application Test Framework \(ATF\) suite called the Application Deployment Test Suite. Two system properties control whether the test runs automatically whenever an app is deployed to a Test environment.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Enable Automated Test Framework \(ATF\) properties

Pipelines and Deployments includes an Application Test Framework \(ATF\) suite called the Application Deployment Test Suite. Two system properties control whether the test runs automatically whenever an app is deployed to a Test environment.

## Before you begin

Role required: admin

## About this task

The tests in the Application Deployment Test Suite can be run on production instances; however, the flows included in the base system run only on non-production \(Test\) instances. Additionally, the tests should run only on an instance defined with an **Instance Type** of **Testing**. For more information, see [Configure your pipeline environments](config-pipeline-environments.md).

**Note:** If you plan on cloning your production instance to one or more non-production instances, you should either create a data preserver for these settings or enable these settings on your production instance. For more information, see Create a clone preserver.

## Procedure

1.  Navigate to the System Properties table by typing `sys_properties.list` in the navigation filter and pressing **Enter**.

2.  Locate the following two properties:

    -   sn\_atf.runner.enabled
    -   sn\_atf.schedule.enabled
3.  If you want these tests to run automatically on non-production instances whenever an app is deployed to a Test instance, open each property record, change the **Value** field to true, and select **Update**.


