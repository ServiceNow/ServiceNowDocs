---
title: Convert custom applications to upgrade from the application repository
description: When your applications are placed in the Custom Applications table \[sys\_app\], you can't upgrade them directly through the Application Repository. This procedure helps you do a one-time conversion when you want to migrate deploying your applications using the Application Repository.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/application-repository-self-hosted/convert-custom-app-to-update-app-repo.html
release: australia
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage customizations to applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Convert custom applications to upgrade from the application repository

When your applications are placed in the Custom Applications table \[sys\_app\], you can't upgrade them directly through the Application Repository. This procedure helps you do a one-time conversion when you want to migrate deploying your applications using the Application Repository.

## Before you begin

Role required: admin

When you start with Update Sets, all your applications in all your instances are placed in the Custom Applications table \[sys\_app\]. However, if you decide to use the recommended ServiceNow® Continuous Integration/Continuous Delivery API/Spoke guidance for using the Application Repository in your CI/CD pipelines, the system doesn't allow the upgrades because the applications already exist in Custom Applications table. They are moving to the ServiceNow Store table \[sys\_store\_app\] so they can be installed from the application repository, which is why they can no longer be developed on that instance.

After you convert the application, it is no longer enabled for development on the instance where the conversion is performed. For a scoped custom application, all associated records in the Customer Updates table are deleted for this application.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  Open the **In Development** tab.

3.  Click the name of the application record that you want to convert.

4.  Select the **Convert to Application Repository Mode** related link.

    \[Omitted image "ui\_action\_sys\_app.png"\] Alt text: Convert to application repository mode related link

5.  Select **Convert**.

    -   In scoped custom applications, the following message displays.

        \[Omitted image "convert-scoped-app-confirm.png"\] Alt text: Scoped custom app confirmation message

    -   In global custom applications, the following message displays.

        \[Omitted image "convert-global-app-confirm.png"\] Alt text: Global custom app confirmation message

    -   After the successful conversion, the following message displays.

        \[Omitted image "convert-success.png"\] Alt text: Successful conversion message


## What to do next

Go to **System Applications-&gt;My Company Applications** and update the application using the software from the application repository. See [Install an application from the application repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/application-repository-self-hosted/install-app-from-repo.md) to learn more.

