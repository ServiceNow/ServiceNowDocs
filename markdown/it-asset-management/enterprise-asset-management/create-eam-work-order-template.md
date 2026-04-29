---
title: Create a template for your Enterprise Asset Management work orders
description: Create a work order template to automatically populate information, generate appropriate tasks, and create asset or part requirements for your work orders.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Create a template for your Enterprise Asset Management work orders

Create a work order template to automatically populate information, generate appropriate tasks, and create asset or part requirements for your work orders.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## About this task

Work order templates are added to the Field Service Catalog, which is part of the ServiceNow® Field Service Management application. You can access the Field Service Catalog by navigating to **All** &gt; **Field Service** &gt; **Catalog and Knowledge**. See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=australia&pubname=australia-field-service-management&ft:locale=en-US) for more information on the Field Service Management application.

**Note:** The Field Service Management application is automatically activated when you request and install the Enterprise Asset Management application from the ServiceNow Store. See [Install Enterprise Asset Management](request-enterprise-asset-management.md) for more details.

## Procedure

1.  From the Enterprise Asset Workspace, open the Work management view.

2.  On the **Work order templates** tab, select **New**.

    The Work Order Templates form opens in a new browser tab.

3.  On the form, fill in the fields.

<table id="table_a3q_rtc_kvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the work order template.

</td></tr><tr><td>

Short Description

</td><td>

Brief description of the work order template.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the work order template.

</td></tr><tr><td>

Checklist template

</td><td>

Checklist template of all items that you must complete as part of a work order.

</td></tr><tr><td>

Workflow**Note:** This field appears only if you select the Add icon ![](../../hardware-asset-management/image/add_content_icon.png) next to the **Name** field.

</td><td>

Workflow for work orders that this template is applied to.

</td></tr></tbody>
</table>4.  Add required tasks to the work order template.

    1.  Select **Add Task**.

    2.  On the Task information form, fill in the fields.

<table id="table_iyg_1bd_kvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task type

</td><td>

Type of task that you want to create. This field is automatically set to **Work Order Task**.

</td></tr><tr><td>

Name

</td><td>

Name of the task.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the task.

</td></tr><tr><td>

Parts and quantities

</td><td>

Asset or part that is required for completing the task. If you select a consumable asset or part, you must also specify the quantity that is required for completing the task. You can add multiple assets or parts to a single task.**Note:** Select the **Mandatory** check box for every asset or part that is required for completing the task.

</td></tr><tr><td>

Dispatch group

</td><td>

Group of agents to whom the task is assigned.

</td></tr><tr><td>

Depends on

</td><td>

Other tasks that must be completed before this task initiates.

</td></tr><tr><td>

Checklist template

</td><td>

Checklist template of all items that you must complete as part of the task.

</td></tr><tr><td>

Work type

</td><td>

Type of work that an agent must perform to complete the task. The options include **Break Fix**, **Calibration**, **Install**, and **Planned Maintenance**.

</td></tr></tbody>
</table>    3.  Repeat steps a and b for each additional task that you want to add to the work order template.

5.  Attach related knowledge base articles to the work order template.

    If your work order template is related to any knowledge base articles with useful reference information, attach the articles to the template.

    1.  In the Model Knowledges related list, select **New**.

    2.  On the Model Knowledge form, select the Lookup using list icon ![](../../software-asset-management2/image/search-icon.png) in the **Knowledge** field to search for and select the knowledge base article that you want to attach to the work order template.

    3.  Select **Submit** in the Model Knowledge form header.

    4.  Repeat steps a to c for each knowledge base article that you want to attach to the work order template.

6.  Select **Submit**.

    The Publish Template dialog box opens.

7.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Category|Field Service Catalog category to which you want to assign the work order template.|
    |Availability|Supported Field Service Catalog format for the work order template. The options are **Desktop Only**, **Mobile Only**, and **Desktop and Mobile**.|

8.  Select **Publish**.


## Result

The work order template is added to the Field Service Catalog.

