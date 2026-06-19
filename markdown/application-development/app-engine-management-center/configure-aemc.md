---
title: Configure the App Engine Management Center
description: Complete AEMC guided setup to initially configure Application Intake and your preferred deployment option \(Pipelines and Deployments, ReleaseOps, or a standalone environment\). The Application Intake guided setup is optional, but setup of one of the deployment options is required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/app-engine-management-center/configure-aemc.html
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure the App Engine Management Center

Complete AEMC guided setup to initially configure Application Intake and your preferred deployment option \(Pipelines and Deployments, ReleaseOps, or a standalone environment\). The Application Intake guided setup is optional, but setup of one of the deployment options is required.

## Before you begin

Role required: admin

Verify that AEMC is installed on your production instance and all of your non-production instances \(development, test, etc.\).

## About this task

AEMC guided setup contains the setup steps for Application Intake and the deployment application options: Pipelines and Deployments, ReleaseOps, or a standalone environment. If you have already configured one or any of these applications, you can skip those steps within the guided setup.

## Procedure

1.  On your production instance, navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **Guided Setup**.

    The landing page provides information on the applications that you must configure: Application Intake, ReleaseOps, and Pipelines and Deployments.

    \[Omitted image "aemc-guided-setup-as2.png"\] Alt text: AEMC guided setup landing page, with cards for setting up Application Intake, ReleaseOps, and Pipelines and Deployments

2.  Initiate guided setup by selecting **Get Started**.

    The App Engine Management Center guided setup category page provides a list of different categories of tasks that you must complete before you can use AEMC.

    \[Omitted image "aemc-guided-setup-3-apps-as2.png"\] Alt text: AEMC Guided Setup category page

    **Note:** If you have previously started any of the guided setup tasks, and then exited without completing them, the **Get Started** button is labeled **Continue**.

3.  Select the first **Get Started** button to initiate the Application Intake Guided Setup.

    There are several [Application Intake configuration tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/app-intake-config-tasks.md) you must complete.

    1.  [Activate the Apply for Citizen Development catalog item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/activate-catalog-item-for-app-intake.md).
    2.  [Add users to the App Engine Admin group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/add-users-to-admin-grp.md).
    3.  [Create development environment records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/config-pipeline-environments.md).
    When you've completed all of the tasks in this category, the Category screen reopens.

4.  Select the **Get Started** button for either ReleaseOps or Pipelines and Deployments guided setup.

    -   If you select **Get started** for ReleaseOps, you complete several [ReleaseOps configuration tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/configure-releaseops-in-aemc.md).
    -   If you select **Get started** for Pipelines and Deployments, you complete several [Pipelines and Deployments configuration tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/config-p-and-d.md).
    When you have completed the tasks for either deployment option, the Category page reappears. You have completed guided setup for App Engine Management Center.

5.  Configure additional properties used to control system behavior in AEMC.


