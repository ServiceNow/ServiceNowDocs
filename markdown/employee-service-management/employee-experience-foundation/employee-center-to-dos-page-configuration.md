---
title: Employee tasks page
description: Configure the tasks page for employees to view and complete all their tasks on a single page. You can configure the page by applying filters to show user approvals, content tasks, and more.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# Employee tasks page

Configure the tasks page for employees to view and complete all their tasks on a single page. You can configure the page by applying filters to show user approvals, content tasks, and more.

## My tasks overview

The My tasks page shows all open and completed tasks for an employee.

![My tasks page on Employee Center portal](../images/to-dos-ec.jpg "My tasks")

## Configure the tasks page

You control the type of open and completed tasks that appear by configuring the filters. The filters define the table and conditions that a task must meet for it to appear on the tasks page for an employee. You can associate one filter per table. For example, you can configure an Approvals filter by:

-   Associating it with the Approval \[sysapproval\_approver\] table with the conditions that the employee is the approver.
-   There is an entity that the approval is for.
-   The approval is in the requested state.

**Note:** The default order is due date. If you have too many filters and find that performance is affected, you can order the tasks by filter. To order by filter, you must enable filter prioritization and assign priority numbers for each filter.

For more information, see [Enable task configuration for approvals](../task/approval-hub-to-dos-page-filters.md).

## Configure Ask a question

Ask a question is a widget that establishes a communication link between a user with an HR Agent or queue to discuss HR tasks or cases. These configurations determine which HR agent or queue to use for communication. For HR tasks, the **Task support team** field defines the HR agent or queue that picks up any communication about the task when a user selects the Ask a question link. To use this option, activate the Connect Service Portal Widgets \(com.glide.connect.sp\_widgets\) plugin.

**Note:** For more information about **Connect**, see [Connect](https://www.servicenow.com/docs/access?context=c_Connect&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

For HR cases, define configuration under **Conversational Interfaces**.

**Note:** For more information about **Conversational Interfaces**, see [Conversational Interfaces](https://www.servicenow.com/docs/access?context=convint-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) and Setting up Agent Chat.

If your company is not using Connect Support, you can choose to hide the **Ask a question** link. To hide the Ask a question link, go to **sys\_properties.list** and find the **sn\_hr\_sp.hr\_ask\_a\_question\_enabled** property. Default value is **true**. To hide the Ask a Question on HR cases and tasks on the Employee Center, change the setting to **false**. For HR tasks, when Agent Workspace is selected in the **Task support team** drop-down, Virtual Agent is used. If Users and groups is selected, Connect Support is used. For more information, see [Adding an HR task to an HR case](../../human-resources/task/t_ViewAnHRTask.md).

Advanced Work Assignment To configure Advanced Work Assignment \(AWA\) for Agent Workspace, see [Advanced Work Assignment \(AWA\) for HR Service Delivery Agent Workspace overview](../../human-resources/concept/awa-hr-overview.md).

## Preconfigured filters

The following filters are included with the Employee Center application. You can use them or configure your own.

For more information, see [Task filters on My tasks](configurable-filters-experience.md)

