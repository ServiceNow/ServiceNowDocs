---
title: Legacy - ServiceNow Studio
description: The legacy ServiceNow Studio provides an Integrated Development Environment \(IDE\)-like interface for application developers to work on custom applications in one centralized location. It offers a simple way to create, review, and update application files from a tabbed environment.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Building pro-code applications, Developing your application, Building applications]
---

# Legacy - ServiceNow Studio

The legacy ServiceNow Studio provides an Integrated Development Environment \(IDE\)-like interface for application developers to work on custom applications in one centralized location. It offers a simple way to create, review, and update application files from a tabbed environment.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

The system opens the new ServiceNow Studio whenever you edit a custom application.

## Capabilities

-   Create an application and application artifacts.
-   Perform code search.
-   Integrate with source control.
-   Create your company's customizations to store applications that belong to other organizations.
-   Use [Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) to create and manage topics, which are blueprints for conversations between a virtual agent and a user. You can design topics that help your users resolve common work issues or guide them through self-service tasks.

![Studio User interface displaying the header, application explorer, content frame, and status bar.](../image/studio-ui-istanbul.png "Studio")

With Studio, application developers can:

-   See exactly what files comprise their application in the **Application Explorer**.
-   Add new files to their application using a single **Create Application File** interface.
-   Navigate to files using familiar search-by-name or by-type behavior with the **Go To** dialog.
-   Find code both within and outside an application using the **Code Search** tool.
-   Operate on multiple files at once using the tabbed interface.
-   Operate on multiple applications at once using multiple studio windows.
-   Publish their application to company instances or the ServiceNow Store.
-   View information about their current application from the **Status Bar**.

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

The ServiceNow IDE is an implementation of Visual Studio Code for the Web on the ServiceNow AI Platform. The ServiceNow SDK uses Visual Studio Code Desktop locally. For more information, see [Building applications in source code](../../custom-application/concept/building-applications-source-code.md).

## Working with the Studio UI

<table id="table_ysl_xvn_1s"><thead><tr><th>

UI element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Header

</td><td>

Displays menus and controls.

</td></tr><tr><td>

**File Menu**

</td><td>

Contains a list of application-specific options. -   **Create File**
-   **Import From Source Control**
-   **Create Application**
-   **Publish**
-   **Settings**
-   **Switch**
-   **Manage Developers**
-   **Launch Script Debugger**

</td></tr><tr><td>

**Source Control Menu**

</td><td>

Contains a list of source control options. -   **Link To Source Control**
-   **Edit Repository Configuration**
-   **Apply Remote Changes**
-   **Commit Changes**
-   **Stash Local Changes**
-   **Switch Branch**
-   **Create Branch**
-   **Create Tag**
-   **Manage Stashes**
-   **View History**

</td></tr><tr><td>

**Window Menu**

</td><td>

Contains a list of tab management options. -   **Close Current Tab**
-   **Close All Tabs**
-   **Close Other Tabs**
-   **Close Unmodified Tabs**

</td></tr><tr><td>

**Search Menu**

</td><td>

Contains a list of search options. -   **Go To**
-   **Code Search**

</td></tr><tr><td>

**User name**

</td><td>

The header displays the name of current user.

</td></tr><tr><td>

**Create Application File**

</td><td>

Allows developers to [add an application file to an application](../task/t_AddAnAppFileToAnApp.md).

</td></tr><tr><td>

**Go To**

</td><td>

Search for application files by name or type.

</td></tr><tr><td>

**Code Search**

</td><td>

Search within application files for a text string. Search options include:

 -   Restrict search to a particular table
-   Include all applications

</td></tr><tr><td>

**Application Explorer**

</td><td>

Displays a list of application files by type. Resize the Application Explorer to see more about application files or to provide more space for the content frame.

</td></tr><tr><td>

**Collapse All**

</td><td>

Collapses all nodes in the application explorer.

</td></tr><tr><td>

**Expand All**

</td><td>

Expand all nodes in the application explorer.

</td></tr><tr><td>

**Data Model** &gt; **Tables**

