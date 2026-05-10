---
title: Configuring App Engine Studio and related apps
description: App Engine Studio \(AES\) configuration involves installing the application and completing guided setup, which walks you through the implementation process, one step at a time. After you finish each setup procedure, you're prompted to begin the next one.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configuring App Engine Studio and related apps

App Engine Studio \(AES\) configuration involves installing the application and completing guided setup, which walks you through the implementation process, one step at a time. After you finish each setup procedure, you're prompted to begin the next one.

## Configuring App Engine Studio

Configure App Engine Studio \(AES\) by installing the application on your development instance \(and any other non-production instances on which users will develop applications\) and completing guided setup. See the following resources for more information:

-   [Installing App Engine Studio](../task/install-aes.md)
-   [Configure App Engine Studio](configure-aes.md)

**Note:** If you plan on cloning your production instance to one or more non-production instances, you should also install the AES product on your production instance prior to cloning. For more information, see [Create a clone preserver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/create-new-clone-preserver.md) and [Cloning instances with AES](cloning-aes-applications.md).

## Configuring related applications

After you finish configuring AES, you have the option to configure other applications related to AES. Each of these applications has its own guided setup. If you have already configured one or more of the applications and you're prompted to configure it again, you can simply ignore that instruction. For more information about the applications related to AES and configuring them, see the following list.

-   **[App Engine Management Center \(AEMC\)](../../app-engine-management-center/concept/configuring-aemc.md)**

    App Engine Management Center AEMC contains all of the features that you need to manage application development within your organization, from idea submission to deployment. Using AEMC, admins can manage requests for new apps and delegate development and collaboration permissions. Admins can also oversee the entire deployment process with insights into individual deployment requests, test suites, and scheduled deployments.

-   **[Application Intake](../task/config-app-intake.md)**

    Application Intake enables citizen developers to submit ideas for applications. Application Intake requests can be viewed in AEMC, where admins can approve or reject the requests.

-   **[Pipelines and Deployments](../../pipelines-and-deployments/task/config-p-and-d.md)**

    Pipelines and Deployments enables release managers and App Engine admins to build custom pipelines across multiple instances. You can also connect the testing suites and frameworks that your organization uses to verify that applications are stable and compatible before they reach production.

-   **[ReleaseOps](../../release-ops/concept/configuring-releaseops.md)**

    ReleaseOps improves the existing pipelines deployment process by supporting the deployment of update sets, leveraging the automation capabilities of ServiceNow Playbooks, and enabling both scheduled and on-demand releases.


-   **[AES and domain separation](aes-domain-sep.md)**  
Domain separation is unsupported for App Engine Studio \(AES\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Installing App Engine Studio](../task/install-aes.md)**  
You can install the App Engine Studio \(AES\) application \(com.snc.app-engine-studio\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Configure App Engine Studio](configure-aes.md)**  
App Engine Studio \(AES\) guided setup provides a sequence of tasks that help you configure AES on your ServiceNow instance.
-   **[Cloning instances with AES](cloning-aes-applications.md)**  
Learn how to protect the data, tables, and templates you've created in App Engine Studio when using System Clone to copy instances from production to non-production.

**Parent Topic:**[Build apps using App Engine Studio](aes-overview.md)

