---
title: Project financials and Source-to-Pay Operations integration
description: Request, track, and manage procurement requests of assets for your projects.As a Project Manager, you can directly access the Source-to-Pay Operations shopping hub portal to place a request to meet your project requirements.After the purchase request is placed, you can track the request details such as Purchase line number, Purchased quantity, unit cost, tax, and state from Project Workspace.Once the requested purchase orders are approved and processed, a purchase order line and a cost plan is automatically created. You can view cost plans for the requisition in Project Workspace.
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage Projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Project financials and Source-to-Pay Operations integration

Request, track, and manage procurement requests of assets for your projects.

## Before you begin

[Install Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=activate-finance-spend-central&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)

Role required: it\_project\_manager

## About this task

Project managers can navigate from Project Workspace to procurement applications and create purchase requests for their projects. The ordered purchase requests are reflected in the Project Workspace. After the purchase request is processed, the purchase line, cost plan, and expense lines are automatically generated. For more information about the integration, see [Sourcing and Procurement Operations integration with Project Management](https://www.servicenow.com/docs/access?context=integration-psm-ppm&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US).![Financials SPO better together workflow diagram.](../images/Financials-SPO-better-together.png)

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace**.

2.  Open a project and select **Details** from the left menu.


**Parent Topic:**[Managing projects with Project Workspace](../../project-workspace/concept/use-projects-pw.md)

## Create purchase request

As a Project Manager, you can directly access the Source-to-Pay Operations shopping hub portal to place a request to meet your project requirements.

### Before you begin

Role required: it\_project\_manager

### Procedure

1.  In the project details page, select More Actions \(![More actions icon.](../../alignment-planner-workspace/images/icon-more-actions-horizontal.png)\) icon and select **Create Purchase Requests**.

    The Source-to-Pay Operations shopping hub portal opens in a new tab.

2.  Place the request for an asset.

    For more details on how to request a product using Source-to-Pay Common Architecture, see [Order a product with quick checkout](https://www.servicenow.com/docs/access?context=order-a-product&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US).

    **Note:** While placing the request for the asset, enter the project number in the **What project is this request for?** field.


## Track purchase line and purchase order lines

After the purchase request is placed, you can track the request details such as Purchase line number, Purchased quantity, unit cost, tax, and state from Project Workspace.

### Before you begin

Role required: it\_project\_manager

### Procedure

1.  Open the project selected while creating the purchase request.

2.  Select **Details** from the left menu.

3.  Select the **Purchase Lines** related list.

    A procurement specialist from the Source-to-Pay Operations approves the purchase requisition. Once the purchase order is created, purchase order line is automatically created in Project Workspace.

    To view the purchase order in Project Workspace:

    1.  Open the project selected while creating the purchase request.
    2.  Select **Details** from the left menu.
    3.  In the Details page, select the **Purchase Order Line** related list.
    **Note:** Every purchase order line creates a cost plan in the selected project.


## Tracking financials of procurement requests

Once the requested purchase orders are approved and processed, a purchase order line and a cost plan is automatically created. You can view cost plans for the requisition in Project Workspace.

### Before you begin

Role required: it\_project\_manager

### Procedure

1.  Open the project selected while creating the purchase request.

2.  Select **Details** from the left menu.

3.  Select the **Cost Plans** related list.

    **Note:** The cost plan is reflected in Financials along with additional details such as start and end fiscal period, planned cost plan breakdown for each fiscal period.

    As next steps, a purchase order is processed and an invoice is generated. An invoice line is created which captures the actual expense of the purchase request. You can view the expense lines generated from the processed invoice from Project Workspace.

    1.  Open the project selected while creating the purchase request.
    2.  Select **Financials** from the left menu.
    3.  Locate the cost plan created for the Purchase Order Line.
    4.  Scroll through the cost plan monthly breakdown, select the row options ![Vertical ellipses option to view expense lines](../../spw-financials/images/fin-options.png) for fiscal period in which the purchase order is created and select **View expense lines**.
    5.  In the Expense lines view, select the **Auto generated expense line for cost plan:** option.
    6.  Total expense incurred while generating the purchase order are displayed in the **Amount** field.

### Result

The processed purchase request is tagged to the selected project. Financials records such as cost plans and expense lines are automatically created and associated with the project expense.

