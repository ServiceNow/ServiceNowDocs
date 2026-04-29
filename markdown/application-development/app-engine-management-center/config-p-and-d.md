---
title: Configure Pipelines and Deployments
description: Use the Pipelines and Deployments guided setup to complete the initial configuration of Pipelines and Deployments. Detailed instructions for each step are provided in subsequent sections of the product documentation.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure Pipelines and Deployments

Use the Pipelines and Deployments guided setup to complete the initial configuration of Pipelines and Deployments. Detailed instructions for each step are provided in subsequent sections of the product documentation.

## Before you begin

Role required: admin

## About this task

The Pipelines and Deployments guided setup provides a sequence of tasks that help you configure Pipelines and Deployments on the ServiceNow AI Platform. For more information about each task, see [Pipelines and Deployments configuration tasks](../reference/p-and-d-config-tasks.md).

Starting with version 28.2.1 of Pipelines and Deployments, you can migrate your existing pipelines to ReleaseOps. To learn more about the migration process and the advantages of migrating to ReleaseOps, see [Migrating App Engine pipelines to ReleaseOps](../../app-engine-management-center/concept/migrating-ae-pipelines-to-releaseops-aemc.md). To get started migrating your existing pipelines, see [Migration tasks](../../app-engine-management-center/concept/migration-tasks-aemc.md).

For general information about guided setup, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Guided Setup**.

    The landing page provides information on the different categories, tools, and user access.

    ![Pipelines and Deployments guided setup landing page](../image/guided-setup-landing-page-vs2.png "Pipelines and Deployments guided setup landing page")

2.  To initiate guided setup, select **Get Started**.

    The Pipelines and Deployments Guided Setup category page provides a list of different categories of tasks you must complete before you can use Pipelines and Deployments.

    **Note:** If you have previously started any of the guided setup tasks, and then exited without completing them, the **Get Started** button will be labeled **Continue**.

    ![Pipelines and Deployments guided setup category page](../image/guided-setup-category-page-vs2.png "Pipelines and Deployments guided setup category page")

    **Important:** Each of the tasks in the following list must be performed on different environments in your pipeline.

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
    5.  [Configure Instance Scan suite](https://www.servicenow.com/docs/access?context=hs-landing-page&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    When you have completed all of the tasks in this category, the Guided Setup screen reappears.

5.  Select the last **Get Started** button to begin performing tasks for all of the other non-production \(that is, test, development, staging, and so forth\) instances in your pipeline.

    1.  [Configure environment credentials](create-pipeline-credentials.md).
    2.  [Configure your controller instance](config-controller-instance.md).
    Congratulations! You have completed guided setup for the Pipelines and Deployments application.

6.  Migrate your existing pipelines to ReleaseOps.

    See [Migration tasks](../../app-engine-management-center/concept/migration-tasks-aemc.md) for more information.


