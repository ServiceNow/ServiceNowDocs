---
title: View reports on authorization boundary elements
description: Use the authorization boundary overview page to define the parameters of a security measure for an organization.
locale: en-US
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# View reports on authorization boundary elements

Use the authorization boundary overview page to define the parameters of a security measure for an organization.

## Before you begin

Role required:

-   sn\_irm\_cont\_auth.authorization\_official
-   sn\_irm\_cont\_auth.information\_owner
-   sn\_irm\_cont\_auth.info\_system\_sec\_manager
-   sn\_irm\_cont\_auth.info\_system\_sec\_officer
-   sn\_irm\_cont\_auth.sec\_control\_assessor
-   sn\_irm\_cont\_auth.system\_owner
-   sn\_irm\_cont\_auth.scheduler
-   sn\_irm\_cont\_auth.system\_user
-   sn\_irm\_cont\_auth.admin
-   sn\_irm\_cont\_auth.executive\_read

## About this task

For example, your organization might have many data centers. You can define a parameter within a boundary, for example `Application servers in San Diego data center`. Setting this boundary and parameter enables you to monitor the objects within the boundary and set the scope.

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and then select the lists icon \(![Lists icon.](../image/ws-list-icon.png)\).

2.  From the Authorization boundaries in the RMF list on the left pane, select an authorization boundary record on the right pane.

    The boundary overview page displays all the authorization packages that are available within the boundary. However, when you select the sidebar, it displays an active package.

    ![Authorization boundary overview page.](../image/auth-bound-overview.png)

3.  Select the sidebar icon \(![Sidebar icon.](../../grc-workspace-compliance/image/pc-ws-sidebar-icon.png)\).

    The Highlighted details section displays:

    -   The name of the active package, its state, and impact. If there’s an active package already existing for the boundary, you can’t create another package for the boundary.
    -   The link to the package, if selected, helps you to navigate to the associated, active authorization package.
    -   The users who are directly responsible and have a key role to play in updating the authorization boundary.
4.  To create another package, select the Authorization Packages related list and deactivate the existing package by selecting false in the **Active** column of the package.

    This action deactivates the current package, and you can then create a package by selecting **New**. A boundary having only one active package behavior is guided by NIST 800-53 revision 5.

    Within this authorization boundary, you can set the boundary filters, such as asset tags as computers. With this set filter condition, all the elements that fulfill the filter condition get added as system elements.

5.  To view the relationship between the selected authorization boundary and all its associated objects in a distinct visualization, select **360° view**.

    **360° view** is added in the Overview pages of Authorization Boundary, Authorization Package, Control, Control objective, Control overlays, Control test, Test template, Test plan, Engagements, and in the Details pages of Indicator, Indicator Template, and POA&amp;Ms.

    ![360° view of all elements associated with the authorization boundary.](../image/abound-cam-ws-360-view.png)


## What to do next

Select the name of the Active package in the side bar to navigate to the Authorization Package overview page.

**Parent Topic:**[Continuous authorization and monitoring tasks in the CAM Workspace](../concept/cam-ws-continuous-auth-monitor.md)

