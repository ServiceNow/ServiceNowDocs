---
title: Convert custom applications to upgrade from the application repository
description: When your applications are placed in the Custom Applications table \[sys\_app\], you can't upgrade them directly through the Application Repository. This procedure helps you do a one-time conversion when you want to migrate deploying your applications using the Application Repository.
locale: en-US
release: yokohama
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage customizations to applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Convert custom applications to upgrade from the application repository

When your applications are placed in the Custom Applications table \[sys\_app\], you can't upgrade them directly through the Application Repository. This procedure helps you do a one-time conversion when you want to migrate deploying your applications using the Application Repository.

## Before you begin

Role required: admin

When you start with Update Sets, all your applications in all your instances are placed in the Custom Applications table \[sys\_app\]. However, if you decide to use the recommended ServiceNow® [Continuous Integration/Continuous Delivery API/Spoke](https://www.servicenow.com/docs/access?context=cicd-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) guidance for using the Application Repository in your CI/CD pipelines, the system doesn't allow the upgrades because the applications already exist in Custom Applications table. They are moving to the ServiceNow Store table \[sys\_store\_app\] so they can be installed from the application repository, which is why they can no longer be developed on that instance.

After you convert the application, it is no longer enabled for development on the instance where the conversion is performed. For a scoped custom application, all associated records in the Customer Updates table are deleted for this application.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  Open the **In Development** tab.

3.  Click the name of the application record that you want to convert.

4.  Select the **Convert to Application Repository Mode** related link.

    ![Convert to application repository mode related link](../image/ui_action_sys_app.png)

5.  Select **Convert**.

    -   In scoped custom applications, the following message displays.

        ![Scoped custom app confirmation message](../image/convert-scoped-app-confirm.png)

    -   In global custom applications, the following message displays.

        ![Global custom app confirmation message](../image/convert-global-app-confirm.png)

    -   After the successful conversion, the following message displays.

        ![Successful conversion message](../image/convert-success.png)


## What to do next

Go to **System Applications-&gt;My Company Applications** and update the application using the software from the application repository. See [Install an application from the application repository](install-app-from-repo.md) to learn more.

