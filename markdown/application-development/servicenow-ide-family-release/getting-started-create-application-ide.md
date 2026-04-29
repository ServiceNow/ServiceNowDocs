---
title: Getting started: Create your first application in the ServiceNow IDE
description: Get started in the ServiceNow IDE by creating an application that you can develop in source code, pushing it to a remote repository, and cloning it on another instance.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Getting started: Create your first application in the ServiceNow IDE

Get started in the ServiceNow IDE by creating an application that you can develop in source code, pushing it to a remote repository, and cloning it on another instance.

The ServiceNow IDE is an implementation of Visual Studio Code for the Web on the ServiceNow AI Platform. With the ServiceNow IDE, you can get started building applications quickly using familiar tools and industry-standard development practices. For an overview of the ServiceNow IDE user interface, see [ServiceNow IDE user interface](servicenow-ide-user-interface.md#).

## Tutorial overview

In this tutorial, you complete the following tasks to familiarize yourself with developing a new application in source code from the ServiceNow IDE:

-   Create an application that supports development in source code.
-   Configure basic authentication and connect your application in the ServiceNow IDE to a remote Git repository and then push your application to the repository.
-   Create a simple table for a to-do list using ServiceNow Fluent APIs.
-   Install a third-party library and use its code in a JavaScript module.
-   Clone the application from the remote Git repository onto another instance.

Afterward, you should be ready to take the basic application you create and continue learning to develop it into a more complex application that meets your requirements.

## Before you begin

You should have access to the following items to complete this tutorial:

-   A non-production instance on the Xanadu release or later with ServiceNow IDE version 2.0.4 or later installed. To complete the last part of the tutorial by cloning the application to another instance, you need access to a second non-production instance. Personal developer instances \(PDIs\) are supported and can be obtained from [developer.servicenow.com](http://developer.servicenow.com). For more information, see [Install or update the ServiceNow IDE](../task/install-servicenow-ide.md).
-   A user with the admin role on both instances.
-   A Git provider such as GitHub, GitLab, Bitbucket, or Azure Repos. This tutorial demonstrates using GitHub.

-   **[Tutorial part 1: Create an application in the ServiceNow IDE](../task/tutorial-create-application-ide.md)**  
Create an application that you can develop in source code in the ServiceNow IDE.
-   **[Tutorial part 2: Initialize a repository for your application](../task/tutorial-initialize-repository-ide.md)**  
Initialize a local Git repository for an application in the ServiceNow IDE and push it to a remote Git repository in GitHub to manage the application in source control.
-   **[Tutorial part 3: Define a table in ServiceNow Fluent code](../task/tutorial-define-table-fluent-ide.md)**  
Create a table and reference it in sample script definitions using the ServiceNow Fluent APIs.
-   **[Tutorial part 4: Install and use a third-party library](../task/tutorial-install-third-party-library-ide.md)**  
Install a third-party library from Node Package Manager \(npm\) and use it in a JavaScript module.
-   **[Tutorial part 5: Clone the application on a different instance](../task/tutorial-clone-application-ide.md)**  
Clone the application from the remote repository to develop it on another instance.
-   **[Tutorial part 6: Learn more about the ServiceNow IDE](../reference/tutorial-next-steps-ide.md)**  
Learn more about the ServiceNow IDE to develop more complex applications.

**Parent Topic:**[Exploring the ServiceNow IDE](exploring-servicenow-ide.md)

**Related topics**  


[ServiceNow IDE user interface](servicenow-ide-user-interface.md#)