</td><td>

A list of application tables.

 Click a table name to display and edit it in the content frame.

</td></tr><tr><td>

**Access Control**

</td><td>

A list of application access elements such as:

 -   **Roles**
-   **Access Controls**

 Click a record name to display and edit it in the content frame.

</td></tr><tr><td>

**Navigation**

</td><td>

A list of application navigational elements such as:

-   **Application Menus**
-   **Modules**
-   **Application Menus \(Mobile\)**
-   **Modules \(Mobile\)**

 Click a record name to display and edit it in the content frame.

</td></tr><tr><td>

**Content frame**

</td><td>

Displays a detail form for each record in its own tabs.

</td></tr><tr><td>

Welcome to Studio

</td><td>

A list of keyboard shortcuts.

</td></tr><tr><td>

Tabs

</td><td>

Each tab contains a specific application file record identified by the record name and file type.

 Click a tab to display and edit the record.

 A tab with a blue circle icon indicates that the record contains unsaved changes.

</td></tr><tr><td>

Status Bar

</td><td>

Displays information about the application and the source control integration.

</td></tr><tr><td>

Application name

</td><td>

The status bar displays the name of the [current application](../task/t_UpdateAnApplicationRecord.md).

</td></tr><tr><td>

Application version

</td><td>

The status bar displays the current [application version](c_ApplicationVersioning.md).

</td></tr><tr><td>

Total files

</td><td>

The status bar displays the total number of [application files](c_ApplicationFiles.md).

</td></tr><tr><td>

Unsaved files

</td><td>

The status bar displays the current number of application files with [unsaved changes](../task/t_CommitChanges.md).

</td></tr><tr><td>

Source control integration status

</td><td>

The status bar displays an icon indicating the current status of the [source control integration](c_SourceControlIntegration.md).

</td></tr></tbody>
</table>-   **[Legacy - Access ServiceNow Studio](../task/t_AccessStudio.md)**  
Application developers access ServiceNow Studio to create, import, or open applications.
-   **[Legacy - ServiceNow Studio keyboard shortcuts](../reference/r_ServiceNowStudioKeyboardShortcuts.md)**  
ServiceNow Studio supports various keyboard shortcuts to manage and edit application files.
-   **[Legacy - Add an application file to an application](../task/t_AddAnAppFileToAnApp.md)**  
Studio allows application developers to add new application files by type.
-   **[Legacy - Publish an application from ServiceNow Studio when linked to Source Control](../task/publish-app-from-studio.md)**  
You can publish a custom application from ServiceNow Studio when linked to Source Control.
-   **[Legacy - Search for an application file by name or type](../task/t_SearchForAppFilesByNameOrType.md)**  
Application developers can use Studio to search for application files.
-   **[Legacy - Search within application files](../task/t_SearchWithinApplicationFiles.md)**  
Studio allows application developers to search within application files for matching record values.
-   **[Legacy - Update a custom application record](../task/t_UpdateAnApplicationRecord.md)**  
You can update a custom application record to add new features or change application functionality.
-   **[Legacy - Switch between applications](../task/t_SwitchBetweenApplications.md)**  
Application developers can switch between applications without leaving the Studio environment.
-   **[Legacy - Global application file management](manage_global_application_files.md)**  
Once you create a globally scoped application in the ServiceNow Studio, you can add existing globally scoped files to it, remove files from it, or move application files between global applications.
-   **[Legacy - Automatic recovery of draft records](c_AutomaticRecoveryOfDraftRecords.md)**  
Studio can maintain a version of any open existing record with unsaved changes. Users can recover unsaved changes when their user session ends unexpectedly due to network latency, session timeout, or service interruption.
-   **[Legacy - Source Control integration](c_SourceControlIntegration.md)**  
Enable application developers to integrate with a Git Source Control repository. Save and manage multiple versions of an application from a non-production instance.

**Parent Topic:**[Building pro-code applications](../../custom-application/reference/building-pro-code-applications.md)

**Related topics**  


[Contextual development environment](c_ContextualDevelopmentEnvironment.md)

