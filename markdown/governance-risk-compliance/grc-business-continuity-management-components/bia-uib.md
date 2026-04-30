---
title: Business impact analysis
description: Business impact analysis is a structured process where you assess the impact categories and dependencies and predict the consequences of a disruption on a business process or business function.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Business impact analysis

Business impact analysis is a structured process where you assess the impact categories and dependencies and predict the consequences of a disruption on a business process or business function.

## An integral component of your business continuity plan

A business impact analysis is an integral component of the business continuity plan for an organization. It includes information on the important information systems and a planning component that includes the strategies for minimizing your risks.

Business managers have to make challenging decisions that can contribute to overall business growth. Sometimes, an unforeseen event or a disruption can cause disruptive effects. Performing a business impact analysis helps your business to mitigate these concerns. By evaluating the potential impact of an event or a decision, your business can predict future consequences and recover from setbacks successfully.

For information on the use cases for business impact analysis, see [Use cases for business impact analysis](bia-use-cases.md).

## Steps involved in creating a business impact analysis

Typically, the following steps involved in creating a business impact analysis:

-   The business impact analysis owner creates a business impact analysis either from the Home page or the business impact analysis record page in the List view of the BCM UIB Workspace.
-   The BIA owner adds additional details for the business impact analysis on the **Details** tab.
-   Different users of the BCM application respond to the assessment questionnaire for the business impact analysis on the **Assessment** tab.
-   Based on the responses received, the BCM application calculates the recovery time objective \(RTO\), recovery point objective \(RPO\), and dependencies for the business impact analysis.
-   The business impact analysis owner reviews the information and submits the analysis for a review and approval to the business manager for services or IT manager for applications respectively.
-   The business manager, IT manager, or BCM lead review the details of the business impact analysis and approve or reject it.
-   An approved business impact analysis is moved to **Approved** and later, it is moved to the **Archived** state.
-   The business impact analysis owner can generate the PDF of the analysis and save a copy for reference.

A typical business impact analysis workflow is shown in the following examples:

![BIA workflow.](../image/bia-lifecycle.png)

![BIA workflow for different roles.](../image/bia-workflow-w.png)

## Setup tasks for the business impact analysis administrator

If you are the business impact analysis administrator, you can view [Setup for a business impact analysis](bcm-admin-tasks.md) for information on the setup tasks.

## Creating a business impact analysis in Business Continuity Workspace

if you are the business impact analysis owner, you can create a business impact analysis in Business Continuity Workspace by using one of the following options:

-   You can navigate to the **Business impact analysis** tab in the Home page and select **Create BIA** as shown in the following example.

    ![Create BIA from the Home page.](../image/bia-home-page.png)

    For the description of the cards and action buttons in the **Business impact analysis** tab of the Home page, see [Home page view](home-page-uib-ws.md).

-   You can also navigate to the List view and select **New** in the Business Impact Analysis records as shown in the following example.

    ![Create BIA from the record page in the List view.](../image/list-view-bcm.png)


To create a business impact analysis in Business Continuity Workspace, see [Create a business impact analysis](../task/create-bia-in-uib-ws.md). For information on managing the tasks that are related to a business impact analysis, see [Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md).

-   **[Use cases for business impact analysis](bia-use-cases.md)**  
You can use the Business Continuity Management application to assess the impact of a downtime on your business services or processes and technical entities such as datacenters or applications. For creating a business impact analysis for your organization, you can refer to the common use cases that are used for managing the business continuity tasks.
-   **[Business impact analysis \(BIA\) templates](bia-templates.md)**  
The Business Continuity Management application provides pre-configured business impact analysis \(BIA\) templates for creating a business impact analysis. If you are the BCM or BIA administrator, you can use the **BIA Templates** module in the Business Continuity Management application. You can then select the type of the template, elements, impact categories, and so on, for the business impact analysis.
-   **[Grid configurations and categories](grid-configurations.md)**  
You can set up the grid configuration to render the BIA dependency assessment grid with configured columns. You can define the grid category such as Dependency Assessment for which the grid configuration is applicable.

**Parent Topic:**[Exploring Business Continuity Management](exploring-bcm.md)

