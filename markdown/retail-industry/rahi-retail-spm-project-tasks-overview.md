---
title: Project tasks in Retail
description: Store associates and managers can view and act on the project work behind a store opening, closing, renovation, or relocation without leaving the Retail.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-spm-project-tasks-overview.html
release: brazil
topic_type: concept
last_updated: "2026-09-17"
reading_time_minutes: 5
keywords: [OCRR, project task, customer project, App SPM Retail]
breadcrumb: [Retail]
---

# Project tasks in Retail

Store associates and managers can view and act on the project work behind a store opening, closing, renovation, or relocation without leaving the Retail.

**Note:**

*SPM Retail Suite and Retail are separate applications, each deployable on its own, and this feature is the integration between them. SPM Retail Suite remains where the project is planned and tracked, Retail becomes where store-level tasks are worked. SPM Retail Suite does not require Retail.*

A store opening, closing, renovation, or relocation is planned at headquarters as a project in Retail Strategic Portfolio Management Suite. The project breaks the work down into project tasks, and the tasks for a particular store appear in Retail so that the store team can complete them. Store personas see the project work for their own store. They act on the tasks assigned to them and record progress where they manage their other work.

Project and project task records stay owned by the Customer Service Management \(CSM\) and Retail Strategic Portfolio Management Suite applications. Retail reads those records and presents them to store personas without adding tables, roles, or access control rules of its own. The project data that store teams act on is the same data that headquarters plans with. For information about creating and managing the projects themselves, see [Explore retail projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/explore-retail-projects-spm-r.md).

## Where project tasks appear

Project tasks appear in two places, and the tasks are the same records in both:

-   **[Find a project task in the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-view-projects-portal.md)**

    Store personas open the **Projects** category for their store, drill into a project, and open a project task. To act on it, see [Assign or close a project task in the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-act-on-tasks-portal.md).

-   **[Find a project task in Retail Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-view-projects-mobile.md)**

    Store personas reach project tasks either through their store details or through the **Tasks** filter in **My Work**. To act on a task, see [Assign or close a project task in Retail Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-act-on-tasks-mobile.md).


The experience is available only when the App SPM Retail plugin is active. When the plugin isn't active, the project and project task surfaces don't appear in the portal or the mobile application. There is no separate setting to turn the feature on or off.

## How project tasks differ from in-store operations tasks

A store opening, closing, renovation, or relocation involves work across several teams, such as legal, finance, procurement, and operations. Part of that work happens in the store itself. Project tasks and in-store operations tasks both reach store teams through Retail, but they are different records:

-   A project task belongs to a headquarters project for a store life cycle event, such as opening or closing a store. The project manager authors it, and it stays part of the project schedule.
-   An in-store operations task supports day-to-day store activity and is usually tied to a store case. For more information, see [In-store operations case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-retail-in-store-operations.md).

A project task isn't copied or converted into an in-store task. The store team acts on the project task itself, so the project manager sees store progress in the project without asking for a separate status update.

## What controls the project tasks a store persona sees

Two rules determine whether a project task reaches a store persona:

-   The project manager decides which project tasks the store team can see by setting the **Visible to customer** field on each project task. A project task without this field set doesn't appear in the portal or the mobile application.
-   Project tasks are scoped to the retail organization that a store persona belongs to. A persona associated with one store doesn't see the project tasks of another store.

Record-level access to project and project task records is owned by the Customer Service Management \(CSM\) and Retail Strategic Portfolio Management Suite applications. Retail adds no access control rules or query rules of its own on those tables. Its portal lists filter on the **Visible to customer** field as well, so an unflagged task is excluded before the list reaches the browser.

A store persona also needs the right roles. Access requires a retail contributor or fulfiller responsibility together with a project stakeholder role, scoped to the store that the persona belongs to. Which surfaces a persona reaches, and which actions they can take, depend on which stakeholder role they hold. For the full breakdown, see [Roles and visibility for project tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-roles.md).

## Reference information

For the tables and fields behind these surfaces, including the three fields that Retail writes, see [Project task data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-data-model.md).

## Related links

-   [Explore retail projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/explore-retail-projects-spm-r.md)
-   

-   **[Make project tasks available to a store team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-project-tasks-enable.md)**  
Install the App SPM Retail plugin and give your store personas the roles and organization membership they need before project tasks appear in Retail.
-   **[Find a project task in the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-view-projects-portal.md)**  
Open the projects for your store in the Retail Portal and drill into the project task you want to work on.
-   **[Find a project task in Retail Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-view-projects-mobile.md)**  
Reach the project tasks for your store from your store details or from **My Work**, and open the one you want to work on.
-   **[Assign or close a project task in the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-act-on-tasks-portal.md)**  
Comment on a project task, assign it to someone in your store, or close it when the work is done.
-   **[Assign or close a project task in Retail Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-spm-act-on-tasks-mobile.md)**  
Comment on a project task, assign it, or close it from the task screen in Retail Mobile.

