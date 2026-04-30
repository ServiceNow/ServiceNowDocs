---
title: Exploring Creator Studio
description: Creator Studio makes creating apps easier by dividing their creation into simple steps. In this section, we'll explain each one.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Exploring Creator Studio

Creator Studio makes creating apps easier by dividing their creation into simple steps. In this section, we'll explain each one.

All the steps involve requests. So, we'll start by explaining how Creator Studio stores requests.

**Summary:** After reading this section, you'll understand:

-   How requests are stored
-   How people enter requests
-   How your app automatically does things

## Let's talk about storing requests

When people make a request, we have to store it somewhere so someone can review it later.

**Tables hold requests**

Creator Studio stores requests in a table. Each row in that table is a request. Here's a simplified version of a table with three requests.

**Use cases:**

-   My monitor stopped working. I need a new one.
-   I'm requesting a new mouse so I can have one at home and in the office.
-   My laptop is over four years old. I want to request a replacement.

**People enter requests using forms**

How do people enter requests that eventually get stored in the app's table? They use your app to fill out a form. The questions on the form contain the information your fulfiller needs.

In our app's table, questions are stored as part of the [record](creator-studio-glossary.md#), which is composed of all the information on the form.

|Request|Name|Email|Request date|
|-------|----|-----|------------|
|I need a new monitor.|Sushma Singh|SushmaSingh@example.com|04-05-2024|
|I need a new laptop.|Peter Smith|PeterSmith@example.com|05-01-2024|

In this example, the form has four fields:

-   Request
-   Requester's name
-   Requester's email address
-   Request date

These fields contain all the info the reviewer needs to accept or reject the request. You'll have to figure out all the information your reviewer needs to make a decision. Later, we'll show you how to create a form \(using Now Assist or on your own\) in the section [Working with forms in Creator Studio](creator-studio-work-with-forms.md).

**Key terms:**

-   **Requester**

    Someone requesting something, like a piece of equipment or permission to do something.

-   **Fulfiller**

    Someone who works on requests. Fulfillers may also approve or deny requests, depending on any approval automation for the app.


Okay, now you understand that requesters fill out forms to create requests and Creator Studio stores those requests in the app's table.

## Try Creator Studio on a PDI

Want to play with Creator Studio on your Personal Development Instance \(PDI\)? It comes automatically installed from the Application Manager on your PDI. For more information, see [Personal developer instance guide](../../applications/concept/personal_developer_instance_guide.md).

-   **[Example apps you can build in Creator Studio](creator-studio-sample-apps.md)**  
Creator Studio enables you to build apps where people can make requests.
-   **[Use App Engine instead of customization](creator-studio-config-vs-custom.md)**  
App Engine development tools, such as Creator Studio, offer an excellent alternative to customizing existing applications on the ServiceNow AI Platform.
-   **[Customization vs. configuration with Creator Studio](creator-studio-custom-vs-config.md)**  
There are important differences between customizing and configuring ServiceNow applications. The ServiceNow platform is built to embrace customization and configuration but how you do so can have significant impacts on ServiceNow support, upgrading to future ServiceNow platform versions, and the functionality of the ServiceNow platform.
-   **[Creating your first app with Creator Studio](creator-studio-creating-your-first-app.md)**  
Creator Studio helps you create your app by dividing it into smaller parts. Each does something special, and you work on them sequentially.
-   **[Creator Studio quick start](../task/creator-studio-quick-start.md#)**  
This quick start guides you through the process of building your first app in Creator Studio and requesting its deployment.
-   **[Get help with Creator Studio](creator-studio-get-help-now.md)**  
To get help with Creator Studio, your ServiceNow instance, plugins, permissions, and more, watch a short video to contact the ServiceNow admin who works in your company.
-   **[Choosing your development experience](crs-choosing-your-experience.md)**  
If you want to develop apps in a more robust environment than Creator Studio, which was designed for no-code developers, you can select a different experience directly from within Creator Studio.
-   **[Service desks and Creator Studio](creator-studio-service-desk-about.md)**  
Service desk apps enable users to request things, such as IT equipment or travel bookings, and track their fulfillment.
-   **[Migrating to Creator Studio from Service Creator](creator-studio-migrating-service-creator.md)**  
Creator Studio is replacing the older Service Creator tool, which will be retired in the Australia release.
-   **[App compatibility with Creator Studio](creator-studio-opening-apps-from-others.md)**  
You can open apps built in Creator Studio in other ServiceNow products, but only apps built in Creator Studio can be opened in Creator Studio.
-   **[Creator Studio apps and tables](creator-studio-templates.md)**  
Creator Studio uses catalog templates to streamline the app creation process. Apps use the Request Task table by default, generating a new row for each submitted request, though admins can change the underlying table for an app.
-   **[Publishing, activation, and deployment workflow for forms, automation, and apps](creator-studio-workflow-publishing-deploying.md)**  
When you build an app in Creator Studio, you must create forms and automation. You can also customize the workspace list configurations and records that fulfillers use before everything is deployed to production.

**Parent Topic:**[Creator Studio](creator-studio-landing.md)

