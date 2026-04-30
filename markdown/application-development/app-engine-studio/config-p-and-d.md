---
title: Configure Pipelines and Deployments
description: Use the App Engine Studio \(AES\) Pipelines and Deployments guided setup to step through the initial configuration of Pipelines and Deployments. Detailed instructions for each step are provided in subsequent sections of the product documentation.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure Pipelines and Deployments

Use the App Engine Studio \(AES\) Pipelines and Deployments guided setup to step through the initial configuration of Pipelines and Deployments. Detailed instructions for each step are provided in subsequent sections of the product documentation.

## Before you begin

Role required: admin

## About this task

The Pipelines and Deployments guided setup provides a sequence of tasks that help you configure Pipelines and Deployments on the ServiceNow AI Platform. For more information on each task, see [Pipelines and Deployments configuration tasks](../reference/p-and-d-config-tasks.md).

For general information about guided setup, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Guided Setup**.

    The landing page provides information on the different categories, tools, and user access.

    ![Pipelines and Deployments guided setup landing page](../image/guided-setup-landing-page-vs2.png "Pipelines and Deployments guided setup landing page")

2.  To initiate guided setup, select **Get Started**.

    The Pipelines and Deployments Guided Setup category page provides a list of different categories of tasks you must complete before you can use Pipelines and Deployments.

    **Note:** If you have previously started any of the guided setup tasks, and then exited without completed them, the **Get Started** button will be labeled **Continue**.

    ![Pipelines and Deployments guided setup category page](../image/guided-setup-category-page-vs2.png "Pipelines and Deployments guided setup category page")

    **Important:** Please be aware that each of the categories of tasks shown here are to be performed on different environments in your pipeline.

3.  Select the first **Get Started** button to begin performing configuration tasks on your production environment.

    1.  [Configure environment credentials](create-pipeline-credentials.md).
    2.  [Configure your pipeline environments](config-pipeline-environments.md).
    3.  [Configure your pipeline](config-pipeline.md).
    4.  [Add users to the App Engine Admin group](../../app-engine-studio/task/add-users-to-admin-grp.md).
    5.  [Add ATF and instance scan suites for testing](../../app-engine-studio/task/add-atf-instance-scan-suite-testing.md).

        **Note:** You can add ATF and instance scan suites for testing only if you've already created them and set up your testing instance. If you have not done this yet, you must come back to this step.

    6.  [Enable Change Management integration](enable-change-management-integration.md).
    7.  [Configure properties to integrate Change Management](../concept/configure-properties-integrate-cm.md#).
    When you have completed all of the tasks in this category, the Guided Setup screen reappears.

4.  Select the next **Get Started** button to begin performing configuration tasks on your testing environment.

    1.  [Configure environment credentials](create-pipeline-credentials.md).
    2.  [Configure your controller instance](config-controller-instance.md).
    3.  [Enable Automated Test Framework \(ATF\) properties](enable-atf-properties.md).
    4.  [Configure Automated Test Framework \(ATF\) suite](../../../administer/auto-test-framework/concept/automated-test-framework.md).
    5.  [Configure Instance Scan suite](https://www.servicenow.com/docs/access?context=hs-landing-page&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
    When you have completed all of the tasks in this category, the Guided Setup screen reappears.

5.  Select the last **Get Started** button to begin performing tasks for all of the other non-production \(that is, test, development, staging, and so forth\) instances in your pipeline.

    1.  [Configure environment credentials](create-pipeline-credentials.md).
    2.  [Configure your controller instance](config-controller-instance.md).
    Congratulations! You have completed guided setup for the Pipelines and Deployments application.


-   **[Pipelines and Deployments configuration tasks](../reference/p-and-d-config-tasks.md)**  
As you work through the Pipelines and Deployments guided setup, you must perform different configuration tasks on each of your instances.

**Parent Topic:**[Configuring App Engine Studio and related apps](../../app-engine-studio/concept/aes-setup.md)

