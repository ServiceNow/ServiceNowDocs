---
title: Guided Application Creator
description: Guided Application Creator is an intuitive development interface for building applications on the ServiceNow AI Platform. It provides a step-by-step process to guide you through your initial application construction.
locale: en-US
release: xanadu
product: Guided Application Creator
classification: guided-application-creator
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Building pro-code applications, Developing your application, Building applications]
---

# Guided Application Creator

Guided Application Creator is an intuitive development interface for building applications on the ServiceNow AI Platform®. It provides a step-by-step process to guide you through your initial application construction.

**Important:** You've landed at a legacy app creation tool that will be supported until the Australia release in Q1 2026. Try building and editing apps in the new version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Explains how to use Guided Application Creator to create a new application for workspace, mobile, and classic with an imported spreadsheet.

Watch this four-minute video to learn about getting started with Guided Application Creator.

**Note:** Although the video describes creating a workspace in Guided Application Creator, this feature is no longer supported.Instead, you can create a workspace using App Engine Studio. For more information, see [Building applications in App Engine Studio](../../app-engine-studio/concept/aes-app-creation.md).

## Using Guided Application Creator

Setting up an application in Guided Application Creator involves:

-   Creating an application record
-   Defining user roles
-   Designating data tables
-   Designing the application for different user experiences

You can also use Guided Application Creator to create an application record and then configure it in Studio later. For more information, see [Create an application record in Guided Application Creator](../task/gac-create-app-record.md).

## User experiences

When you set up an application in Guided Application Creator, you can make your application available in the following user experiences.

<table id="table_p4k_ygk_vhb"><thead><tr><th>

User experience

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mobile

</td><td>

ServiceNow Agent mobile app. Select this user experience to support users who work from a mobile device.

</td></tr><tr><td>

Classic

</td><td>

Classic ServiceNow AI Platform experience. Select this user experience to let your users work on your application via lists and forms.

</td></tr></tbody>
</table>## Guided Application Creator and the application creation process

Setting up an application in Guided Application Creator does not capture the entire process of creating an application. It is just one step of the process. Before you set up an application in Guided Application Creator, plan what kind of application you need for your business requirements before you build it.

After you set up an application in Guided Application Creator, you can further develop the application using [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md), [Flows in Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US), and [Team Development](../../team-development/concept/c_TeamDevelopment.md). After the application is fully built, you can test the application and then share the application with your users.

For more information on the application creation process, see [Building applications](../../custom-application/concept/build-applications.md).

## Activation information

Guided Application Creator is enabled via the Guided Application Creator \(com.glide.sn-guided-app-creator\) plugin, which is active by default in the ServiceNow AI Platform.

To work in Guided Application Creator, use a different browser. For more detail on Internet Explorer 11 support, see [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275).

-   **[Setting up an application in Guided Application Creator](../task/set-up-app.md)**  
Set up an application in Guided Application Creator to store information and manage business processes.
-   **[Data table guidelines for Guided Application Creator](gac-tables.md#)**  
When you create an application in Guided Application Creator, you can optionally create a data table for your application. To ensure that you are within the limits of your subscription and that your application performs as expected, consult the data table guidelines before you create a data table.
-   **[Allow global application development in Guided Application Creator](../task/gac-activate-global.md)**  
By default, developers can't create applications in the global scope in Guided Application Creator. You can limit global application development to certain developers by assigning them an additional role.
-   **[Add field types in Guided Application Creator](../task/gac-add-field-types.md)**  
When you add fields to a custom table in Guided Application Creator, there are only 18 field types available by default. You can add a property to include more field types.

**Parent Topic:**[Building pro-code applications](../../custom-application/reference/building-pro-code-applications.md)

