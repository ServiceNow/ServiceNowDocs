---
title: Monitoring and managing security from the CAM Workspace Home page
description: The CAM Workspace is a centralized hub where you can continuously monitor and manage compliance of users and systems with the NIST Risk Management Framework to ensure adherence to your security policies and guidelines.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2025-07-29"
reading_time_minutes: 3
breadcrumb: [CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Monitoring and managing security from the CAM Workspace Home page

The CAM Workspace is a centralized hub where you can continuously monitor and manage compliance of users and systems with the NIST Risk Management Framework to ensure adherence to your security policies and guidelines.

## Accessing the Home page

Navigate to **All** &gt; **CAM Workspace**.

![CAM home page displaying the overall status of the CAM objects.](../image/cam-ws-home-page.png)

## Overview section

Authorization boundaries define the scope of a particular system that can be continuously managed and monitored using the CAM application.

-   **Total boundaries**

    The donut chart displays the relative proportion of total boundaries present in your organization based on operational status.

-   **Packages by step**

    The bar chart displays the count of packages in each NFT step. However, there’s only one package that is active for the selected boundary.

-   **Mission critical boundaries**

    The bar chart displays the count of mission-critical boundaries by operational status.

-   **Packages by impact**

    Active packages are characterized as low, medium, or high impact and in NFT states such as Select, Implement, Assess, Authorize, and Monitor.

-   **Aging of Packages**

    Track the ageing of the package at different steps, showing you for how many days the authorization package stayed in each step. If the package moves back to a previous step, the widget will clear the number of days recorded for the subsequent steps. Only the days spent in the current step and the previous step are displayed.


## Tracking section

Tracks the active controls, control tests, and plan of action and milestones \(POA&amp;Ms\) as separate widgets to give an overall status of these CAM objects.

-   **Controls report**

    Total count of active, compliant, non-compliant controls. The pie chart displays the status proportionally.

-   **Control tests report**

    Total count of active and overdue control tests and count of control tests in the Open, Work in Progress, and Review statuses. For these CAM control tests, the parent is an engagement and the engagement is associated with the authorization package.

-   **POA&amp;Ms report**

    Counts of open and overdue POA&amp;Ms and the stacked horizontal chart depicts their priority status. POA&amp;Ms are issues related to an authorization package, or control, engagement, control test of the package.


## Tasks section

Displays your and your group's pending tasks. Select **View all tasks** to open the Tasks landing page as described in [Monitor and manage CAM tasks](../task/tasks-page-cam-ws.md).

CAM roles that are required for particular tasks are listed in [CAM user roles](../../grc-cam/reference/cam-roles-list.md).

## Required roles

-   Authorization Official \(sn\_irm\_cont\_auth.authorization\_official\), to approve and update authorization packages.
-   CAM admin \(sn\_irm\_cont\_auth.admin\), to perform all system admin tasks in CAM.
-   Executive Reader \(sn\_irm\_cont\_auth.executive\_read\), to read CAM Workspace.
-   Information Owner \(sn\_irm\_cont\_auth.information\_owner\), to update information types of an authorization package.
-   Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\), to conduct information system security management activities.
-   Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\), to verify that the appropriate operational security posture is maintained for an information system.
-   Reader \(sn\_irm\_cont\_auth.reader\), to read CAM Workspace.
-   Scheduler \(sn\_irm\_cont\_auth.scheduler\), to run all scheduled jobs for the application.
-   Security Control Assessor \(sn\_irm\_cont\_auth.sec\_control\_assessor\), to conduct a thorough assessment of the management, operational, and technical security controls of an information system.
-   System Owner \(sn\_irm\_cont\_auth.system\_owner\), to procure, develop, integrate, modify, operate, and maintain an information system.
-   System User \(sn\_irm\_cont\_auth.system\_user\), to update authorization boundaries, set boundary filter, elements, milestones, and acceptance tasks.

## Access the Home page of the CAM Workspace

To access the Home page, navigate to **All** &gt; **CAM Workspace**.

**Parent Topic:**[Continuous authorization and monitoring tasks in the CAM Workspace](cam-ws-continuous-auth-monitor.md)

