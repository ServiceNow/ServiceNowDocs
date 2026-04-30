---
title: Application Intake configuration tasks
description: As you work through the App Engine Studio \(AES\) Application Intake guided setup, you must perform different configuration tasks.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure Application Intake, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Application Intake configuration tasks

As you work through the App Engine Studio \(AES\) Application Intake guided setup, you must perform different configuration tasks.

## Activating and configuring the intake request process, and setting up development environments

The tasks for configuring Application Intake are listed below, along with links to detailed instructions for completing them.

<table id="table_lqq_1qt_rhb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate the catalog item where developers will submit their application ideas

</td><td>

Activate the Apply for Citizen Development catalog item so that citizen developers can submit their ideas for applications.

 For detailed instructions, see [Activate the Apply for Citizen Development catalog item](../task/activate-catalog-item-for-app-intake.md).

</td></tr><tr><td>

Set up the Apply for Citizen Development catalog item

</td><td>

For quick setup and use, use the predefined Apply for Citizen Development catalog item in Catalog Builder. To customize your app intake form, either update the Apply for Citizen Development catalog item, or use the AES App Intake template as a starting point and add questions and fields as needed.

 For detailed instructions, see [Customize the App Intake form in Catalog Builder](../task/customize-app-intake-form-catalog-builder.md#).

</td></tr><tr><td>

Add users to the App Engine Admins group

</td><td>

Add users to the App Engine Admin group. After the email address of the App Engine Admin group is configured, members can receive notifications for app development-related requests, including application intake requests.**Note:** If you already added users on the production instance using [AES guided setup](../concept/configure-aes.md) or [Configure Pipelines and Deployments](../../pipelines-and-deployments/task/config-p-and-d.md) guided setup, you can skip this step.

 For detailed instructions, see [Add users to the App Engine Admin group](../task/add-users-to-admin-grp.md).

</td></tr><tr><td>

Create development environment records

</td><td>

On your production instance, create an environment record of type "Development" for each development instance that you want to provision users to. This will allow your production instance to connect to your development instances.**Note:** If these records have already been set up in the Pipelines and Deployments Guided Setup, you can skip this step.

 For detailed instructions, see [Configure your pipeline environments](../../pipelines-and-deployments/task/config-pipeline-environments.md).

</td></tr></tbody>
</table>When you have completed Application Intake guided setup, proceed to [Pipelines and Deployments guided setup](../../pipelines-and-deployments/task/config-p-and-d.md) to fully configure App Engine Studio.

-   **[Activate the Apply for Citizen Development catalog item](../task/activate-catalog-item-for-app-intake.md)**  
Enable citizen developers to submit their ideas for applications by activating the Apply for Citizen Development catalog item. This is the first step in configuring the App Engine Studio \(AES\) Application Intake app.
-   **[Customize the App Intake form in Catalog Builder](../task/customize-app-intake-form-catalog-builder.md#)**  
Create a custom app intake experience for your organization by editing the fields and questions on the App Engine Studio \(AES\) App Intake form in Catalog Builder.
-   **[Manage user groups for Application Intake](../task/manage-app-intake-user-groups.md)**  
Control which user groups are available for admins to give Creator Studio and App Engine Studio app development permissions to during the Application Intake process. These groups are managed on the User Groups Permission Types \[sn\_app\_intake\_permission\_type\] table.

**Parent Topic:**[Configure Application Intake](../task/config-app-intake.md)

