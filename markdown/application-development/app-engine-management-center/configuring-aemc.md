---
title: Configuring AEMC
description: Learn about the configuration process for AEMC.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/app-engine-management-center/configuring-aemc.html
release: brazil
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [App Engine Management Center, Run, AI Workflow Factory, Building applications]
---

# Configuring AEMC

Learn about the configuration process for AEMC.

## AEMC configuration overview

To start using AEMC, you must install AEMC on your instances and configure AEMC and related features, such as Application Intake, Pipelines and Deployments, ReleaseOps, and Developer Sandboxes.

The following list outlines the process for configuring AEMC and related features:

1.  Install AEMC on each instance that will participate in your AEMC deployment pipeline \(for example: development, test, production etc.\).
2.  [Configure the App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/configure-aemc.md) by completing guided setup.
3.  [Configure Application Intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/config-app-intake.md) to set up who can submit requests for new applications and what questions appear on the application intake form.
4.  Choose from and configure one of the three deployment options:
    -   [Configure Pipelines and Deployments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/config-p-and-d.md)
    -   [Configure ReleaseOps in AEMC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/configure-releaseops-in-aemc.md)
    -   [Configure a standalone environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/configure-standalone.md)
5.  [Test App Engine Management Center functionality on a non-production instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/test-aemc-non-production-instance.md) to verify that AEMC is working as expected, before you start deploying changes to production.

-   **[Configure the App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/configure-aemc.md)**  
Use the App Engine Management Center \(AEMC\) guided setup to step through the initial configuration of the Application Intake and Pipelines and Deployments applications. The Application Intake guided setup is optional, but if you want to use AEMC, the Pipelines and Deployments guided setup is required.
-   **[Configure Application Intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/config-app-intake.md)**  
Use the App Engine Studio \(AES\) Application Intake guided setup to step through the initial configuration of the Application Intake application. Detailed instructions for each step are provided in subsequent sections of the product documentation.
-   **[Configure ReleaseOps in AEMC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/configure-releaseops-in-aemc.md)**  
Complete ReleaseOps guided setup in AEMC to start using ReleaseOps for your deployments.
-   **[Configure Pipelines and Deployments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/config-p-and-d.md)**  
Use the Pipelines and Deployments guided setup to complete the initial configuration of Pipelines and Deployments. Detailed instructions for each step are provided in subsequent sections of the product documentation.
-   **[Configure a standalone environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/configure-standalone.md)**  
With App Engine Management Center \(AEMC\), you no longer need an active deployment pipeline to get started. Complete the standalone environment setup to start deploying changes quickly. You can add a pipeline later when you're ready to automate deployments.

**Parent Topic:**[App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/app-engine-management-center.md)

