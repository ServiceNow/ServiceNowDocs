---
title: Configure a standalone environment
description: With App Engine Management Center \(AEMC\), you no longer need an active deployment pipeline to get started. Complete the standalone environment setup to start deploying changes quickly. You can add a pipeline later when you're ready to automate deployments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/app-engine-management-center/configure-standalone.html
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-06-03"
reading_time_minutes: 2
keywords: [standalone, environment setup, without pipeline]
breadcrumb: [Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure a standalone environment

With App Engine Management Center \(AEMC\), you no longer need an active deployment pipeline to get started. Complete the standalone environment setup to start deploying changes quickly. You can add a pipeline later when you're ready to automate deployments.

## Before you begin

Role required: admin

Related tasks:

-   [Configure environment credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/create-pipeline-credentials.md)
-   [Configure your pipeline environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/config-pipeline-environments.md)

## About this task

The standalone configuration option enables you to set up AEMC without having to configure an active deployment pipeline. Configure your development environment first, then production, and optionally your testing environment. You can add a pipeline later when you're ready to automate deployments.

For general information about guided setup, see [Using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/guided-setup.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Guided Setup**.

    **Note:** The landing page provides information about the different categories, tools, and user access.

2.  Select **Get Started** \(or **Continue** if you have previously started guided setup\).

    **Note:** The Pipelines and Deployments Guided Setup category page appears, displaying a list of setup tasks grouped by environment. For standalone installation, you will complete environment setup tasks only and skip pipeline creation entirely. You can add a pipeline later if needed.

3.  In the development environments category, select **Get Started** and complete setting up the controller instance.

    For more information, see [Configure your controller instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/config-controller-instance.md).

    **Note:** When you have completed this environment setup task, the Guided Setup screen reappears.

4.  If you have a testing environment, select **Get Started** in the testing environment category and configure your controller instance.

    **Note:** When you have completed this task, the Guided Setup screen reappears.

5.  In the production environment category, select **Get Started** and add users to the App Engine admin group.

    For more information, see [Add users to the App Engine admin group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/add-users-to-admin-grp.md).

    **Note:** When you have completed this environment setup task, the Guided Setup screen reappears. Standalone AEMC environment setup is complete.


## Result

Your AEMC standalone environment is set up and ready to use. When you're ready to automate your deployments, see [Configure your pipeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-management-center/config-pipeline.md).

