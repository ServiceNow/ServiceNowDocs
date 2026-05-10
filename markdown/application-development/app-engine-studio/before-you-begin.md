---
title: Plan your app development
description: The application development process in App Engine Studio \(AES\) begins with your idea for the next effective app. Careful planning is the key to creating a successful app that is beneficial to your business.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Plan your app development

The application development process in App Engine Studio \(AES\) begins with your idea for the next effective app. Careful planning is the key to creating a successful app that is beneficial to your business.

## Fit for the ServiceNow AI Platform

Consider the characteristics of your application to help determine whether it is suited for the ServiceNow AI Platform.

<table id="table_xf5_nmn_swb"><thead><tr><th>

Good fit

</th><th>

Poor fit

</th></tr></thead><tbody><tr><td>

-   Simple forms
-   Task management
-   Request management
-   Spreadsheet-driven processes
-   Repeatable processes
-   Third-party integrations
-   Orchestration of multiple systems
-   Single experience from functions in multiple systems
-   Web and mobile access to the same apps and data simultaneously

</td><td>

-   Unstructured data
-   Unrepeatable processes
-   Content that needs graphics processing
-   Streaming audio or video
-   Highly customized user interface

</td></tr></tbody>
</table>## Plan before you build

In order to build your application, you need access to a ServiceNow instance and an admin or delegated developer role in that instance. If you have delegated developer permissions, you can develop applications but have fewer privileges than an admin.

Essentially, an application is a digital program that supports user tasks. As you plan your app, consider the questions in the following table.

|Questions|Answers and considerations|
|---------|--------------------------|
|What are the goals, objectives, and outputs of your application? What business problem are you trying to solve?|Without a clear business objective, you might have difficulty measuring the success of your application or justifying its continued use within the organization.|
|Are you turning a spreadsheet into a ServiceNow application or does the application exist somewhere else?|The answer to this question helps determine the tools you would use within the ServiceNow AI Platform to support your efforts.|
|Who will use your application?|Identifying your target audience has a direct impact on the features you include in your application, the data you choose to capture, and the interface you provide for the application.|
|Do you want all users to have the same ability to see and edit parts of your application or should some people have more or less access than others?|Identifying who has access to what information during the planning stage is a critical step in application development.|
|What is the main purpose of the application? Is the application used to provide information, collect information, route information, look up information, request something, or collaborate on information?|Identifying the application's purpose helps to establish the features and functions you need to build into your application.|
|Will your application require entering information or does the data in your application exist in your ServiceNow instance \(that is, user data\)? Will data be imported from an external source?|Use available data sources as much as possible to avoid duplication of data and to ensure your application has the data it needs to meet business objectives.|
|How will users interact with your application? Will users access your application using their computer or mobile device?|Understanding how users access your application affects how you build your application's functionality.|
|How will you report on your application to stakeholders?|If your application is meeting a business purpose, you might need to provide reports showing usage, adoption, and key business objectives related to your application.|
|How will you maintain this application?|Planning for the maintenance of your application at the start can prevent roadblocks further into the development process.|

The answers to these questions can help you decide whether you want to base your application on a predefined template or create your app from scratch.

## Irreversible considerations

Some actions you take when building an application might be irreversible. Be aware of these actions and plan for them in advance.

<table id="table_gtq_sbm_5wb"><thead><tr><th>

Action

</th><th>

Considerations

</th></tr></thead><tbody><tr><td>

Creating a scoped or global application

</td><td>

When you create an application, you can choose to create it in a private scope \(scoped application\) or in a global scope \(global application\). Scoped applications have extra functionality for managing development, application deployment, and data security. By default, all applications are created in a private scope. Citizen developers should generally work with scoped applications.

</td></tr><tr><td>

Using different instances

</td><td>

Proof of concept \(PoC\) applications can be built in a personal developer instance \(PDI\) obtained from the [ServiceNow Developer site](https://developer.servicenow.com/dev.do).

 -   PDI names are similar to dev12345.service-now.com.
-   PoC applications can be rebuilt in your PDI. Don’t import the PoC app into your PDI.

 Production applications that your organization uses should be created in a development instance so they can be subject to your organization’s testing and deployment process. Ask your ServiceNow administrator which instance to use for developing applications that will eventually be deployed to your organization’s production instance.

</td></tr><tr><td>

Selecting an application name

</td><td>

Based on your application’s display name, auto-complete displays suggestions for an internal name also known as the application scope. Application scopes are written in the form x\_\[company code\]\_\[app\_name\], for example, x\_acme\_legal\_request.

 Every property created in your application inherits the application scope name so be sure to choose it carefully before starting to develop your application.

 **Note:** You can always change the application's display name but the application scope name can’t be changed.

</td></tr><tr><td>

Selecting table and field names

</td><td>

After your application is created, begin creating tables and fields. Tables and fields have internal database names that should be edited only at creation time.

</td></tr></tbody>
</table>## Application Intake process

Any member of your organization can submit ideas for app development through a process called Application Intake. After the idea has been submitted and approved, developers can begin building the app with a guided, intuitive app development environment in App Engine Studio.

The Application Intake request process benefits your organization as follows:

-   Simplifies the process to request, approve, track, and store app ideas.
-   Improves planning by providing visibility into all app ideas.
-   Provides an efficient process to filter out repetitive requests.

For more information, see [Submit your idea for app development](../task/submit-intake-request.md).

-   The intake request form is available through the standard Service Catalog. For information about how you can modify this form, see [Service catalog items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_IntroductionToCatalogItems.md).
-   The intake request process uses Flows in Workflow Studio to determine the approval flow. To adjust the approval flow, see [Flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flows.md).
-   Admins review intake application requests in App Engine Management Center. For more information, see [Managing app development using the App Engine Management Center](../../app-engine-management-center/concept/managing-app-development-using-aemc.md).

## Application templates

An application template provides predefined content to support a certain purpose. For example, the Travel Request template provides application content for submitting and approving employee travel requests. Choose the template that most closely fits your application goals.

If the available templates don't fit your application goals, you can [create your app from scratch](../task/create-app-scratch.md) and control all aspects of the development process.

## Additional resources for planning your app development

<table id="table_cw4_2j1_2bc"><thead><tr><th>

Learn more about planning app development

</th><th>

ServiceNow resources

</th></tr></thead><tbody><tr><td>

ServiceNow provides additional resources on planning your app development

</td><td>

![](../../../reuse/icons/brand-icons/bus-try-a-demo.svg) [Launching an effective Citizen Development program](https://www.servicenow.com/demo/demonow-detail.html?videoid=launching-an-effective-citizen-development-program)

</td></tr></tbody>
</table>**Parent Topic:**[Building apps in App Engine Studio](aes-app-creation.md)

