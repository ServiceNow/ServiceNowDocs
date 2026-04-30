---
title: Business continuity planning
description: Business continuity planning helps you enact and mitigate risk at the time of an event. You can address and plan on the primary scope of the activities, documentation, loss scenarios, recovery teams, approvals, and so on. You can then configure a structured workflow of your business continuity planning tasks in BCM UIB Workspace.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Business continuity planning

Business continuity planning helps you enact and mitigate risk at the time of an event. You can address and plan on the primary scope of the activities, documentation, loss scenarios, recovery teams, approvals, and so on. You can then configure a structured workflow of your business continuity planning tasks in BCM UIB Workspace.

When you create a comprehensive business continuity plan for different possible disruptive scenarios, your organization is equipped to face a crisis or any adverse situation.

## Steps involved in creating a business continuity plan

Typically, the following steps involved in creating a business continuity plan:

-   The BCM program manager or planner creates a business continuity plan either from the Home page or the Planning record page in the List view of the BCM UIB Workspace.
-   The BCM program manager or planner adds additional details for the business continuity plan such as its scope, documentation section, recovery teams, related plans, and so on.
-   The business impact analysis owner reviews the information and submits the analysis for a review and approval to the business manager for services or IT manager for applications respectively.
-   The business manager, IT manager, or BCM lead review the details of the business continuity plan and approve it.
-   The approved business continuity plan is moved to **Approved** and later, it is moved to the **Archived** state.
-   The business continuity plan owner can generate the PDF of the plan and save a copy for reference.

A typical business continuity plan workflow is shown in the following example:

![Business continuity plan workflow.](../image/bcp-lifecycle.png)

## Setup tasks for business continuity planning

If you are the BCP administrator, you can view [Setup for a business continuity plan](bcp-admin-tasks.md) for information on the BCP setup tasks.

## Creating a business continuity plan in Business Continuity Workspace

if you are the business continuity plan owner, you can create a business continuity plan in Business Continuity Workspace by using one of the following options:

-   You can navigate to the **Planning** tab in the Home page and select **Create BCP** as shown in the following example.

    ![Planning tab in the Home page.](../image/bcp-homepage-uib.png)

    For the description of the cards and action buttons in the **Planning** tab of the Home page, see [Home page view](home-page-uib-ws.md).

-   You can also navigate to the List view and select **New** in the Planning records.

To create a business continuity plan in Business Continuity Workspace, see [Create a business continuity plan](../task/create-bcp-plan-in-uib-ws.md). For information on managing tasks related to a business continuity plan, see [Structured workflows for BCPs](bcp-tasks-performed-by-bcp-owner.md).

-   **[Assets and plans related to BCP](related-assets-related-plans.md)**  
You can identify the assets and plans related to a business continuity plan. You can then recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.
-   **[Recovery teams, loss scenarios, and recovery tasks](recovery-teams.md)**  
Business continuity planning workspace guides you to complete your business continuity plan. You can create a recovery team, define roles for the users, and direct the team to execute the plan. When you create a continuity plan for a department or a business unit, it is necessary to identify the loss scenarios to the business continuity plan.
-   **[Use cases for business continuity planning](bcp-use-cases.md)**  
This section describes the common use cases that are used for business continuity planning in the Business Continuity Management application. You can deploy these use cases individually or you can combine them to meet your specific needs.

**Parent Topic:**[Exploring Business Continuity Management](exploring-bcm.md)

