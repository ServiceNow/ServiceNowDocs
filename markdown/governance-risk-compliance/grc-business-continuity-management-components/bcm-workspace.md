---
title: BCM Configurable Workspace
description: Starting with version 5.x.x, the Business Continuity Management application supports BCM Configurable Workspace. You can perform your business continuity tasks with an intuitive functionality in BCM Configurable Workspace.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# BCM Configurable Workspace

Starting with version 5.x.x, the Business Continuity Management application supports BCM Configurable Workspace. You can perform your business continuity tasks with an intuitive functionality in BCM Configurable Workspace.

## Enhancements in the BCM Configurable Workspace

BCM Configurable Workspace \(also known as Business Continuity Workspace\) offers an enhanced and simplified user experience for its users. The BCM application users can take advantage of the enhancements in BCM Configurable Workspace over BCM classic Workspace:

1.  Manage the crisis events, business impact analysis, planning, and exercises from an interactive dashboard in the Home page.
2.  Monitor your individual and team tasks in the My tasks page and act on your pending tasks quickly.
3.  Respond to the alerts in Crisis map and manage the recovery tasks effectively.
4.  Visualize 360-degree relationship data for your business impact analysis, planning, exercises, and crisis events records and get a complete overview of all dependencies.

The Business Continuity Workspace in the classic Workspace is automatically updated to point to BCM Configurable Workspace. For information on BCM classic Workspace, see [Using BCM Classic Workspace](mainitain-bcm-with-classic-workspace.md).

## Configurable and role-driven Workspace

The BCM Configurable Workspace is configurable and role-driven, offering a unique experience tailored to each user or role in your organization. Logging in with specific user roles provides access to different functions and corresponding user interface views.

For more information on the user roles in the BCM application, see [Components installed with Business Continuity Management](../reference/installed-with-bcm.md#).

For more information on the store apps, see [Business Continuity Management and ServiceNow Store](bcm-and-store.md).

## Support for the BCM Classic Workspace

Starting with the Vancouver release, the BCM Configurable Workspace provides the latest user experience.

The BCM Classic Workspace is an obsolete user interface that is not compatible with the new features and enhancements introduced with the Xanadu release. If you continue to use the BCM Classic Workspace after the upgrade, you may encounter issues and errors that will not be supported by ServiceNow®.

To avoid any disruptions, transitioning to the BCM Configurable Workspace before or immediately following the Xanadu release offers the latest functionality and the best user experience.

## Users of the BCM application

The BCM application is the central workbench for these types of users:

-   BCM administrators
-   BCM managers
-   BCM planners
-   BCM contributors
-   BCM viewers
-   Business users
-   IT application owners

## Navigating to the BCM Configurable Workspace

When you log in to the Business Continuity Management application with a specific user role, you can open the Business Continuity Workspace using one of these options:

-   First option: Navigate to **Workspaces &gt; Business Continuity Workspace** in the application instance as shown in the example.

    ![Workspaces menu for Business Continuity Workspace.](../image/bcm-workspace-menu.png)

-   Second option: Navigate to **All &gt; Business Continuity &gt; Business Continuity Workspace** in the application instance as shown in the example.

    ![Application navigator menu for Business Continuity Workspace.](../image/bcm-application-nav-menu.png)


**Note:** The Business Continuity Workspace in the classic Workspace view is automatically updated to navigate to BCM Configurable Workspace.

## Icons in the Business Continuity Workspace

When you launch Business Continuity Workspace, the Workspace sidebar includes icons for these components.

-   Home page: Displays key continuity tasks in a single-pane view.
-   Tasks page: Displays assigned tasks for the logged‑in user. For more information, see [My tasks page view](my-tasks-page-uib-ws.md).
-   Lists: Displays counts and statuses for BIA, planning, exercise, and crisis event records. For more information, see [List view](list-view-uib-ws.md).
-   Crisis map: Displays real-time threat alerts from different locations in a map view. For more information, see [Crisis map view](crisis-map-uib-ws.md).

## Managing functional components

Manage the functional components of the BCM application in the BCM Configurable Workspace:

-   **Business impact analysis**

    A business impact analysis helps you identify high‑risk assets and measure the consequences of disruptions. You can estimate recovery time, evaluate dependencies, and assess business and technical impacts. For details on creating and managing BIAs, see [Business impact analysis](bia-uib.md) and [Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md).

-   **Business continuity planning**

    Continuity planning enables you to prepare recovery strategies, documentation, and loss scenarios. You can also define recovery teams and associate related plans. For more information, see [Business continuity planning](bcp-uib.md) and [Structured workflows for BCPs](bcp-tasks-performed-by-bcp-owner.md).

-   **Exercise management**

    Exercises simulate crisis conditions and help validate continuity plans. You can manage events, review outcomes, and refine plans for future scenarios. For more information, see [Structured workflows for exercises](performing-tasks-to-manage-exercise-events.md).

-   **Crisis management**

    Crisis management enables you to respond to actual disruptions, prioritize activities, and manage actions that reduce operational impact. For details, see [Crisis events](crisis-management-uib.md) and [Structured workflows for crisis events](perform-tasks-to-manage-crisis-events.md).

    **Note:** For setting up Business Continuity Management, see [General administration setup for BCM](set-up-bcm-bcmadmin-tasks.md).


