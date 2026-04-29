---
title: Configuring App Engine Studio and related apps
description: App Engine Studio \(AES\) guided setup walks you through the implementation process, one step at a time. As you finish each setup procedure, you're prompted to begin the next one.
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

App Engine Studio \(AES\) guided setup walks you through the implementation process, one step at a time. As you finish each setup procedure, you're prompted to begin the next one.

When you have finished configuring AES, you have the option of configuring other products related to AES:

-   App Engine Management Center \(AEMC\)
-   Application Intake
-   Pipelines and Deployments

Each of these products has its own guided setup. If you have already configured one or more of the products and you are prompted to configure it again, you can simply ignore that instruction. The following diagram illustrates the preferred method for implementing AES and associated applications:

![AES implementation](../image/aes-config-infographic-smaller.png "AES implementation")

AES implementation usually follows these steps.

1.  On a development instance, install AES and the Pipelines and Deployments plugin. For more information, see [Installing App Engine Studio](../task/install-aes.md).
2.  Complete the AES guided setup. For more information, see [Configure App Engine Studio](configure-aes.md).
3.  On your production instance:
    1.  Complete the Application Intake guided setup. For more information, see [Configure Application Intake](../task/config-app-intake.md).
    2.  Complete the Pipelines and Deployments guided setup. For more information, see [Configure Pipelines and Deployments](../../pipelines-and-deployments/task/config-p-and-d.md).
4.  On a development instance, complete the first non-production task of the Pipelines and Deployments guided setup.
5.  On your test instance, install Pipelines and Deployments.
6.  Complete both non-production tasks of the Pipelines and Deployments guided setup on the test instance.
7.  In all the other non-production instances in your pipeline:
    1.  Install Pipelines and Deployments.
    2.  Complete the first non-prod tasks of the Pipelines and Deployments guided setup.
8.  Repeat step 7 across all non-production instances, as needed.
9.  Install the AEMC plugin on each instance in your pipeline. For more information, see [Configure the App Engine Management Center](../task/configure-aemc.md).

    AEMC allows admins to manage app development from intake through production on your production instance.


**Note:** If you plan on cloning your production instance to one or more non-production instances, you should also install the AES product on your production instance prior to cloning. For more information, see [Create a clone preserver](https://www.servicenow.com/docs/access?context=create-new-clone-preserver&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Cloning instances with AES](cloning-aes-applications.md).

-   **[AES and domain separation](aes-domain-sep.md)**  
Domain separation is unsupported for App Engine Studio \(AES\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Installing App Engine Studio](../task/install-aes.md)**  
You can install the App Engine Studio \(AES\) application \(com.snc.app-engine-studio\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Configure App Engine Studio](configure-aes.md)**  
App Engine Studio \(AES\) guided setup provides a sequence of tasks that help you configure AES on your ServiceNow instance.
-   **[Cloning instances with AES](cloning-aes-applications.md)**  
Learn how to protect the data, tables, and templates you've created in App Engine Studio when using System Clone to copy instances from production to non-production.

**Parent Topic:**[Build apps using App Engine Studio](aes-overview.md)

