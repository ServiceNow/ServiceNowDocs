---
title: Exploring Business Continuity Management
description: Learn how you can use the Business Continuity Management application to manage your business continuity tasks using predefined templates and workflows.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Business Continuity Management, Governance, Risk, and Compliance]
---

# Exploring Business Continuity Management

Learn how you can use the Business Continuity Management application to manage your business continuity tasks using predefined templates and workflows.

## Business Continuity Management overview

The Business Continuity Management application provides a framework to perform continuous management activities such as business impact analysis, business continuity planning, exercise management, and crisis management. The structured workflows in the Business Continuity Management application improve your organizational ability to respond to the issues and recover quickly from the disruptions.

## Business Continuity Management workflow

A typical workflow in the Business Continuity Management application involves the following steps for managing your business continuity tasks:

![BCM high level workflow.](../image/bcm-data-flow-lucid.png)

1.  An administrator downloads the Business Continuity Management application from ServiceNow Store.
2.  The BCM administrator sets up the Business Continuity Management application and the templates for performing the business continuity activities.
3.  The BCM program manager or business impact analysis \(BIA\) administrator creates a business impact analysis to determine the impact of a disruption on the business processes and IT applications. The BIA administrator also focuses on the consequences of incidents and estimates the time of recovery to resume normal business operations.
4.  The BCM program manager or BCM lead reviews the assessments and approves the business impact analysis.
5.  The BCM program manager or business continuity plan \(BCP\) administrator creates a business continuity plan and adds the relevant assets, scope, documentation, related plans, recovery teams, loss scenarios, and recovery tasks to it. The BCP administrator then sends an approval request to the BCM lead to review and approve the business continuity plan.
6.  The BCM program manager creates exercise events, tracks the assets and their dependencies, and approves the exercise events.
7.  The BCM program manager responds to the crisis events, tracks the assets and their associated dependencies, and manages the recovery tasks to mitigate the negative impact of a disruption.
8.  The BCM program manager manages the alerts from the Crisis map interface and initiates the response workflows to minimize the downtime.
9.  The BCM administrator or BCM program manager sends the emergency notifications in Everbridge notifications system and notifies the stakeholders about the crisis alerts.

## Business Continuity Management benefits

The Business Continuity Management application provides the following benefits:

|Benefit|Feature|Users|
|-------|-------|-----|
|Manage your business continuity activities from the interactive dashboard in the Home page.|[Home page view](home-page-uib-ws.md)|BCM program manager|
|Monitor your individual and team tasks from a single dashboard in the **My tasks** view.|[My tasks page view](my-tasks-page-uib-ws.md)|BCM program manager|
|Assess your critical business services and IT applications by creating a business impact analysis.|[Create a business impact analysis](../task/create-bia-in-uib-ws.md)|BCM program manager or BIA administrator|
|Prepare a business continuity plan with a response strategy and get it reviewed by the BCM leads and program managers.|[Create a business continuity plan](../task/create-bcp-plan-in-uib-ws.md)|BCM program manager or BCP administrator|
|Finalize your business continuity plan by continuously testing and exercising an event.|[Create an exercise](../task/start-exercise-event-in-uib-ws.md)|BCM program manager or BCM planner|
|Respond to an actual crisis event and manage the associated event tasks.|[Start a crisis event](../task/start-crisis-event-in-uib-ws.md)|BCM program manager or BCM planner|
|Respond to the alerts in Crisis map and set the recovery tasks into action to manage the alerts.|[Manage alerts from the map interface](../task/manage-alerts-in-crisis-map-interface-uib-ws.md)|BCM administrator or BCM program manager|
|Notify the stakeholders about the crisis alerts by sending emergency notifications in Everbridge.|[Sending notifications with Everbridge](ebn-collective-tasks.md)|BCM administrator or BCM program manager|

## Coral theme

Coral is now the default theme for the Business Continuity Workspace. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[BCM Configurable Workspace](bcm-workspace.md)**  
Starting with version 5.x.x, the Business Continuity Management application supports BCM Configurable Workspace. You can perform your business continuity tasks with an intuitive functionality in BCM Configurable Workspace.
-   **[Business impact analysis](bia-uib.md)**  
Business impact analysis is a structured process where you assess the impact categories and dependencies and predict the consequences of a disruption on a business process or business function.
-   **[Business continuity planning](bcp-uib.md)**  
Business continuity planning helps you enact and mitigate risk at the time of an event. You can address and plan on the primary scope of the activities, documentation, loss scenarios, recovery teams, approvals, and so on. You can then configure a structured workflow of your business continuity planning tasks in BCM UIB Workspace.
-   **[Element definitions and variables](element-definitions.md)**  
An element definition is a configuration item that is assessed in the business impact analysis. The element definitions are also recovered in the business continuity plan. If you have the administrator role, you can set up an element variable that is required for a particular dependency of an element.
-   **[Exercises](exercise-management-uib.md)**  
Exercises are used to provide continuous testing and improving of continuity plans. You can use the exercises to finalize your business continuity plan and improve its effectiveness and usability in an actual crisis event. You can manage your exercises in BCM UIB Workspace.
-   **[Crisis events](crisis-management-uib.md)**  
Managing a crisis event in BCM UIB Workspace helps you to minimize the downtime of critical business functions and processes across your organization. It is also used to minimize the financial, reputation, legal, and regulatory impact during a crisis event.
-   **[Crisis map interface](threats-feeds-alerts-crisis-map.md)**  
You can integrate Crisis map with the BCM application and initiate the response workflows for crisis management. After installing the Crisis map application, you can view the **Threat and Alert Data Feeds** module in your BCM application instance.
-   **[Emergency notifications in Everbridge](integrating-crisis-mgmt-with-everbridge-uib.md)**  
You can integrate Crisis Management in the BCM application with Everbridge notifications system. You can then send an emergency notification to an individual or a group of people alerting them of an impending emergency. It provides a one-way notification and two-way communication through properly established delivery channels.

**Parent Topic:**[Business Continuity Management](business-continuity-mangmt-overview.md)

