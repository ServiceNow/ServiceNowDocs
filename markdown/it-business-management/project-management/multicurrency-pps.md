---
title: Multicurrency in Project Management
description: Use the multicurrency feature to execute a project or part of a project in a different geographic location that has a different local currency.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Explore, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Multicurrency in Project Management

Use the multicurrency feature to execute a project or part of a project in a different geographic location that has a different local currency.

The feature helps you to view the cost details of the project in a currency that is different from your functional currency. The values in the project's cost plans, benefit plans, and corresponding cost fields of the project form are also converted to a currency that you specify as project currency. Therefore, you don't need to convert the project currency to the functional currency of the project when the project is executed at a location that uses a currency different than your functional currency.

## Activation information

Activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin to enable the multicurrency features in Project Management. Activating the plugin enables the project currency view in project, cost plans, and benefit plans forms. With the project currency view, you can manage your project financials and cost plans in multiple project currencies.

**Note:** Activating this plugin automatically activates PPM Standard \(com.snc.financial\_planning\_pmo\) plugin and therefore you get the option to switch between the default view and the project currency view.

## Project currency view

In addition to the default view in the Project form, there is Project Currency view, which you can optionally enable to view the multicurrency fields. You can enable this view from the form context menu. The view appears only when you activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.

Unlike the Default view, the Project Currency view contains multicurrency-related fields.

You can designate a currency other than the functional currency as the processing Project Currency for a project. The **Financials** tab of the Project form has the **Project currency** field. You can select an active currency from the Currencies \[fx\_currency\] table.

**Note:**

The **Project currency** field of a project becomes read-only field and locked down for updating the currency once you create a cost plan, cost plan breakdown, benefit plan, benefit plan breakdown, or an expense line for the project.

## Specify project currency in Demand

You can specify the project currency that you want to use for managing a project when you convert a demand to a project. You can continue to manage the demand using your functional currency, project currency, or a local currency. For more information, see [Multicurrency in Demand Management](../../planning-and-policy/concept/multicurrency-demand.md).

## Projects in Project Workspace

Track your projects in project currency in the Project Workspace. Create and monitor the cost plans and benefit plans for a project in project currency. For more information on project workspace, see [Project Workspace](../../project-workspace/concept/project-workspace-landing-page.md).

To view the cost component in project currency at the grid level and at the breakdown level, see [Create and manage cost plans and benefit plans for a project](../../project-management/task/view-plan-financials-in-project-workspace.md).

## Project status reports

To view the planned and actual cost status of your projects in project currency, open the overview and cost sections of [project status reports](../../project-management/task/project-status-report.md).

