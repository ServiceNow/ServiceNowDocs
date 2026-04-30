---
title: Exploring Vendor Management Workspace
description: Use Vendor Management Workspace to monitor metrics and analyze your vendor's health from a single user interface. Gain insights when you compare top-performing vendors and track compensation your vendors owe you when they breach the service agreement.
locale: en-US
release: yokohama
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Vendor Management Workspace, IT Service Management]
---

# Exploring Vendor Management Workspace

Use Vendor Management Workspace to monitor metrics and analyze your vendor's health from a single user interface. Gain insights when you compare top-performing vendors and track compensation your vendors owe you when they breach the service agreement.

## Vendor Management Workspace overview

The video provides an overview of Vendor Management Workspace.Video that shows the overview of Vendor Management Workspace 

As a vendor manager, you can:

-   Organize your vendors into vendor KPI groups and analyze vendor performance.
-   Gain insights into how your vendors are performing in comparison with other vendors in your organization.
-   Track the compensation that you vendors owe for breaching service agreements.

## Vendor Management Workspace users

|User|Description|
|----|-----------|
|[Vendor admin](../reference/installed-w-vendor-manager-configurable-workspace.md)|Vendor admins can add vendors and set up vendor metrics.|
|[Vendor manager](../reference/installed-w-vendor-manager-configurable-workspace.md)|Vendor managers use Vendor Management Workspace to evaluate vendor health.|
|[UI builder admin](https://www.servicenow.com/docs/access?context=security-roles&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|Using UI builder, UI builder admins can customize Vendor Management Workspace based on the users' needs.|

## Vendor Management Workspace workflow

![Infographic for Vendor Management Workspace workflow. The text that describes the flow follows this infographic.](../image/vendor-management-workspace-workflow.png)

In this workflow:

1.  Administrators activate Vendor Management Workspace. The application is installed after the Vendor Manager Workspace \(sn\_itsm\_vendor\) plugin is activated. Vendor administrators can then configure the application and vendor managers can use the application.

    **Note:** After the administrators activate Vendor Management Workspace, they can also customize Vendor Management Workspace using [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

2.  Vendor admins can create KPI groups so that vendor managers can track vendor metrics.
3.  Vendor admins and vendor managers can do any of the following:
    -   Integrate with other ServiceNow applications to assess vendors who use data from other applications.
    -   Generate vendor satisfaction assessment to measure stakeholder satisfaction.
    -   Create improvement initiatives to track tasks to improve a service, process, or a task.
    -   Create performance targets to set goals to achieve desired vendor scores.
4.  Vendor managers can do any of the following:
    -   Create service credits to track vendor breach of agreements.
    -   Create vendor tickets to track issues as they arise.
    -   Associate SLAs and service commitments with vendors to monitor how quickly vendors resolve issues.
    -   Analyze vendor metrics using the vendor KPI group data.
    -   Monitor vendor performance within a KPI group and assess them.

## Vendor Management Workspace benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Add vendors and set up vendor metrics to analyze their performance goals.|[Configuring Vendor Management Workspace](configuring-vendor-management-workspace.md)|[Vendor admin](../reference/installed-w-vendor-manager-configurable-workspace.md)|
|Monitor vendor metrics and evaluate vendor health using Vendor Management Workspace.|[Managing vendors using Vendor Management Workspace](using-vendor-management-workspace.md)|[Vendor manager](../reference/installed-w-vendor-manager-configurable-workspace.md)|
|Bring in data from other ServiceNow applications to assess the relationship with your vendors.|[Integrating Vendor Management Workspace with other ServiceNow applications](vendor-manager-workspace-integrations.md)|[Vendor admin](../reference/installed-w-vendor-manager-configurable-workspace.md)|
|Create custom web experience in Vendor Management Workspace based on your needs.|[Customize a Vendor Management Workspace page using UI Builder](../task/customize-vmw-page.md)|[Admin, Workspace admin, or UI builder admin](https://www.servicenow.com/docs/access?context=security-roles&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|

