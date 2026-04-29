---
title: Parts of an application in ServiceNow
description: Applications in ServiceNow have tables, UI elements, application files, integrations, and dependencies, all with a layer of security through the entire app.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Building apps in ServiceNow, Getting Started guide for developers, Building applications]
---

# Parts of an application in ServiceNow

Applications in ServiceNow have tables, UI elements, application files, integrations, and dependencies, all with a layer of security through the entire app.

## Parts of an application

![Infographic showing how applications contain tables, UI elements, files, integrations, and dependencies. For a text description, refer to the following content.](../image/parts-of-an-app.png)

-   **Tables** are the foundation of ServiceNow applications, where data is stored and new records are created.
-   **UI elements** enable users to interact with your application. Menus, modules, lists, and forms are just some of the UI elements you can add to an application.
-   **Application files** such as business rules, UI actions, and workflows make up the bulk of your application. They define how aspects of the application function and how people interact with it.
-   **Integrations** such as REST and SOAP Web services connect your application to third-party systems and use them on the ServiceNow AI Platform.
-   **Dependencies** are the elements of other applications that this application is dependent on. These are listed as a related list in the application record.

## Custom application record

The custom application record defines and identifies an application and all its associated artifacts.

It's similar to a system dictionary record for a table or column in that it stores the most current configuration of an application. The system automatically creates a custom application record during the application creation process. You can use this record to perform the following tasks.

-   Change the application name
-   Change the application version
-   View the scope the system uses to identify application files and configuration records
-   Enable scoped administration
-   Manage design and runtime access to the application
    -   Select what JavaScript standards the application supports
    -   Select how the system tracks runtime API operations
    -   Permit or restrict access to tables from other applications
-   Monitor or enforce subscriptions
-   Select the default menu in which to display application modules
-   Set the user role required to access the application
-   Add or update a logo
-   View all application files
-   View resources from other applications on which the application depends
-   View the run-time resource to which the application has been granted access
-   View the design-time resources to which the application has been granted access

**Parent Topic:**[Overview of building apps in ServiceNow](overview-building-apps-in-servicenow.md)

