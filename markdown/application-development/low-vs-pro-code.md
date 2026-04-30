---
title: Low-code versus pro-code development
description: Learn the difference between low-code and pro-code solutions on the ServiceNow AI Platform.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Low-code versus pro-code development

Learn the difference between low-code and pro-code solutions on the ServiceNow AI Platform.

## Which builder should I use to create an app?

![Different builders available for different skill levels](../../creator-studio/image/mmasset0020724-appengine-landing.svg "Types of builders")

**Want to build an app easily, without code?**

Creator Studio specializes in helping you craft request-fulfillment applications without writing code. For example, an application to request office supplies by filling out a form, and someone approves or denies your request. For more information, see [Exploring Creator Studio](../../creator-studio/concept/exploring-creator-studio.md).

**Need a more general app but still want low-code options?**

App Engine Studio lets you build a broader range of apps than Creator Studio without being a programming pro. For more information, see [Exploring App Engine Studio](../../app-engine-studio/concept/exploring-aes.md).

**Are you a developer who wants more control in a centralized user interface?**

Build apps smarter and deliver them faster with the new ServiceNow Studio. ServiceNow Studio empowers platform developers with a modern, unified environment for building on the ServiceNow AI Platform. ServiceNow Studio features streamlined navigation to applications and metadata, integrated low-code tools, efficient tracking and packaging of development work that accelerates development processes and enhances productivity. For more information, see [Exploring ServiceNow Studio](../../servicenow-studio/concept/exploring-servicenow-studio.md).

**Are you a developer who wants to use industry-standard development tools and processes?**

The ServiceNow IDE and ServiceNow SDK support developing applications in source code with ServiceNow Fluent, creating JavaScript modules, and using third-party libraries. ServiceNow Fluent is a domain-specific programming language for creating application metadata in code.

The ServiceNow IDE is an implementation of Visual Studio Code for the Web on the ServiceNow AI Platform. The ServiceNow SDK uses Visual Studio Code Desktop locally. For more information, see [Building applications in source code](building-applications-source-code.md).

## What is low-code development

Low-code development is a new approach to app creation that allows users with limited coding experience to create powerful apps. Low-code development platforms rely on graphical interfaces and configuration instead of manual coding. These new low-code development platforms enable more people to create and deploy apps quickly and efficiently.

## Benefits of low-code development

Low-code app development streamlines the development process to build more apps faster. Low-code solutions require fewer developers, and allow non-developers to build apps. Pre-built templates provide developers a head start building apps. System administrators can manage app development from a single location and collaborate with other developers. Decrease the time that it takes to deploy apps using predefined workflows in the ServiceNow AI Platform.

## ServiceNow no-code and low-code development tools

-   [Creator Studio](../../creator-studio/concept/creator-studio-landing.md)
-   [App Engine Studio](../../app-engine-studio/concept/aes-overview.md)
-   [UI Builder](../../../administer/ui-builder/concept/ui-builder-overview.md)
-   [Guided Application Creator](../../guided-app-creator/concept/guided-app-creator.md)
-   [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md)
-   [Flows in Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)
-   [Workspace Builder](../../app-engine-studio/task/configure-workspace-builder.md)
-   [Exploring decision tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

For more information on low-code development tools, see [Building low-code applications](../reference/building-low-code-applications-with-app-engine.md).

## No-code development tool example

Creator Studio makes creating basic request-fufillment apps easier by dividing their creation into simple steps. You can create forms for users to request catalog items and use form submissions to initiate automated playbooks. Find out more in [Creator Studio](../../creator-studio/concept/creator-studio-landing.md).

![Select the Create app button](../../creator-studio/image/crs-create-app-button.png "Create app an app in Creator Studio")

## What is platform development

If you're comfortable with the ServiceNow AI Platform and some development tools, use the new [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md) to access all of the builders and development tools in one place.

## Platform development tool example

![Create an app using either the Navigator icon or the Create button](../../servicenow-studio/image/sn-studio-create-app.png "Create an app in ServiceNow Studio")

## What is pro-code development

Pro-code development is used by developers to create complex apps that can't be built with a low-code tool. Traditionally, pro-code development is used to create apps from scratch using custom code to solve a business need. Developers need to have knowledge of coding and how to use programming languages to build apps.

## Benefits of pro-code development

The advantage of pro-code development is being able to create custom apps without the limitation of a tool. You can build custom apps unique to your business needs without limits. Developers can create apps with a custom look and feel to match your company's branding.

## ServiceNow pro-code development tools

-   [ServiceNow IDE](../../servicenow-ide/concept/servicenow-ide-landing.md)
-   [ServiceNow SDK](../../servicenow-sdk/concept/servicenow-sdk-landing.md)
-   [Scripting](../../../script/topic/c_Script.md)
-   [REST APIs](https://www.servicenow.com/docs/access?context=c_RESTAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
-   [ServiceNow Extensions for Visual Studio Code](../../applications/concept/vs-code.md)

For more information on pro-code development tools, see [Building pro-code applications](../reference/building-pro-code-applications.md).

## Low-code versus no-code

The terms low-code and no-code tend to get used interchangeably, but they aren't exactly the same thing. While both low-code and no-code solutions provide tools for simplified app development, the differences are worth considering.

-   **Low-code**

    Low-code platforms are designed for professional developers and non-technical business users. They require very little training or experience and use visual-based modeling to streamline the development process. They also allow people with coding experience to dive deeper, coding by hand when needed.

-   **No-code**

    No-code platforms require no development experience, and are designed specifically for citizen developers and business users. No-code solutions open app development up to essentially everyone, but can lead to shadow IT—unsanctioned app development within an organization.


