---
title: Configure the App Engine Management Center
description: Use the App Engine Management Center \(AEMC\) guided setup to step through the initial configuration of the Application Intake and Pipelines and Deployments applications. The Application Intake guided setup is optional, but if you want to use AEMC, the Pipelines and Deployments guided setup is required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/app-engine-management-center/configure-aemc.html
release: zurich
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure the App Engine Management Center

Use the App Engine Management Center \(AEMC\) guided setup to step through the initial configuration of the Application Intake and Pipelines and Deployments applications. The Application Intake guided setup is optional, but if you want to use AEMC, the Pipelines and Deployments guided setup is required.

## Before you begin

Role required: admin

Ensure that AEMC is installed on your production instance and all of your non-production instances \(development, test, and the like\).

## About this task

Essentially, the AEMC guided setup contains the setup steps for both the Application Intake and Pipelines and Deployments applications. If you have already configured one or both of these applications, you can skip those steps within the guided setup.

## Procedure

1.  On your production instance, navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **Guided Setup**.

    The landing page provides information on the two applications that you must configure, Application Intake and Pipelines and Deployments.

    \[Omitted image "aemc-guided-setup-landing.png"\] Alt text: AEMC Guided setup landing page

2.  Initiate guided setup by selecting **Get Started**.

    The App Engine Management Center guided setup category page provides a list of different categories of tasks that you must complete before you can use AEMC.

    \[Omitted image "aemc-guided-setup-two-apps.png"\] Alt text: AEMC Guided Setup category page

    **Note:** If you have previously started any of the guided setup tasks, and then exited without completing them, the **Get Started** button is labeled **Continue**.

3.  Select the first **Get Started** button to initiate the Application Intake Guided Setup.

    There are several [Application Intake configuration tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/app-intake-config-tasks.md) you must complete.

    1.  [Activate the Apply for Citizen Development catalog item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/activate-catalog-item-for-app-intake.md).
    2.  [Add users to the App Engine Admin group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-studio/add-users-to-admin-grp.md).
    3.  [Create development environment records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/config-pipeline-environments.md).
    When you've completed all of the tasks in this category, the Category screen reopens.

4.  Select the next **Get Started** button to initiate the Pipelines and Deployments Guided Setup.

    There are several [Pipelines and Deployments configuration tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/p-and-d-config-tasks.md) you must complete.

    On your production instance:

    1.  [Configure environment credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/create-pipeline-credentials.md).
    2.  [Configure your pipeline environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/config-pipeline-environments.md).
    3.  [Configure your pipeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/config-pipeline.md).
    4.  [Add users to the App Engine Admin group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-studio/add-users-to-admin-grp.md).
    5.  [Add ATF and instance scan suites for testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/add-atf-instance-scan-suite-testing.md).

        **Note:** You can add ATF and instance scan suites for testing only if you've already created them and set up your testing instance. If you have not done this yet, you must come back to this step.

    6.  [Enable Change Management integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/enable-change-management-integration.md).
    7.  [Configure properties to integrate Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/configure-properties-integrate-cm.md).
    On your testing instance:

    1.  [Configure environment credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/create-pipeline-credentials.md).
    2.  [Configure your controller instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/config-controller-instance.md).
    3.  [Enable Automated Test Framework \(ATF\) properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/enable-atf-properties.md).
    4.  [Configure Automated Test Framework \(ATF\) suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/automated-test-framework-atf/automated-test-framework.md).
    5.  [Configure Instance Scan suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/instance-scan/hs-landing-page.md).
    On your other, non-production instances:

    1.  [Configure environment credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/create-pipeline-credentials.md).
    2.  [Configure your controller instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-management-center/config-controller-instance.md).
    When you have completed the tasks in the second category, the Category page reappears. You have completed guided setup for App Engine Management Center.

5.  Configure additional properties used to control system behavior in AEMC.


