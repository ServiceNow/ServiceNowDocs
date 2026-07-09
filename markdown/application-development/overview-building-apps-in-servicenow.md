---
title: Standard app development in ServiceNow
description: The ServiceNow AI Platform enables you to create global and custom applications. You can work in classic lists and forms, or you can build apps using App Engine products such as ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/overview-building-apps-in-servicenow.html
release: australia
topic_type: concept
last_updated: "2026-06-16"
reading_time_minutes: 5
breadcrumb: [Getting Started guide for developers, Building applications]
---

# Standard app development in ServiceNow

The ServiceNow AI Platform enables you to create global and custom applications. You can work in classic lists and forms, or you can build apps using App Engine products such as ServiceNow Studio.

## What apps are in ServiceNow

A ServiceNow app is a package that performs a specific task for a specified group of users. Think of an app as a container with a set of rules around who can access and edit it. For example, ServiceNow apps can include an API, a table, a workspace, a form, a flow, or any combination of those things.

Some applications may only contain a few files, and others could contain thousands of files. In ServiceNow Studio, you can create and work on different sized apps with a variety of file types, depending on your permissions.

## Agentic development and standard app development

Agentic development is an AI-driven approach to application development. Use agentic development and ServiceNow AI-powered app building tools to describe your goals in natural language, and the ServiceNow AI Platform generates full-stack applications, workflows, and integrations. The ServiceNow AI Platform automatically incorporates governance into the app creation process.

Agentic development and using AI to build apps with the ServiceNow AI Platform collapses the traditional app development lifecycle—from ideation to deployment—into minutes instead of weeks. For more information, see [Agentic development on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/vibe-coding-landing.md).

Traditional app development on the ServiceNow AI Platform usually takes place in ServiceNow Studio. ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps with ease.

Use ServiceNow Studio to build apps and app files with integrated tools, access and edit app metadata in scoped and global apps, and package app changes for deployment, all in one powerful development tool. For more information, see [ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-landing.md).

## Apps and plugins

In ServiceNow, applications and plugins are related but distinct concepts.

**Applications** are collections of ServiceNow components \(tables, business rules, UI pages, etc.\) that deliver specific functionality. They're essentially containers that bundle related features together. Applications can be:

-   Custom-built by your organization
-   Purchased from the ServiceNow Store
-   Core applications that come with ServiceNow \(like Incident Management\)

**Plugins** are a specific type of application that adds functionality to your ServiceNow instance. The key differences between plugins and apps are as follows.

-   Plugins are typically installed via activation rather than traditional app installation.
-   Plugins are often foundational components that other apps depend on.
-   Once activated, plugins integrate deeply into the platform
-   Plugins are harder to remove - you can't easily deactivate a plugin once it's in use.

Examples: ITIL, HR Service Delivery, Software Asset Management

**Note:** All plugins are applications, but not all applications are plugins. Plugins are the heavyweight, deeply-integrated applications that become part of your platform's foundation.

## Apps and workflows

**Applications** are collections of components that deliver functionality - the building blocks of your ServiceNow instance.

**Workflows** are automation tools within ServiceNow that define a sequence of activities to complete a process. Think of them as flowcharts that automate business processes. Workflows:

-   Automate approvals, notifications, and task assignments.
-   Define the step-by-step flow of work \(if X happens, then do Y\).
-   Are often part of an application.
-   Use a drag-and-drop workflow editor.

Example: An approval workflow for purchase requests

The relationship: A workflow is a component that lives inside an application.

For instance, the Incident Management application might contain workflows that automatically assign tickets, send notifications, or escalate issues.

**Note:** Applications are the "what" \(the functionality\), workflows are the "how" \(the automated processes that make things happen\).

-   **[Determining good candidates for apps in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/determining-good-candidates-for-apps.md)**  
Before creating an app in ServiceNow, determine if the idea is a good candidate for an application.
-   **[Configure, customize, or build apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/configure-customize-or-build-new-apps.md)**  
Configuration and customization are hallmarks of the ServiceNow AI Platform that enable your company to customize workflows to fit its specific needs. You can also build new apps for novel use cases or departmental processes that don't fit within the scope of your current applications.
-   **[Plan your app before you start building](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/plan-app-building.md)**  
Planning your application before development ensures scalability, governance, and alignment with organizational goals. Effective planning reduces duplication, helps prevent technical debt, and ensures compliance with ServiceNow best practices. It also helps define clear objectives, timelines, and resource requirements.
-   **[ServiceNow files in applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-files-in-applications.md)**  
ServiceNow files are digital documents and assets stored within the ServiceNow AI Platform that serve various purposes across applications and workflows.
-   **[ServiceNow metadata in applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-metadata-in-applications.md)**  
ServiceNow metadata refers to the configuration and structural definitions that make up a ServiceNow application itself.
-   **[Build your first application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-your-first-app.md)**  
Build, configure, and deploy custom apps from a single development environment, ServiceNow Studio. ServiceNow Studio gives admins and developers integrated tools to create app files, edit scoped and global app metadata, and package changes for deployment.
-   **[User interface and experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-ui-and-experience.md)**  
Learn about user interfaces and tools for building them as you create applications on the ServiceNow AI Platform.
-   **[Integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-integrations.md)**  
Integrations enable you to connect your custom app to external systems to send and receive data. The ServiceNow AI Platform supports multiple integration capabilities to fit your use case.

**Parent Topic:**[Getting Started guide for developers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/getting-started-landing-page.md)

