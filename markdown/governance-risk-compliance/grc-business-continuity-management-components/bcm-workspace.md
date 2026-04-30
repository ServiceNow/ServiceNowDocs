---
title: BCM Configurable Workspace
description: Starting with version 5.x.x, the Business Continuity Management application supports BCM Configurable Workspace. You can perform your business continuity tasks with an intuitive functionality in BCM Configurable Workspace.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# BCM Configurable Workspace

Starting with version 5.x.x, the Business Continuity Management application supports BCM Configurable Workspace. You can perform your business continuity tasks with an intuitive functionality in BCM Configurable Workspace.

## Enhancements in BCM Configurable Workspace

BCM Configurable Workspace \(also known as Business Continuity Workspace\) offers an enhanced and simplified user experience for its users. The BCM application users can take advantage of the following enhancements in BCM Configurable Workspace over BCM classic Workspace:

1.  Manage the crisis events, business impact analysis, planning, and exercises from an interactive dashboard in the Home page.
2.  Monitor your individual and team tasks in the My tasks page and act on your pending tasks quickly.
3.  Respond to the alerts in Crisis map and manage the recovery tasks effectively.
4.  Visualize 360-degree relationship data for your business impact analysis, planning, exercises, and crisis events records and get a complete overview of all dependencies.

The Business Continuity Workspace in the classic Workspace is automatically updated to point to BCM Configurable Workspace. For information on BCM classic Workspace, see [Using BCM Classic Workspace](mainitain-bcm-with-classic-workspace.md).

## Configurable and role-driven Workspace

The BCM Configurable Workspace is configurable and role-driven, offering a unique experience tailored to each user or role in your organization. Logging in with specific user roles provides access to different functions and corresponding user interface views.

For more information on the user roles in the BCM application, see [Components installed with Business Continuity Management](../reference/installed-with-bcm.md#).

For more information on the store apps, see [Business Continuity Management and ServiceNow Store](bcm-and-store.md).

## Support for BCM Classic Workspace

Starting with the Vancouver release, the BCM Configurable Workspace provides the latest user experience. Post Xanadu release, the BCM Classic Workspace is being prepared for future deprecation. Although the BCM Classic Workspace can still be used post Xanadu release via URLs, it will be hidden from the navigation. Using the BCM Configurable Workspace will ensure a smooth transition post Xanadu release.

The BCM Classic Workspace is an obsolete user interface that will not be compatible with the new features and enhancements introduced with the Xanadu release. If you continue to use the BCM Classic Workspace after the upgrade, you may encounter issues and errors that will not be supported by ServiceNow®.

To avoid any disruptions, transitioning to the BCM Configurable Workspace before or immediately following the Xanadu release offers the latest functionality and best user experience.

## Users of the BCM application

The BCM application is the central workbench for the following types of users:

-   BCM administrators
-   BCM managers
-   BCM planners
-   BCM contributors
-   BCM viewers
-   Business users
-   IT application owners

## Navigating to BCM Configurable Workspace

When you log in to the Business Continuity Management application with a specific user role, you can navigate to the Business Continuity Workspace by using one of the following options:

-   First option: Navigate to **Workspaces &gt; Business Continuity Workspace** in the application instance as shown in the following example.

    ![Workspaces menu for Business Continuity Workspace.](../image/bcm-workspace-menu.png)

-   Second option: Navigate to **All &gt; Business Continuity &gt; Business Continuity Workspace** in the application instance as shown in the following example.

    ![Application navigator menu for Business Continuity Workspace.](../image/bcm-application-nav-menu.png)


**Note:** The Business Continuity Workspace in the classic Workspace view is automatically updated to navigate to BCM Configurable Workspace.

## Icons in Business Continuity Workspace

When you launch Business Continuity Workspace, you can view the following icons in the side bar of the Workspace view.

-   Home page: Displays your business continuity tasks in a single pane view.
-   Tasks page: Displays an overview of the tasks for the logged-in user. For more information, see [My tasks page view](my-tasks-page-uib-ws.md).
-   Lists: Displays the count and status of the business impact analysis, planning, exercise, and crisis event records. For more information, see [List view](list-view-uib-ws.md).
-   Crisis map: Displays the real-time threat alerts from different locations in a map view. For more information, see [Crisis map view](crisis-map-uib-ws.md).

## Managing functional components in BCM Configurable Workspace

You can manage the following functional components of the BCM application in BCM Configurable Workspace:

-   **Business impact analysis**

    Performing a business impact analysis helps you to identify high risk assets and determine the impact of disruption on your critical business functions or services. By analyzing the impact, you can estimate the time of recovery to resume business and also focus on the consequences of incidents and disruptions.

    For information on creating a business impact analysis, see [Business impact analysis](bia-uib.md). For information on the structured workflow tasks for business impact analysis, see [Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md).

-   **Business continuity planning**

    Planning your business continuity tasks enables you to develop continuity and recovery plans for critical business processes and IT functions. Disaster recovery enables you to protect, recover, and restore the organizational critical data and its technology systems. You can also develop a business continuity strategy for each activity.

    For information on creating a business continuity plan, see [Business continuity planning](bcp-uib.md). For information on the structured workflow tasks for business continuity planning, see [Structured workflows for BCPs](bcp-tasks-performed-by-bcp-owner.md).

-   **Exercise management**

    Creating an event to exercise the plan in a simulated crisis helps you to validate your business continuity plans by continuous testing. You can then improve the effectiveness of the plans and usability during a simulated crisis.

    For information on the exercise events, see [Exercises](exercise-management-uib.md). For information on the structured workflow tasks for exercise management, see [Structured workflows for exercises](performing-tasks-to-manage-exercise-events.md).

-   **Crisis management**

    Managing an actual crisis event helps you to mitigate the negative impact of a disruption to the business system. You can then prioritize the actions and apply the right strategy to minimize the downtime.

    For information on the crisis events, see [Crisis events](crisis-management-uib.md). For information on the structured workflow tasks for crisis management, see [Structured workflows for crisis events](perform-tasks-to-manage-crisis-events.md).

    **Note:** For setting up Business Continuity Management, see [General administration setup for BCM](set-up-bcm-bcmadmin-tasks.md).


-   **[Home page view](home-page-uib-ws.md)**  
The Home page in Business Continuity Workspace serves as the landing page of the BCM application.
-   **[My tasks page view](my-tasks-page-uib-ws.md)**  
My tasks page displays a single-pane view of your pending tasks, tasks assigned to your user group, and the tasks that are on your watchlist.
-   **[List view](list-view-uib-ws.md)**  
The List view in BCM UIB Workspace displays the scope of all BCM functional components and their key metric information.
-   **[Crisis map view](crisis-map-uib-ws.md)**  
When you install the GRC: Crisis map application in your instance, you can view the Crisis map icon in the List view. You can integrate the Crisis map application with BCM and analyze real-time threat alerts from different locations in a map view. You can then take remedial actions and manage the crisis events from Business Continuity Workspace.

**Parent Topic:**[Exploring Business Continuity Management](exploring-bcm.md)

