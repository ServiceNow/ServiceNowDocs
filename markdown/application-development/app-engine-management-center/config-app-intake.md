---
title: Configure Application Intake
description: Use the App Engine Studio \(AES\) Application Intake guided setup to step through the initial configuration of the Application Intake application. Detailed instructions for each step are provided in subsequent sections of the product documentation.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure Application Intake

Use the App Engine Studio \(AES\) Application Intake guided setup to step through the initial configuration of the Application Intake application. Detailed instructions for each step are provided in subsequent sections of the product documentation.

## Before you begin

Before you can use Application Intake to submit application ideas, you must ensure that the [App Engine Studio application is installed](install-aes.md).

Role required: admin

## About this task

Application Intake guided setup provides a sequence of tasks that help you configure the Application Intake app on the ServiceNow AI Platform. For more information on each task, see [Application Intake configuration tasks](../reference/app-intake-config-tasks.md).

For general information about guided setup, see [Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/guided-setup.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Application Intake** &gt; **Guided Setup**.

    The landing page provides information on the different categories, tools, and user access.

    ![App Intake guided setup landing page](../image/app-intake-gs-landing-pg.png "Application Intake guided setup landing page")

2.  To initiate guided setup, select **Get Started**.

    The Application Intake Guided Setup page provides a list of different tasks you must complete before you can use Application Intake to submit requests.

    ![App Intake guided setup tasks](../image/app-intake-gs-tasks.png "Application Intake guided setup category page")

    **Note:** If you have previously started any of the guided setup tasks, and then exited without completed them, the **Get Started** button is labeled **Continue**.

3.  Select the first **Get Started** button to initiate the Application Intake Guided Setup.

    There are several [Application Intake configuration tasks](../reference/app-intake-config-tasks.md) you must complete.

    1.  [Activate the Apply for Citizen Development catalog item](activate-catalog-item-for-app-intake.md).
    2.  [Add users to the App Engine Admin group](add-users-to-admin-grp.md).
    When you've completed all of the tasks in this category, the Category screen reopens.

4.  Select the next **Get Started** button to begin performing tasks for configuring development environments for your users.

    On your production instance, [Create development environment records](../../pipelines-and-deployments/task/config-pipeline-environments.md) for each development instance that you want to provision users to. This process allows your production instance to connect to your development instances.

    **Note:** If these records have already been set up in the Pipelines and Deployments Guided Setup, you can skip this step. When you have completed the tasks in the second category, the Category screen reappears.

    Congratulations! You have completed guided setup for Application Intake.


