---
title: Schedule Planning
description: Manage space assignments to help employees head back to the office.
locale: en-US
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 4
breadcrumb: [Explore, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Schedule Planning

Manage space assignments to help employees head back to the office.

## Schedule Planning overview

Schedule Planning provides a streamlined experience for project managers to assign and manage employee assignments based on project time frames.

As a project manager, you can do the following:

-   View a list of employees assigned to your project
-   View a list of spaces allocated for your project
-   Create a schedule plan for a specific period to map spaces to the employees
-   Execute a schedule plan to assign spaces to the Workplace Profile of the users

## Accessing Schedule Planning

You must install the following plugins to use the Schedule Planner module:

-   Workplace Central
-   Workplace Space Management

You can install the plugins from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). You can also visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information of all the released apps, see the [ServiceNow Store release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Important:** You must set a value for the **sn\_wsd\_core.ALLOCATION\_TYPE** property to enable schedule planning.

To access the Schedule Planner, navigate to **All** &gt; **Workplace Central**, then select the **Schedule Planner** module in the workspace.

![Schedule Planner dashboard with information about schedule plans, departments, users, and allocations.](../images/schedule-plan-dashboard.png)

As a project owner, you can view the created schedule plans, projects assigned to you, and the spaces and users assigned to the projects. You can create a schedule plan or edit existing schedule plans. For more information, see [Working with Schedule Planning](working-with-schedule-planning.md).

**Note:** A project owner can create schedule plans for the projects that are assigned to them. Projects can be assigned to a user from the following fields:

-   **Primary contact** field of the department
-   **Manager** field of the cost center
-   **Managed by group** or **Managed by** field of the workplace entity

Only one of the fields is considered for the project list based on the **sn\_wsd\_core.ALLOCATION\_TYPE** property.

## Schedule Plan states

A schedule plan can be in one of the following states:

-   Draft: Project owner has created a new schedule plan but has not filled the details or started the workplace assignments.
-   In Progress: Project owner has filled the schedule plan details and the workplace locations are being assigned to the users.
-   Published: Schedule plan is created and the workplace locations are assigned to all the users.
-   Complete: Schedule plan has reached the specified end date and the workplace location assignments are made inactive.
-   Cancelled: Project owner has cancelled the schedule plan and the workplace location assignments are made inactive.

**Note:** The **Complete the lapsed schedule plan** job runs every day to check which schedule plans have reached the end date and move them to the **Complete** state.

**Parent Topic:**[Exploring Workplace Space Management](../../workplace-space-management/concept/explore_wsm.md)

**Parent Topic:**[Explore Workplace Central](workplace-central.md)

**Related topics**  


[Space Optimization](space-optimization.md)

[Scenario Planning](scenario-planning.md)

[Allocation - types, setting, and impact](../../workplace-space-management/reference/setting-an-allocation-and-its-impact.md)

[Lists module](wsd-lists-module.md)

[Workplace Analytics](workplace-analytics.md)

[Space Planning](space-planning.md)

[Space Optimization](space-optimization.md)

[Scenario Planning](scenario-planning.md)

[Space assistance](space-assistance.md)

[Event Planner](event-planner.md)

[Move Management](move-mgmt.md)

[Case management](case-management-workspace.md)

[Kiosk Indoor Mapping](kiosk-indoor-mapping.md)

