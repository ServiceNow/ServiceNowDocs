---
title: Build your first application
description: Build, configure, and deploy custom apps from a single development environment, ServiceNow Studio. ServiceNow Studio gives admins and developers integrated tools to create app files, edit scoped and global app metadata, and package changes for deployment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/build-your-first-app.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Standard app development, Getting Started guide for developers, Building applications]
---

# Build your first application

Build, configure, and deploy custom apps from a single development environment, ServiceNow Studio. ServiceNow Studio gives admins and developers integrated tools to create app files, edit scoped and global app metadata, and package changes for deployment.

ServiceNow Studio features streamlined navigation to applications and metadata, integrated low-code tools, efficient tracking and packaging of development work that accelerates development processes and enhances productivity. Though you can begin building with the classic lists and forms on the platform, beginning in ServiceNow Studio gives you a head start with some basic app elements.

## ServiceNow Studio features and benefits

Use ServiceNow Studio to build, manage, and deploy apps faster in a single development environment. It provides the following features for admins and delegated developers.

\[Omitted image "sn-studio-features-benefits-as1.png"\] Alt text: ServiceNow Studio offers a unified experience for all development activities on the ServiceNow AI Platform.

-   AI-native design: Use the generative and agentic AI capabilities in ServiceNow Studio to build apps faster and extend custom applications with AI. For more information, see [AI tools and files in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-now-assist-tools-sn-studio.md).
-   Build Agent: Use Build Agent, an autonomous AI agent, to create and update applications in ServiceNow Studio. For more information, see [Build Agent in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/build-agent-in-servicenow-studio.md).
-   Integrated builders: Access low-code builders available in the ServiceNow AI Platform, including Table Builder and flows in Workflow Studio, alongside app development tools. For more information, see [Access integrated development tools and builders in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/open-and-switch-between-integrated-development-tools.md).
-   AI and code search: Search for any application or metadata record in your instance using AI Search and standard code search. For more information, see [Find an app or app file using Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/qs-find-app-app-file-using-search.md) and [Find an app or app file using the Navigator panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/qs-find-app-app-file-using-navigator-panel.md).
-   Accelerated deployment: Create and package apps for deployment using update sets, pipelines, or the Application Repository without leaving ServiceNow Studio. For more information, see [Update sets in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-update-sets-in-servicenow-studio.md) and [Publish app changes to the Application Repository from ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/qs-publish-changes-to-app-using-app-repo.md).
-   Choose your development experience: Switch between development environments using the experience switcher in ServiceNow Studio to use the best tool for each stage of your project. For more information, see [Change your development experience in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/change-your-development-experience.md).
-   Create apps and files: Create apps and files in any scope that you have access to edit, including the global scope. For more information, see [Create an application in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-an-application-in-servicenow-studio.md) and [Create an app file in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-create-app-file.md).
-   Global and custom scope: Open and edit files of any scope you have access to, including global and custom files. The scope switches automatically when you switch between open files in different applications. For more information, see [Open apps and app files across scopes in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/qs-open-apps-files-across-scopes.md).

## Other options for building apps

ServiceNow Studio is the best option to get started creating apps fast. However, there are other options for getting started building an application.

-   App Engine Studio and Creator Studio enable you to build simple applications, which you can edit further in ServiceNow Studio.

    For more information, see [Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/creator-studio/creator-studio-landing.md) and [Build apps using App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-overview.md).

-   ServiceNow IDE enables you to create and develop scoped applications in source code in an integrated development environment \(IDE\). Apps created in the ServiceNow IDE are converted to Fluent and deployed through the IDE. However, most IDE apps can also be updated in ServiceNow Studio.

    For more information about pro-code development, see [ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/servicenow-ide-landing.md).

-   Custom tables generate lists and forms—lists display multiple records in a spreadsheet-like view while forms show detailed information for a single record. The typical development pattern is: create your custom table, customize the form layout for data entry, configure the list view for browsing records, then add UI policies, scripts, and actions to control behavior.

    For more information about developing using classic lists and forms, see [ServiceNow AI Platform® forms, fields, and lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/now-platform-forms-fields-lists.md).


-   **[Parts of an application in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/parts-of-an-application.md)**  
Applications in ServiceNow have tables, UI elements, application files, integrations, and dependencies, all with a layer of security through the entire app.
-   **[Tables and data models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/tables-and-data-models.md)**  
Tables are the foundation of ServiceNow applications, as they define what data you're storing and how it's structured. Each table consists of fields \(columns\) that hold specific data types such as strings, dates, numbers, and references to other tables.
-   **[Building a data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-a-data-model.md)**  
Plan your data model carefully before building an application on the ServiceNow AI Platform. It defines what information you're managing, how it connects, and ultimately determines what your application can do.
-   **[Automation basics for apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automation-basics-for-apps.md)**  
Automation is central to ServiceNow application development and is a core strength of the ServiceNow AI Platform. Automation enables developers to build applications that reduce manual work, enforce consistency, and respond intelligently to business events.
-   **[Dependencies for custom applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationDependencies.md)**  
Every custom application record includes a related list identifying its dependencies on other applications. Dependencies are references from your custom application to functionality provided by other applications or plugins installed on the instance.
-   **[Forms and list layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/forms-and-list-layouts.md)**  
Forms and list layouts control how an app's data appears to users. A form displays a single record so users can view or edit it. A list displays multiple records so users can browse, filter, and find the data they need.
-   **[Adding business logic to apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/adding-business-logic-to-apps.md)**  
Business logic lets your app respond automatically to data changes, enforce rules, and perform calculations without requiring user intervention.
-   **[Building workflows and automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-workflows-and-automations.md)**  
Workflows and automation let your app take action automatically in response to events, record changes, or schedules. Rather than relying on users to manually move work forward, you define the logic once and let the platform execute it consistently.
-   **[Advanced scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/advanced-scripting.md)**  
As an app grows in complexity, it may reach the limits of what business rules, script includes, and Flow Designer actions can accomplish through configuration alone. Advanced scripting means writing directly against ServiceNow's server-side JavaScript APIs to handle logic that requires more precision or flexibility than low-code tools provide.

**Parent Topic:**[Standard app development in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/overview-building-apps-in-servicenow.md)

